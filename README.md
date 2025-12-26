<!DOCTYPE html>
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
}

/* HEADER – RUSKA ZASTAVA PREKO CELE POVRŠINE */
header.ruska-zastava {
    height: 320px;
    background-image: url('download (10).jfif');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
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

header.ruska-zastava h1 {
    margin: 0;
    font-size: 32px;
    color: #ffffff;
}

header.ruska-zastava p {
    margin-top: 15px;
    font-size: 16px;
    color: #ffffff;
}

/* LAYOUT */
main {
    display: flex;
}

/* NAVIGACIJA */
nav {
    width: 300px;
    background: #ffffff;
    border-right: 1px solid #ddd;
    padding: 20px;
    height: calc(100vh - 320px);
    overflow-y: auto;
}

nav h3 {
    color: #1f3a5f;
}

nav ul {
    list-style: none;
    padding-left: 0;
}

nav li {
    margin: 12px 0;
    cursor: pointer;
    color: #1f3a5f;
    font-weight: 500;
}

nav li:hover {
    text-decoration: underline;
}

/* SADRŽAJ */
section {
    flex: 1;
    padding: 30px;
    overflow-y: auto;
}

.card {
    background: #ffffff;
    padding: 25px;
    margin-bottom: 20px;
    border-radius: 6px;
    box-shadow: 0 2px 6px rgba(0,0,0,0.08);
}

.card h2 {
    color: #1f3a5f;
}

/* STIL ZA LOGO (ISTI ZA SVE KARTICE) */
.logo-centar {
    display: block;
    max-width: 250px;
    height: auto;
    margin: 20px auto;
    border-radius: 4px;
}
</style>
</head>

<body>

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
    <li onclick="showSection('amb')">Kabinet ambasadora</li>
    <li onclick="showSection('dip')">Diplomatska kancelarija</li>
    <li onclick="showSection('pol')">Političko odeljenje</li>
    <li onclick="showSection('eko')">Trgovinsko predstavništvo</li>
    <li onclick="showSection('konz')">Konzularno odeljenje</li>
    <li onclick="showSection('odbr')">Izaslanik odbrane</li>
    <li onclick="showSection('kul')">Ruski dom</li>
    <li onclick="showSection('adm')">Administrativno-tehnička služba</li>
</ul>
</nav>

<section id="content">
<div class="card">
<h2>Dobrodošli</h2>
<p>
Ova virtuelna simulacija prikazuje unutrašnju organizaciju Ambasade Ruske Federacije
u Republici Srbiji, sa tačnim institucionalnim opisima i hijerarhijom diplomatske misije.
</p>
</div>
</section>

</main>

<script>
const sections = {

amb: `
<div class="card">
<h2>Kabinet ambasadora</h2>
<p><strong>Šef misije:</strong> Nj. E. gospodin Aleksandar Bocan-Harčenko,
Izvanredni i Opunomoćeni Ambasador Ruske Federacije u Republici Srbiji.</p>
<p>
Ukazom Predsednika Ruske Federacije od 10. juna 2019. godine br. 256,
imenovan je za Izvanrednog i Opunomoćenog Ambasadora Ruske Federacije u Republici Srbiji.
</p>
</div>`,

dip: `
<div class="card">
<h2>Diplomatska kancelarija</h2>
<p>
Diplomatska kancelarija pomaže ambasadoru u obavljanju političkih,
protokolarnih i analitičkih zadataka, priprema izveštaje i održava
kontakte sa državnim institucijama Republike Srbije.
</p>
</div>`,

pol: `
<div class="card">
<h2>Političko odeljenje</h2>
<p>
Političko odeljenje prati unutrašnju i spoljnu politiku Republike Srbije,
izrađuje analitičke izveštaje i učestvuje u pripremi političkih konsultacija.
</p>
</div>`,

eko: `
<div class="card">
<h2>Trgovinsko predstavništvo Ruske Federacije</h2>
<p><strong>Adresa:</strong> Katićeva 8–10, Beograd</p>
<p><strong>Trgovinski predstavnik:</strong> gđa Irina Negrbetskaia</p>
<p>
Predstavlja trgovinsko-ekonomske interese Ruske Federacije
i podržava bilateralnu privrednu saradnju.
</p>
</div>`,

konz: `
<div class="card">
<h2>Konzularno odeljenje</h2>
<p><strong>Adresa:</strong> Deligradska 32, Beograd</p>
<p><strong>Šef:</strong> Savetnik Aleksandra Simonova</p>
<p>
Obavlja poslove zaštite prava i interesa državljana Ruske Federacije,
izdavanje viza i konzularne usluge.
</p>
</div>`,

odbr: `
<div class="card">
<h2>Aparat Izaslanika odbrane</h2>
<img src="izaslanik_odbrane.png" alt="Izaslanik odbrane" class="logo-centar">
<p><strong>Izaslanik odbrane:</strong> general-major Gennady Mozhaev</p>
<p>
Zvanično predstavništvo Ministarstva odbrane Ruske Federacije,
zaduženo za vojno-političku i vojno-tehničku saradnju.
</p>
</div>`,

kul: `
<div class="card">
<h2>Ruski centar za nauku i kulturu u Beogradu (Ruski dom)</h2>
<img src="Ruski dom12345.png" alt="Logo Ruski dom" class="logo-centar">
<p><strong>Adresa:</strong> Kraljice Natalije 33, Beograd</p>
<p><strong>Direktor:</strong> Jevgenij Baranov</p>
<p>
Najstariji Ruski dom u sistemu Rossotrudničestva,
osnovan 1933. godine.
</p>
</div>`,

adm: `
<div class="card">
<h2>Administrativno-tehnička služba</h2>
<p>
Obezbeđuje logističku, tehničku i administrativnu podršku
radu Ambasade Ruske Federacije.
</p>
</div>`
};

function showSection(key) {
    document.getElementById("content").innerHTML = sections[key];
}
</script>

</body>
</html>
