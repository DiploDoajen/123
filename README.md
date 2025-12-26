<html lang="sr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Virtuelna ambasada Ruske Federacije u Republici Srbiji</title>

<style>
    :root {
        --primary-blue: #1f3a5f;
        --accent-red: #d52b1e;
        --bg-color: #f4f6f8;
    }

    body {
        font-family: "Segoe UI", Tahoma, sans-serif;
        margin: 0;
        background: var(--bg-color);
        color: #1a1a1a;
        overflow-x: hidden;
    }

    /* 1. EKSPERTSKI LOADER (PRECIZNA ESTETIKA) */
    #loader-wrapper {
        position: fixed;
        top: 0; left: 0; width: 100%; height: 100%;
        background: #ffffff;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        z-index: 10000;
        transition: opacity 0.6s cubic-bezier(0.4, 0, 0.2, 1);
    }

    .loader-content {
        text-align: center;
        width: 250px;
    }

    .loading-text {
        font-size: 11px;
        text-transform: uppercase;
        letter-spacing: 4px;
        color: var(--primary-blue);
        margin-bottom: 15px;
        font-weight: 700;
    }

    .progress-container {
        width: 100%;
        height: 2px;
        background: #eee;
        overflow: hidden;
        position: relative;
    }

    .progress-bar {
        width: 0%;
        height: 100%;
        background: var(--primary-blue);
        animation: progressMove 1.2s cubic-bezier(0.65, 0.05, 0.36, 1) forwards;
    }

    @keyframes progressMove {
        0% { width: 0%; }
        100% { width: 100%; }
    }

    /* 2. SPLASH SCREEN (KREMLJ) */
    #kremlj-screen {
        position: fixed;
        top: 0; left: 0; width: 100%; height: 100%;
        background: #000 url('kremlj.png') no-repeat center center;
        background-size: cover;
        z-index: 9998;
        display: none;
        opacity: 0;
        filter: blur(10px);
        transition: opacity 0.8s ease, filter 0.8s ease;
        cursor: pointer;
    }

    #kremlj-screen.visible {
        display: block;
        opacity: 1;
        filter: blur(0px);
    }

    .enter-text {
        position: absolute;
        bottom: 15%;
        width: 100%;
        text-align: center;
        color: #fff;
        font-size: 14px;
        font-weight: 400;
        text-transform: uppercase;
        letter-spacing: 6px;
        text-shadow: 0 2px 10px rgba(0,0,0,0.5);
        animation: fadeInText 2s ease-in-out infinite alternate;
    }

    @keyframes fadeInText {
        from { opacity: 0.3; letter-spacing: 6px; }
        to { opacity: 1; letter-spacing: 8px; }
    }

    /* 3. GLAVNI SADRŽAJ */
    #main-content {
        display: none;
        opacity: 0;
        transition: opacity 0.8s ease;
    }

    header.ruska-zastava {
        height: 300px;
        background: url('download (10).jfif') center/cover no-repeat;
        display: flex; align-items: center; justify-content: center;
    }

    .overlay {
        background: rgba(0,0,0,0.65);
        padding: 2.5rem;
        border-radius: 4px;
        text-align: center;
        backdrop-filter: blur(5px);
        border: 1px solid rgba(255,255,255,0.1);
    }

    h1 { color: #fff; margin: 0; font-size: 28px; font-weight: 300; letter-spacing: 1px; }

    main { display: flex; min-height: calc(100vh - 300px); }

    nav { width: 300px; background: #fff; border-right: 1px solid #e0e4e8; padding: 2rem; }

    .nav-button {
        display: block; width: 100%; padding: 14px;
        margin-bottom: 10px;
        background: #ffffff;
        border: 1px solid #eee;
        color: #1f3a5f;
        font-weight: 600;
        text-align: left;
        cursor: pointer;
        transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
        font-size: 13px;
        text-transform: uppercase;
        letter-spacing: 1px;
    }

    .nav-button:hover { 
        background: var(--primary-blue); 
        color: #fff; 
        border-color: var(--primary-blue);
        box-shadow: 0 4px 12px rgba(31, 58, 95, 0.2);
    }

    section { flex: 1; padding: 3rem; }
    .card { background: #fff; padding: 3rem; border-radius: 4px; box-shadow: 0 10px 30px rgba(0,0,0,0.05); }
</style>
</head>

<body>

    <div id="loader-wrapper">
        <div class="loader-content">
            <div class="loading-text">Inicijalizacija sistema</div>
            <div class="progress-container">
                <div class="progress-bar"></div>
            </div>
        </div>
    </div>

    <div id="kremlj-screen" onclick="enterSite()">
        <div class="enter-text">Kliknite za ulaz</div>
    </div>

    <div id="main-content">
        <header class="ruska-zastava">
            <div class="overlay">
                <h1>VIRTUELNA AMBASADA RUSKE FEDERACIJE</h1>
            </div>
        </header>

        <main>
            <nav id="sidebar">
                <button class="nav-button" onclick="showSection('amb')">Ambasador</button>
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
                    <h2 style="font-weight: 300;">Dobrodošli</h2>
                    <p style="line-height: 1.6; color: #555;">Sistem je spreman. Odaberite željeni sektor iz navigacionog panela.</p>
                </div>
            </section>
        </main>
    </div>

<script>
    // EKSPERTSKO UPRAVLJANJE UČITAVANJEM
    window.addEventListener('load', function() {
        const loader = document.getElementById('loader-wrapper');
        const splash = document.getElementById('kremlj-screen');

        // Brza inicijalizacija nakon učitavanja svih resursa
        setTimeout(() => {
            loader.style.opacity = '0';
            setTimeout(() => {
                loader.style.display = 'none';
                splash.classList.add('visible');
            }, 600);
        }, 1200); // 1.2s je idealno vreme za vizuelnu progresiju bara
    });

    function enterSite() {
        const splash = document.getElementById('kremlj-screen');
        const main = document.getElementById('main-content');
        
        splash.style.opacity = '0';
        splash.style.filter = 'blur(20px)';
        
        setTimeout(() => {
            splash.style.display = 'none';
            main.style.display = 'block';
            setTimeout(() => main.style.opacity = '1', 50);
        }, 700);
    }

    const sections = {
        amb: `<div class="card"><h2>Kabinet ambasadora</h2><p>Pristup poverljivim podacima i zvanični raspored šefa misije.</p></div>`,
        dip: `<div class="card"><h2>Diplomatska kancelarija</h2><p>Koordinacija diplomatskih nota i protokola.</p></div>`,
        pol: `<div class="card"><h2>Političko odeljenje</h2><p>Analitički izveštaji i bilateralna saradnja.</p></div>`,
        eko: `<div class="card"><h2>Trgovinsko predstavništvo</h2><p>Ekonomski odnosi i podrška privrednicima.</p></div>`,
        konz: `<div class="card"><h2>Konzularno odeljenje</h2><p>Usluge državljanima i vizni režim.</p></div>`,
        odbr: `<div class="card"><h2>Izaslanik odbrane</h2><p>Vojno-diplomatski sektor.</p></div>`,
        kul: `<div class="card"><h2>Ruski dom</h2><p>Kulturna razmena i edukacija.</p></div>`,
        adm: `<div class="card"><h2>Administracija</h2><p>Tehničko upravljanje i logistika.</p></div>`
    };

    function showSection(key) {
        const container = document.getElementById("content");
        container.style.opacity = '0';
        setTimeout(() => {
            container.innerHTML = sections[key];
            container.style.opacity = '1';
        }, 300);
    }
</script>

</body>
</html>
