<!DOCTYPE html>
<html lang="sr">
<head>
    <meta charset="UTF-8">
    <title>Virtuelna ambasada Ruske Federacije u Republici Srbiji</title>

    <style>
        body {
            margin: 0;
            font-family: Arial, Helvetica, sans-serif;
            background-color: #f4f6f8;
        }

        /* GORNJI NASLOV */
        .top-title {
            padding: 20px;
            font-size: 28px;
            font-weight: bold;
            color: #0b5ed7;
        }

        /* HERO SEKCIJA */
        .hero {
            background-image: url("https://upload.wikimedia.org/wikipedia/commons/f/f3/Flag_of_Russia.svg");
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;

            height: 360px;
            padding: 50px 20px;
            color: #ffffff;
            text-align: center;
            position: relative;
        }

        .hero::before {
            content: "";
            position: absolute;
            inset: 0;
            background-color: rgba(0, 0, 0, 0.5);
        }

        .hero * {
            position: relative;
            z-index: 1;
        }

        .hero h1 {
            font-size: 32px;
            margin-bottom: 10px;
        }

        .hero hr {
            width: 60%;
            border: 1px solid rgba(255, 255, 255, 0.6);
            margin: 20px auto;
        }

        .hero p {
            font-size: 16px;
        }

        /* LOGOTIPI U HERO */
        .logos {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin-top: 25px;
        }

        .logos img {
            height: 80px;
            background-color: #ffffff;
            padding: 8px;
            border-radius: 6px;
        }

        /* GLAVNI SADRŽAJ */
        .container {
            display: flex;
            max-width: 1200px;
            margin: 30px auto;
            gap: 30px;
            padding: 0 20px;
        }

        /* LEVI MENI */
        .sidebar {
            width: 300px;
            background-color: #ffffff;
            padding: 20px;
            border-radius: 6px;
        }

        .sidebar h3 {
            margin-top: 0;
            color: #0b5ed7;
        }

        .sidebar ul {
            list-style: none;
            padding: 0;
        }

        .sidebar li {
            padding: 8px 0;
            border-bottom: 1px solid #e0e0e0;
        }

        /* DESNI SADRŽAJ */
        .content {
            flex: 1;
            background-color: #ffffff;
            padding: 25px;
            border-radius: 6px;
        }

        .content h2 {
            margin-top: 0;
        }

        .institution {
            margin-bottom: 25px;
        }

        .institution h3 {
            margin-bottom: 5px;
            color: #0b5ed7;
        }

        .institution p {
            margin: 5px 0;
        }
    </style>
</head>

<body>

<div class="top-title">
    DiploSimulacijaFPN
</div>

<div class="hero">
    <h1>Virtuelna ambasada Ruske Federacije u Republici Srbiji</h1>
    <hr>
    <p>Zvanična struktura i unutrašnja organizacija diplomatske misije</p>

    <div class="logos">
        <!-- LOGOTIP RUSKOG DOMA -->
        <img src="https://ruskidom.rs/wp-content/uploads/2022/06/logo-ruski-dom.png"
             alt="Ruski dom u Beogradu">

        <!-- LOGOTIP MINISTARSTVA ODBRANE RF -->
        <img src="https://upload.wikimedia.org/wikipedia/commons/5/5d/Emblem_of_the_Ministry_of_Defence_of_the_Russian_Federation.svg"
             alt="Ministarstvo odbrane Ruske Federacije">
    </div>
</div>

<div class="container">

    <div class="sidebar">
        <h3>Prostorije ambasade</h3>
        <ul>
            <li>Kabinet ambasadora</li>
            <li>Diplomatska kancelarija</li>
            <li>Političko odeljenje</li>
            <li>Ekonomsko odeljenje</li>
            <li>Konzularno odeljenje</li>
            <li>Kancelarija vojnog atašea</li>
            <li>Ruski dom</li>
        </ul>
    </div>

    <div class="content">
        <h2>Dobrodošli</h2>

        <p>
            Ova virtuelna simulacija predstavlja unutrašnju organizaciju Ambasade
            Ruske Federacije u Republici Srbiji, uključujući ključne institucije,
            nadležnosti i funkcije diplomatskog osoblja.
        </p>

        <div class="institution">
            <h3>Ambasador Ruske Federacije</h3>
            <p><strong>Titula:</strong> Izvanredni i opunomoćeni ambasador</p>
            <p><strong>Uloga:</strong> Najviši predstavnik Ruske Federacije u Republici Srbiji,
                odgovoran za ukupno vođenje diplomatske misije.</p>
        </div>

        <div class="institution">
            <h3>Vojni ataše</h3>
            <p><strong>Institucija:</strong> Ministarstvo odbrane Ruske Federacije</p>
            <p><strong>Uloga:</strong> Predstavlja oružane snage Ruske Federacije,
                prati vojno-političke odnose i saradnju sa Republikom Srbijom.</p>
        </div>

        <div class="institution">
            <h3>Ruski dom u Beogradu</h3>
            <p><strong>Institucija:</strong> Federalna agencija „Rossotrudničestvo“</p>
            <p><strong>Uloga:</strong> Kulturna, obrazovna i humanitarna saradnja,
                promocija ruskog jezika, kulture i nauke.</p>
        </div>

    </div>

</div>

</body>
</html>
