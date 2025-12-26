<!DOCTYPE html>
<html lang="sr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Virtuelna ambasada Ruske Federacije u Republici Srbiji</title>

<style>
    /* RESET I OSNOVA */
    body {
        font-family: "Segoe UI", Tahoma, sans-serif;
        margin: 0;
        background: #f4f6f8;
        color: #1a1a1a;
        overflow-x: hidden;
    }

    /* 1. BRZI LOADER (FADE OUT EFEKAT) */
    #loader-wrapper {
        position: fixed;
        top: 0; left: 0; width: 100%; height: 100%;
        background: #ffffff;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        z-index: 10000;
        transition: opacity 0.4s ease, visibility 0.4s;
    }

    .spinner {
        width: 40px;
        height: 40px;
        border: 4px solid #f3f3f3;
        border-top: 4px solid #1f3a5f;
        border-radius: 50%;
        animation: spin 0.8s linear infinite;
    }

    @keyframes spin { 100% { transform: rotate(360deg); } }

    /* 2. SPLASH SCREEN (KREMLJ) */
    #kremlj-screen {
        position: fixed;
        top: 0; left: 0; width: 100%; height: 100%;
        background: #000 url('kremlj.png') no-repeat center center;
        background-size: cover;
        z-index: 9998;
        display: none;
        opacity: 0;
        transition: opacity 0.5s ease;
        cursor: pointer;
    }

    #kremlj-screen.visible {
        display: block;
        opacity: 1;
    }

    .enter-text {
        position: absolute;
        bottom: 15%;
        width: 100%;
        text-align: center;
        color: #fff;
        font-size: clamp(18px, 4vw, 24px);
        font-weight: bold;
        text-shadow: 0 2px 10px rgba(0,0,0,0.8);
        text-transform: uppercase;
        letter-spacing: 2px;
        animation: pulse 1.5s infinite;
    }

    @keyframes pulse { 0%, 100% { opacity: 0.5; } 50% { opacity: 1; } }

    /* 3. GLAVNI SADRŽAJ */
    #main-content {
        display: none;
        opacity: 0;
        transition: opacity 0.5s ease;
    }

    header.ruska-zastava {
        height: 300px;
        background: url('download (10).jfif') center/cover no-repeat;
        display: flex; align-items: center; justify-content: center;
    }

    .overlay {
        background: rgba(0,0,0,0.6);
        padding: 2rem;
        border-radius: 8px;
        text-align: center;
        backdrop-filter: blur(3px);
    }

    h1 { color: #fff; margin: 0; font-size: clamp(20px, 5vw, 32px); }

    main { display: flex; min-height: calc(100vh - 300px); }

    nav {
        width: 280px;
        background: #fff;
        border-right: 1px solid #ddd;
        padding: 1.5rem;
    }

    .nav-button {
        display: block; width: 100%; padding: 12px;
        margin-bottom: 8px;
        background: #f8f9fa;
        border: 1px solid #dee2e6;
        border-radius: 4px;
        color: #1f3a5f;
        font-weight: 600;
        text-align: left;
        cursor: pointer;
        transition: 0.2s;
    }

    .nav-button:hover { background: #1f3a5f; color: #fff; transform: translateX(5px); }

    section { flex: 1; padding: 2rem; }
    .card { background: #fff; padding: 2rem; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.05); }
</style>
</head>

<body>

    <div id="loader-wrapper">
        <div class="spinner"></div>
        <p style="margin-top:15px; font-family: sans-serif; font-size: 14px; color: #666;">Učitavanje...</p>
    </div>

    <div id="kremlj-screen" onclick="enterSite()">
        <div class="enter-text">Kliknite za ulazak</div>
    </div>

    <div id="main-content">
        <header class="ruska-zastava">
            <div class="overlay">
                <h1>Virtuelna ambasada Ruske Federacije</h1>
            </div>
        </header>

        <main>
            <nav id="sidebar">
                <button class="nav-button" onclick="showSection('amb')">Kabinet ambasadora</button>
                <button class="nav-button" onclick="showSection('dip')">Diplomatska kancelarija</button>
                <button class="nav-button" onclick="showSection('pol')">Političko odeljenje</button>
                <button class="nav-button" onclick="showSection('eko')">Trgovinsko predstavništvo</button>
                <button class="nav-button" onclick="showSection('konz')">Konzularno odeljenje</button>
                <button class="nav-button" onclick="showSection('odbr')">Izaslanik odbrane</button>
                <button class="nav-button" onclick="showSection('kul')">Ruski dom</button>
                <button class="nav-button" onclick="showSection('adm')">Administracija</button>
            </nav>

            <section id="content">
                <div class="card">
                    <h2>Dobrodošli</h2>
                    <p>Izaberite odeljenje iz menija za pregled informacija.</p>
                </div>
            </section>
        </main>
    </div>

<script>
    // EKSPERTSKO UČITAVANJE
    window.addEventListener('load', function() {
        const loader = document.getElementById('loader-wrapper');
        const splash = document.getElementById('kremlj-screen');

        // Kratko kašnjenje samo radi stabilnosti UI-ja (0.5s umesto 1.5s)
        setTimeout(() => {
            loader.style.opacity = '0';
            setTimeout(() => {
                loader.style.visibility = 'hidden';
                splash.classList.add('visible');
            }, 400);
        }, 500);
    });

    function enterSite() {
        const splash = document.getElementById('kremlj-screen');
        const main = document.getElementById('main-content');
        
        splash.style.opacity = '0';
        setTimeout(() => {
            splash.style.display = 'none';
            main.style.display = 'block';
            setTimeout(() => main.style.opacity = '1', 50);
        }, 500);
    }

    const sections = {
        amb: `<div class="card"><h2>Kabinet ambasadora</h2><p>Nj. E. Aleksandar Bocan-Harčenko.</p></div>`,
        dip: `<div class="card"><h2>Diplomatska kancelarija</h2><p>Protokol i zvanična korespondencija.</p></div>`,
        pol: `<div class="card"><h2>Političko odeljenje</h2><p>Međudržavni odnosi i analitika.</p></div>`,
        eko: `<div class="card"><h2>Trgovinsko predstavništvo</h2><p>Katićeva 8–10, Beograd.</p></div>`,
        konz: `<div class="card"><h2>Konzularno odeljenje</h2><p>Deligradska 32, Beograd.</p></div>`,
        odbr: `<div class="card"><h2>Izaslanik odbrane</h2><p>Vojno-tehnička saradnja.</p></div>`,
        kul: `<div class="card"><h2>Ruski dom</h2><p>Kraljice Natalije 33, Beograd.</p></div>`,
        adm: `<div class="card"><h2>Administracija</h2><p>Tehnička podrška ambasade.</p></div>`
    };

    function showSection(key) {
        const container = document.getElementById("content");
        container.style.opacity = '0';
        setTimeout(() => {
            container.innerHTML = sections[key];
            container.style.opacity = '1';
        }, 200);
    }
</script>

</body>
</html>
