<!DOCTYPE html>
<html lang="sr">
<head>
<meta charset="UTF-8">
<title>Virtuelna ambasada Ruske Federacije u Republici Srbiji</title>

<style>
body {
    font-family: "Segoe UI", Arial, sans-serif;
    margin: 0;
    background: #f4f6f8;
    color: #1a1a1a;
    overflow-x: hidden;
}

/* 1. LOADING SCREEN */
#loader-wrapper {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #ffffff;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    z-index: 10000;
}

.spinner {
    width: 50px;
    height: 50px;
    border: 5px solid #f3f3f3;
    border-top: 5px solid #1f3a5f;
    border-radius: 50%;
    animation: spin 1s linear infinite;
}

@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

/* 2. KREMLJ EKRAN (SPLASH SCREEN) */
#kremlj-screen {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: black url('kremlj.png') no-repeat center center;
    background-size: cover;
    z-index: 9998;
    display: none; /* Prikazuje se nakon loadera */
    cursor: pointer;
}

#kremlj-screen .enter-text {
    position: absolute;
    bottom: 12%;
    width: 100%;
    text-align: center;
    color: white;
    font-size: 26px;
    text-shadow: 2px 2px 15px rgba(0,0,0,1);
    font-weight: bold;
    letter-spacing: 2px;
    animation: pulse 2s infinite;
}

@keyframes pulse {
    0% { opacity: 0.4; transform: scale(1); }
    50% { opacity: 1; transform: scale(1.05); }
    100% { opacity: 0.4; transform: scale(1); }
}

/* 3. GLAVNI SADRŽAJ */
#main-content {
    display: none; 
}

header.ruska-zastava {
    height: 320px;
    background-image: url('download (10).jfif');
    background-size: cover;
    background-position: center;
    display: flex;
    align-items: center;
    justify-content: center;
}

header.ruska-zastava .overlay {
    background: rgba(0,0,0,0.6);
    padding: 30px 50px;
    border-radius: 10px;
    text-align: center;
}

header.ruska-zastava h1 { margin: 0; font-size: 32px; color: #ffffff; }

main { display: flex; min-height: calc(100vh - 320px); }

nav {
    width: 300px;
    background: #ffffff;
    border-right: 1px solid #ddd;
    padding: 20px;
}

.nav-button {
    display: block;
    width: 100%;
    padding: 12px 15px;
    background-color: #f8f9fa;
    color: #1f3a5f;
    border: 1px solid #d1d8e0;
    border-radius: 6px;
    text-align: left;
    font-weight: 600;
    cursor: pointer;
    margin-bottom: 10px;
    transition: 0.3s ease;
}

.nav-button:hover {
    background-color: #1f3a5f;
    color: #ffffff;
    padding-left: 20px;
}

section { flex: 1; padding: 40px; }
.card { background: #ffffff; padding: 30px; border-radius: 8px; box-shadow: 0 4px 12px rgba(0,0,0,0.1); }
</style>
</head>

<body>

<div id="loader-wrapper">
    <div class="spinner"></div>
    <p style="margin-top: 20px; color: #1f3a5f; font-weight: bold; letter-spacing: 1px;">SISTEM SE UČITAVA...</p>
</div>

<div id="kremlj-screen" onclick="enterSite()">
    <div class="enter-text">KLIKNITE ZA ULAZAK U AMBASADU</div>
</div>

<div id="main-content">
    <header class="ruska-zastava">
        <div class="overlay">
            <h1>Virtuelna ambasada Ruske Federacije u Republici Srbiji</h1>
            <p style="color:white; margin-top:10px; font-style: italic;">Zvanična digitalna struktura diplomatske misije</p>
        </div>
    </header>

    <main>
        <nav>
            <h3 style="color: #1f3a5f;">Prostorije</h3>
            <ul style="list-style: none; padding: 0;">
                <li><button class="nav-button" onclick="showSection('amb')">Kabinet ambasadora</button></li>
                <li><button class="nav-button" onclick="showSection('dip')">Diplomatska kancelarija</button></li>
                <li><button class="nav-button" onclick="showSection('pol')">Političko odeljenje</button></li>
                <li><button class="nav-button" onclick="showSection('eko')">Trgovinsko predstavništvo</button></li>
                <li><button class="nav-button" onclick="showSection('konz')">Konzularno odeljenje</button></li>
                <li><button class="nav-button" onclick="showSection('odbr')">Izaslanik odbrane</button></li>
                <li><button class="nav-button" onclick="showSection('kul')">Ruski dom</button></li>
                <li><button class="nav-button" onclick="showSection('adm')">Administrativno-tehnička služba</button></li>
            </ul>
        </nav>

        <section id="content">
            <div class="card">
                <h2>Dobrodošli</h2>
                <hr style="border: 0; border-top: 1px solid #eee; margin: 20px 0;">
                <p>Uspešno ste pristupili informacionom sistemu Ambasade Ruske Federacije. Koristite meni sa leve strane za navigaciju kroz odeljenja.</p>
            </div>
        </section>
    </main>
</div>

<script>
// Logika za Loader i Splash Screen
window.onload = function() {
    setTimeout(function() {
        // Sakrij loader
        document.getElementById('loader-wrapper').style.display = 'none';
        // Prikaži sliku Kremlja (kremlj.png)
        document.getElementById('kremlj-screen').style.display = 'block';
    }, 1500); // Traje 1.5 sekundi
};

// Funkcija za ulazak na glavni deo sajta
function enterSite() {
    document.getElementById('kremlj-screen').style.display = 'none';
    document.getElementById('main-content').style.display = 'block';
}

// Sadržaj sekcija
const sections = {
    amb: `<div class="card"><h2>Kabinet ambasadora</h2><p><strong>Ambasador:</strong> Nj. E. Aleksandar Bocan-Harčenko.</p></div>`,
    dip: `<div class="card"><h2>Diplomatska kancelarija</h2><p>Protokol i korespodencija misije.</p></div>`,
    pol: `<div class="card"><h2>Političko odeljenje</h2><p>Analiza i saradnja na međudržavnom nivou.</p></div>`,
    eko: `<div class="card"><h2>Trgovinsko predstavništvo</h2><p>Katićeva 8–10
