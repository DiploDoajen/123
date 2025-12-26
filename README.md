<!DOCTYPE html>
<html lang="sr">
<head>
<meta charset="UTF-8">
<title>Virtuelna ambasada Ruske Federacije u Republici Srbiji</title>

<style>
/* STIL ZA LOADING SCREEN */
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
    z-index: 9999;
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

/* STIL ZA KREMLJ EKRAN (PREKO CELOG EKRANA) */
#kremlj-screen {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: url('kremlj.png'); /* Ovde ide tvoja slika */
    background-size: cover;
    background-position: center;
    z-index: 9998;
    display: none; /* Inicijalno sakriveno dok se učitava */
    cursor: pointer;
}

#kremlj-screen .enter-text {
    position: absolute;
    bottom: 10%;
    width: 100%;
    text-align: center;
    color: white;
    font-size: 24px;
    text-shadow: 2px 2px 10px rgba(0,0,0,0.8);
    font-weight: bold;
    animation: pulse 2s infinite;
}

@keyframes pulse {
    0% { opacity: 0.5; }
    50% { opacity: 1; }
    100% { opacity: 0.5; }
}

/* OSNOVNI STILOVI SAJTA */
body {
    font-family: "Segoe UI", Arial, sans-serif;
    margin: 0;
    background: #f4f6f8;
    color: #1a1a1a;
    display: none; /* Sakrivamo glavni sadržaj dok se ne klikne na sliku */
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
    background: rgba(0,0,0,0.55);
    padding: 30px 50px;
    border-radius: 10px;
    text-align: center;
}

header.ruska-zastava h1 { margin: 0; font-size: 32px; color: #ffffff; }
header.ruska-zastava p { margin-top: 15px; font-size: 16px; color: #ffffff; }

main { display: flex; }

nav {
    width: 300px;
    background: #ffffff;
    border-right: 1px solid #ddd;
    padding: 20px;
    height: calc(100vh - 320px);
    overflow-y: auto;
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
    transition: all 0.3s ease;
}

.nav-button:hover {
    background-color: #1f3a5f;
    color: #ffffff;
    transform: translateX(5px);
}

section { flex: 1; padding: 30px; }
.card { background: #ffffff; padding: 25px; border-radius: 6px; box-shadow: 0 2px 6px rgba(0,0,0,0.08); }
</style>
</head>

<body>

<div id="loader-wrapper">
    <div class="spinner"></div>
    <p style="margin-top: 20px; color: #1f3a5f; font-weight: bold;">Učitavanje...</p>
</div>

<div id="kremlj-screen" onclick="enterSite()">
    <div class="enter-text">KLIKNITE ZA ULAZAK</div>
</div>

<div id="main-content">
    <header class="ruska-zastava">
        <div class="overlay">
            <h1>Virtuelna ambasada Ruske Federacije u Republici Srbiji</h1>
            <p>Zvanična struktura i unutrašnja organizacija diplomatske misije</p>
        </div>
    </header>

    <main>
        <nav>
            <h3>Prostorije ambasade</h3>
            <ul>
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
                <p>Ova virtuelna simulacija prikazuje unutrašnju organizaciju Ambasade Ruske Federacije u Republici Srbiji.</p>
            </div>
        </section>
    </main>
</div>

<script>
// Funkcija koja se pokreće čim se stranica učita
window.onload = function() {
    setTimeout(function() {
        // Sakrij loader
        document.getElementById('loader-wrapper').style.display = 'none';
        // Prikaži Kremlj sliku
        document.getElementById('kremlj-screen').style.display = 'block';
    }, 1500); // 1.5 sekundi
};

// Funkcija za ulazak na sajt nakon klika na sliku
function enterSite() {
    document.getElementById('kremlj-screen').style.display = 'none';
    document.body.style.display = 'block';
}

const sections = {
    amb: `<div class="card"><h2>Kabinet ambasadora</h2><p>Šef misije: Nj. E. Aleksandar Bocan-Harčenko.</p></div>`,
    dip: `<div class="card"><h2>Diplomatska kancelarija</h2><p>Pomaže ambasadoru u obavljanju zadataka.</p></div>`,
    pol: `<div class="card"><h2>Političko odeljenje</h2><p>Prati politiku Republike Srbije.</p></div>`,
    eko: `<div class="card"><h2>Trgovinsko predstavništvo</h2><p>Katićeva 8–10, Beograd.</p></div>`,
    konz: `<div class="card"><h2>Konzularno odeljenje</h2><p>Deligradska 32, Beograd.</p></div>`,
    odbr: `<div class="card"><h2>Izaslanik odbrane</h2><p>General-major Gennady Mozhaev.</p></div>`,
    kul: `<div class="card"><h2>Ruski dom</h2><p>Kraljice Natalije 33, Beograd.</p></div>`,
    adm: `<div class="card"><h2>Administrativno-tehnička služba</h2><p>Logistička podrška.</p></div>`
};

function showSection(key) {
    document.getElementById("content").innerHTML = sections[key];
}
</script>

</body>
</html>
