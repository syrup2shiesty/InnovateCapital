<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>INNOVATE CAPITAL | Trading Mentorship</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, Helvetica, sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: #050505;
            color: white;
            line-height: 1.6;
        }

        :root {
            --blue: #8ed8ff;
            --blue-dark: #55b9e8;
            --white: #ffffff;
            --black: #050505;
            --grey: #b8b8b8;
            --card: #0d0d0d;
        }

        /* NAVIGATION */

        nav {
            width: 100%;
            position: fixed;
            top: 0;
            left: 0;
            z-index: 1000;
            background: rgba(5, 5, 5, 0.92);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(142, 216, 255, 0.15);
        }

        .nav-container {
            max-width: 1200px;
            margin: auto;
            padding: 20px 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 22px;
            font-weight: 800;
            letter-spacing: 2px;
            color: white;
        }

        .logo span {
            color: var(--blue);
        }

        .nav-links {
            display: flex;
            gap: 30px;
            list-style: none;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-size: 14px;
            transition: 0.3s;
        }

        .nav-links a:hover {
            color: var(--blue);
        }

        /* HERO */

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 120px 20px 80px;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: "";
            position: absolute;
            width: 600px;
            height: 600px;
            background: var(--blue);
            opacity: 0.07;
            filter: blur(130px);
            border-radius: 50%;
            top: 10%;
            left: 50%;
            transform: translateX(-50%);
        }

        .hero-content {
            max-width: 900px;
            position: relative;
            z-index: 1;
        }

        .small-heading {
            color: var(--blue);
            font-size: 14px;
            letter-spacing: 4px;
            text-transform: uppercase;
            margin-bottom: 20px;
            font-weight: bold;
        }

        .hero h1 {
            font-size: clamp(50px, 9vw, 105px);
            line-height: 0.95;
            letter-spacing: -3px;
            margin-bottom: 25px;
        }

        .hero h1 span {
            color: var(--blue);
        }

        .hero p {
            max-width: 680px;
            margin: auto;
            color: #cfcfcf;
            font-size: 18px;
        }

        .hero-buttons {
            margin-top: 40px;
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .button {
            display: inline-block;
            padding: 15px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: 0.3s;
        }

        .primary-button {
            background: var(--blue);
            color: #050505;
        }

        .primary-button:hover {
            background: white;
            transform: translateY(-3px);
        }

        .secondary-button {
            border: 1px solid #444;
            color: white;
        }

        .secondary-button:hover {
            border-color: var(--blue);
            color: var(--blue);
        }

        /* GENERAL */

        section {
            padding: 100px 20px;
        }

        .container {
            max-width: 1100px;
            margin: auto;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title .label {
            color: var(--blue);
            text-transform: uppercase;
            letter-spacing: 3px;
            font-size: 13px;
            font-weight: bold;
        }

        .section-title h2 {
            font-size: 42px;
            margin-top: 10px;
        }

        .section-title p {
            color: #999;
            max-width: 650px;
            margin: 15px auto 0;
        }

        /* ABOUT */

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-text h3 {
            font-size: 32px;
            margin-bottom: 20px;
        }

        .about-text h3 span {
            color: var(--blue);
        }

        .about-text p {
            color: #bdbdbd;
            margin-bottom: 18px;
        }

        .founder-card {
            background: linear-gradient(145deg, #111111, #080808);
            border: 1px solid rgba(142, 216, 255, 0.2);
            padding: 45px;
            border-radius: 12px;
            position: relative;
            overflow: hidden;
        }

        .founder-card::after {
            content: "";
            position: absolute;
            width: 120px;
            height: 120px;
            background: var(--blue);
            opacity: 0.08;
            border-radius: 50%;
            right: -40px;
            bottom: -40px;
        }

        .founder-card .role {
            color: var(--blue);
            text-transform: uppercase;
            letter-spacing: 2px;
            font-size: 12px;
            font-weight: bold;
        }

        .founder-card h3 {
            font-size: 35px;
            margin: 10px 0;
        }

        .founder-card p {
            color: #aaa;
        }

        /* MENTORSHIP */

        .mentorship {
            background: #080808;
        }

        .features {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .feature-card {
            background: var(--card);
            border: 1px solid #1c1c1c;
            padding: 35px 28px;
            border-radius: 10px;
            transition: 0.3s;
        }

        .feature-card:hover {
            transform: translateY(-6px);
            border-color: var(--blue);
        }

        .feature-number {
            color: var(--blue);
            font-size: 14px;
            font-weight: bold;
            margin-bottom: 20px;
        }

        .feature-card h3 {
            font-size: 21px;
            margin-bottom: 12px;
        }

        .feature-card p {
            color: #999;
            font-size: 15px;
        }

        /* APPROACH */

        .approach-box {
            border: 1px solid rgba(142, 216, 255, 0.2);
            border-radius: 12px;
            padding: 60px;
            text-align: center;
            background: linear-gradient(
                145deg,
                rgba(142,216,255,0.05),
                rgba(0,0,0,0)
            );
        }

        .approach-box h2 {
            font-size: 38px;
            margin-bottom: 20px;
        }

        .approach-box h2 span {
            color: var(--blue);
        }

        .approach-box p {
            color: #aaa;
            max-width: 750px;
            margin: auto;
            font-size: 17px;}


/* =========================
   VARIABLES
========================= */

:root {
    --black: #050607;
    --black2: #0a0d10;
    --blue: #9ddcff;
    --blue-dark: #67c8ff;
    --white: #ffffff;
    --grey: #a8b3bd;
    --line: rgba(157,220,255,0.18);
}


/* =========================
   CONTAINER
========================= */

.container {
    width: 90%;
    max-width: 1150px;
    margin: auto;
}


/* =========================
   NAVBAR
========================= */

nav {
    position: fixed;
    top: 0;
    left: 0;

    width: 100%;

    z-index: 999;

    background: rgba(5,6,7,0.88);

    backdrop-filter: blur(15px);

    border-bottom: 1px solid rgba(157,220,255,0.12);
}

.navbar {
    height: 75px;

    display: flex;

    align-items: center;

    justify-content: space-between;
}

.brand {
    display: flex;

    align-items: center;

    gap: 12px;

    font-size: 13px;

    font-weight: bold;

    letter-spacing: 4px;
}

.brand-icon {
    width: 35px;
    height: 35px;

    border: 1px solid var(--blue);

    display: flex;

    align-items: center;
    justify-content: center;

    color: var(--blue);

    font-family: Georgia, serif;

    font-size: 20px;
}

.nav-links {
    display: flex;

    gap: 30px;

    list-style: none;
}

.nav-links a {
    color: #c5ced5;

    font-size: 14px;

    transition: 0.3s;
}

.nav-links a:hover {
    color: var(--blue);
}

.nav-button {
    border: 1px solid var(--blue);

    color: var(--blue);

    padding: 10px 19px;

    transition: 0.3s;
}

.nav-button:hover {
    background: var(--blue);

    color: #050607;
}


/* =========================
   HERO
========================= */

.hero {
    min-height: 100vh;

    display: flex;

    align-items: center;

    padding-top: 100px;

    background:

        radial-gradient(
            circle at 80% 20%,
            rgba(103,200,255,0.13),
            transparent 30%
        );
}

.hero-grid {
    display: grid;

    grid-template-columns: 1fr 1fr;

    gap: 70px;

    align-items: center;
}

.small-title {
    color: var(--blue);

    font-size: 12px;

    letter-spacing: 4px;

    margin-bottom: 25px;
}

.hero h1 {
    font-family: Georgia, "Times New Roman", serif;

    font-size: clamp(55px, 8vw, 105px);

    line-height: 0.9;

    font-weight: normal;

    letter-spacing: -5px;

    margin-bottom: 30px;
}

.hero h1 span {
    display: block;

    color: var(--blue);
}

.hero-text {
    max-width: 650px;

    color: var(--grey);

    font-size: 17px;

    line-height: 1.8;

    margin-bottom: 35px;
}

.buttons {
    display: flex;

    gap: 15px;

    flex-wrap: wrap;
}

.button {
    padding: 14px 25px;

    border: 1px solid var(--blue);

    font-weight: bold;

    transition: 0.3s;
}

.primary {
    background: var(--blue);

    color: #050607;
}

.primary:hover {
    background: white;

    border-color: white;

    transform: translateY(-3px);
}

.secondary {
    color: var(--blue);
}

.secondary:hover {
    background: rgba(157,220,255,0.08);

    transform: translateY(-3px);
}


/* =========================
   LOGO
========================= */

.logo-area {
    display: flex;

    justify-content: center;

    align-items: center;
}

.logo-container {
    width: 390px;

    max-width: 90%;

    aspect-ratio: 1 / 1;

    background: #000000;

    border: 1px solid rgba(157,220,255,0.22);

    display: flex;

    align-items: center;

    justify-content: center;

    position: relative;

    box-shadow:
        0 0 90px rgba(103,200,255,0.08);
}

.logo-container::before {
    content: "";

    position: absolute;

    width: 18px;
    height: 18px;

    top: -1px;
    left: -1px;

    border-top: 1px solid var(--blue);
    border-left: 1px solid var(--blue);
}

.logo-container::after {
    content: "";

    position: absolute;

    width: 18px;
    height: 18px;

    bottom: -1px;
    right: -1px;

    border-right: 1px solid var(--blue);
    border-bottom: 1px solid var(--blue);
}

.logo-svg {
    width: 85%;

    height: 85%;
}


/* =========================
   SECTIONS
========================= */

section {
    padding: 110px 0;

    border-top: 1px solid rgba(255,255,255,0.06);
}

.section-label {
    color: var(--blue);

    font-size: 11px;

    letter-spacing: 4px;

    margin-bottom: 18px;

    text-transform: uppercase;
}

h2 {
    font-family: Georgia, "Times New Roman", serif;

    font-size: clamp(45px, 6vw, 70px);

    line-height: 1;

    font-weight: normal;

    margin-bottom: 30px;
}

.blue {
    color: var(--blue);
}


/* =========================
   ABOUT
========================= */

.about-grid {
    display: grid;

    grid-template-columns: 0.8fr 1.2fr;

    gap: 80px;
}

.about-text {
    color: var(--grey);

    font-size: 17px;

    line-height: 1.9;
}

.about-text strong {
    color: white;
}

.stats {
    display: grid;

    grid-template-columns: 1fr 1fr;

    gap: 15px;

    margin-top: 35px;
}

.stat {
    padding: 28px;

    background: rgba(255,255,255,0.035);

    border: 1px solid var(--line);

    transition: 0.3s;
}

.stat:hover {
    border-color: rgba(157,220,255,0.5);

    transform: translateY(-4px);
}

.stat-number {
    color: var(--blue);

    font-family: Georgia, serif;

    font-size: 38px;
}

.stat-description {
    color: #89949e;

    font-size: 13px;
}


/* =========================
   APPROACH
========================= */

.cards {
    display: grid;

    grid-template-columns: repeat(3, 1fr);

    gap: 20px;

    margin-top: 45px;
}

.card {
    min-height: 250px;

    padding: 32px;

    background:
        linear-gradient(
            145deg,
            rgba(157,220,255,0.06),
            rgba(255,255,255,0.015)
        );

    border: 1px solid var(--line);

    transition: 0.3s;
}

.card:hover {
    transform: translateY(-7px);

    border-color: rgba(157,220,255,0.5);
}

.card-number {
    color: var(--blue);

    font-size: 11px;

    letter-spacing: 3px;

    margin-bottom: 45px;
}

.card h3 {
    font-size: 21px;

    margin-bottom: 13px;
}

.card p {
    color: #929da7;

    font-size: 14px;

    line-height: 1.7;
}


/* =========================
   CONTACT
========================= */

.contact-box {
    padding: 65px;

    border: 1px solid rgba(157,220,255,0.25);

    background:
        linear-gradient(
            135deg,
            rgba(157,220,255,0.09),
            rgba(255,255,255,0.02)
        );

    display: grid;

    grid-template-columns: 1fr auto;

    gap: 50px;

    align-items: center;
}

.contact-text {
    color: var(--grey);

    max-width: 650px;

    line-height: 1.8;
}

.contact-buttons {
    display: flex;

    flex-direction: column;

    gap: 12px;

    min-width: 220px;
}

.phone {
    text-align: center;

    font-size: 14px;

    color: white;
}


/* =========================
   FOOTER
========================= */

footer {
    padding: 50px 0 30px;

    border-top: 1px solid rgba(255,255,255,0.07);
}

.footer-top {
    display: flex;

    justify-content: space-between;

    align-items: center;

    margin-bottom: 35px;
}

.footer-logo {
    color: var(--blue);

    letter-spacing: 4px;

    font-size: 14px;
}

.footer-links {
    display: flex;

    gap: 20px;

    color: #7d8992;

    font-size: 13px;
}

.risk {
    border-top: 1px solid rgba(255,255,255,0.07);

    padding-top: 25px;

    color: #707b84;

    font-size: 12px;

    line-height: 1.8;
}

.risk strong {
    color: #aab6c2;
}

.copyright {
    color: #505960;

    font-size: 11px;

    margin-top: 20px;
}


/* =========================
   MOBILE
========================= */

@media (max-width: 850px) {

    .nav-links {
        display: none;
    }

    .hero-grid {
        grid-template-columns: 1fr;
    }

    .about-grid {
        grid-template-columns: 1fr;
    }

    .cards {
        grid-template-columns: 1fr;
    }

    .contact-box {
        grid-template-columns: 1fr;

        padding: 40px 28px;
    }

    .contact-buttons {
        width: 100%;
    }

    .logo-area {
        margin-top: 30px;
    }
}

@media (max-width: 550px) {

    .brand {
        font-size: 10px;

        letter-spacing: 2px;
    }

    .nav-button {
        padding: 8px 12px;

        font-size: 12px;
    }

    .hero h1 {
        font-size: 55px;
    }

    .stats {
        grid-template-columns: 1fr;
    }

    .footer-top {
        flex-direction: column;

        align-items: flex-start;

        gap: 20px;
    }

    .footer-links {
        flex-wrap: wrap;
    }
}

</style>

</head>


<body>


<!-- =========================
     NAVIGATION
========================= -->

<nav>

<div class="container navbar">

    <a href="#home" class="brand">

        <div class="brand-icon">
            I
        </div>

        INNOVATE CAPITAL

    </a>


    <ul class="nav-links">

        <li>
            <a href="#about">
                About
            </a>
        </li>

        <li>
            <a href="#approach">
                Approach
            </a>
        </li>

        <li>
            <a href="#contact">
                Contact
            </a>
        </li>

    </ul>


    <a
        href="https://chat.whatsapp.com/Lf4GFgYb9dbGUpiXBc6APm"
        target="_blank"
        class="nav-button"
    >
        Join Us
    </a>

</div>

</nav>



<!-- =========================
     HERO
========================= -->

<section class="hero" id="home">

<div class="container hero-grid">


    <div>

        <div class="small-title">
            XAUUSD • FOREX • MENTORSHIP
        </div>


        <h1>

            TRADE WITH

            <span>
                INTENTION.
            </span>

        </h1>


        <p class="hero-text">

            INNOVATE CAPITAL focuses solely on XAUUSD.

            With 4 years of experience in the forex trading market,
            we simplify the concepts, methods and processes we use
            today into a clear learning experience designed to help
            traders understand the market and identify trading
            opportunities.

        </p>


        <div class="buttons">

            <a
                href="https://chat.whatsapp.com/Lf4GFgYb9dbGUpiXBc6APm"
                target="_blank"
                class="button primary"
            >
                JOIN THE GROUP
            </a>


            <a
                href="#about"
                class="button secondary"
            >
                EXPLORE
            </a>

        </div>

    </div>



    <!-- =========================
         LOGO
    ========================== -->

    <div class="logo-area">

        <div class="logo-container">


            <svg
                class="logo-svg"
                viewBox="0 0 500 500"
                xmlns="http://www.w3.org/2000/svg"
            >

                <!-- Main I -->

                <text
                    x="250"
                    y="245"
                    text-anchor="middle"
                    font-family="Georgia, serif"
                    font-size="220"
                    fill="#e8d5c3"
                >
                    I
                </text>


                <!-- Left Laurel -->

                <g
                    fill="none"
                    stroke="#b9b9b9"
                    stroke-width="5"
                    stroke-linecap="round"
                >

                    <path
                        d="M90 285
                           C125 315 165 330 220 330"
                    />

                    <path
                        d="M105 298
                           C95 286 86 276 78 264"
                    />

                    <path
                        d="M120 306
                           C112 292 105 281 100 267"
                    />

                    <path
                        d="M137 313
                           C130 298 126 285 123 270"
                    />

                    <path
                        d="M154 318
                           C149 302 147 289 146 274"
                    />

                    <path
                        d="M172 323
                           C168 307 168 294 169 279"
                    />

                    <path
                        d="M190 326
                           C188 311 190 298 192 284"
                    />

                    <path
                        d="M208 329
                           C208 315 211 303 215 290"
                    />

                </g>


                <!-- Right Laurel -->

                <g
                    fill="none"
                    stroke="#b9b9b9"
                    stroke-width="5"
                    stroke-linecap="round"
                >

                    <path
                        d="M410 285
                           C375 315 335 330 280 330"
                    />

                    <path
                        d="M395 298
                           C405 286 414 276 422 264"
                    />

                    <path
                        d="M380 306
                           C388 292 395 281 400 267"
                    />

                    <path
                        d="M363 313
                           C370 298 374 285 377 270"
                    />

                    <path
                        d="M346 318
                           C351 302 353 289 354 274"
                    />

                    <path
                        d="M328 323
                           C332 307 332 294 331 279"
                    />

                    <path
                        d="M310 326
                           C312 311 310 298 308 284"
                    />

                    <path
                        d="M292 329
                           C292 315 289 303 285 290"
                    />

                </g>


                <!-- Company Name -->

                <text
                    x="250"
                    y="375"
                    text-anchor="middle"
                    font-family="Arial, sans-serif"
                    font-size="35"
                    letter-spacing="10"
                    fill="#ffffff"
                >
                    INNOVATE
                </text>


                <text
                    x="250"
                    y="415"
                    text-anchor="middle"
                    font-family="Arial, sans-serif"
                    font-size="19"
                    letter-spacing="9"
                    fill="#ffffff"
                >
                    CAPITAL
                </text>

            </svg>

        </div>

    </div>

</div>

</section>



<!-- =========================
     ABOUT
========================= -->

<section id="about">

<div class="container about-grid">


    <div>

        <div class="section-label">
            01 / ABOUT
        </div>


        <h2>

            Focused.

            <br>

            <span class="blue">
                Simple.
            </span>

            <br>

            Intentional.

        </h2>

    </div>



    <div>

        <p class="about-text">

            <strong>INNOVATE CAPITAL</strong>
            focuses solely on

            <strong>XAUUSD</strong>.

            With 4 years of experience in the forex trading market,
            I summarize and simplify the concepts, methods and
            processes I use today and teach them in a way that is
            easier to understand.

            <br><br>

            The goal is to help learners understand the market,
            develop their own process and learn how to identify
            potential trading opportunities.

        </p>


        <div class="stats">


            <div class="stat">

                <div class="stat-number">
                    04+
                </div>

                <div class="stat-description">
                    Years of forex market experience
                </div>

            </div>


            <div class="stat">

                <div class="stat-number">
                    XAUUSD
                </div>

                <div class="stat-description">
                    Primary market focus
                </div>

            </div>


        </div>

    </div>

</div>

</section>



<!-- =========================
     APPROACH
========================= -->

<section id="approach">

<div class="container">


    <div class="section-label">
        02 / OUR APPROACH
    </div>


    <h2>

        A clearer way to

        <br>

        <span class="blue">
            learn trading.
        </span>

    </h2>



    <div class="cards">


        <div class="card">

            <div class="card-number">
                01 — FOCUS
            </div>

            <h3>
                XAUUSD Specialisation
            </h3>

            <p>

                We keep the learning focused on Gold,
                allowing concepts to be studied around
                one primary market.

            </p>

        </div>



        <div class="card">

            <div class="card-number">
                02 — SIMPLIFY
            </div>

            <h3>
                Complex → Simple
            </h3>

            <p>

                Trading concepts are broken down into
                straightforward explanations so learners
                can understand the reasoning behind a setup.

            </p>

        </div>



        <div class="card">

            <div class="card-number">
                03 — DEVELOP
            </div>

            <h3>
                Build Your Process
            </h3>

            <p>

                Learn how to analyse the market and develop
                a structured approach to making trading decisions.

            </p>

        </div>


    </div>

</div>

</section>



<!-- =========================
     CONTACT
========================= -->

<section id="contact">

<div class="container">


    <div class="contact-box">


        <div>

            <div class="section-label">
                03 / GET STARTED
            </div>


            <h2>
                Ready to learn?
            </h2>


            <p class="contact-text">

                If you're interested in learning how experienced
                professionals approach the market and want to build
                a stronger understanding of XAUUSD, contact
                INNOVATE CAPITAL and join the community.

            </p>

        </div>



        <div class="contact-buttons">


            <a
                href="https://chat.whatsapp.com/Lf4GFgYb9dbGUpiXBc6APm"
                target="_blank"
                class="button primary"
            >
                JOIN WHATSAPP
            </a>


            <a
                href="tel:+27699309058"
                class="button secondary"
            >
                CALL / WHATSAPP
            </a>


            <div class="phone">
                +27 69 930 9058
            </div>


        </div>


    </div>

</div>

</section>



<!-- =========================
     FOOTER
========================= -->

<footer>

<div class="container">


    <div class="footer-top">


        <div class="footer-logo">
            INNOVATE CAPITAL
        </div>


        <div class="footer-links">

            <a href="#about">
                About
            </a>

            <a href="#approach">
                Approach
            </a>

            <a href="#contact">
                Contact
            </a>

        </div>


    </div>



    <!-- RISK DISCLAIMER -->

    <div class="risk">

        <strong>
            RISK DISCLAIMER:
        </strong>

        Forex and leveraged trading involve substantial risk and may
        result in the loss of some or all of your capital.

        Past experience, examples, educational material or trading
        results do not guarantee future results.

        INNOVATE CAPITAL does not guarantee profits and does not
        stand liable for losses that may occur from trading decisions.

        Trading should only be undertaken with funds you can afford
        to lose.

        This website is for educational and informational purposes
        and should not be interpreted as personalised financial advice.

    </div>


    <div class="copyright">

        © 2026 INNOVATE CAPITAL. All rights reserved.

    </div>


</div>

</footer>


</body>
</html>
