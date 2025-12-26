<!DOCTYPE html>
<html lang="sr">
<head>
<meta charset="UTF-8">
<title>Virtuelna ambasada RF u Republici Srbiji</title>

<style>
body {
    margin: 0;
    font-family: Arial, Helvetica, sans-serif;
    background: #f4f6f8;
}

header {
    height: 360px;
    background: linear-gradient(
        rgba(0,0,0,0.55),
        rgba(0,0,0,0.55)
    ),
    url("data:image/svg+xml;utf8,
    <svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 3 2'>
    <rect width='3' height='2' fill='%23fff'/>
    <rect y='0.66' width='3' height='0.66' fill='%23003f87'/>
    <rect y='1.32' width='3' height='0.66' fill='%23d52b1e'/>
    </svg>");
    background-size: cover;
    color: white;
    text-align: center;
    padding-top: 70px;
}

header h1 {
    font-size: 32px;
}

header p {
    margin-top: 15px;
}

main {
    display: flex;
    max-width: 1200px;
    margin: 30px auto;
    gap: 30px;
    padding: 0 20px;
}

nav {
    width: 280px;
    background: white;
    border-radius: 6px;
    padding: 20px;
}

nav h3 {
    color: #0b5ed7;
}

nav button {
    width: 100%;
    padding: 10px;
    margin-bottom: 8px;
    background: #0b5ed7;
    color: white;
    border: none;
    cursor: pointer;
    border-radius: 4px;
}

nav button:hover {
    background: #084298;
}

section {
    flex: 1;
    background: white;
    padding: 25px;
    border-radius: 6px;
}

.institution {
    display: none;
}

.institution.active {
    display: block;
}

.institution h2 {
    color: #0b5ed7;
}
</style>

<script>
function showSection(id) {
    const sections = document.querySelectorAll('.institution');
    sections.forEach(sec => sec.classList.remove('active'));
    document.getElementById(id).classList.add('active');
}
</script>

</head>

<body>

<header>
    <h1>Virtuelna ambasada Ruske Federacije u Republici Srbiji</h1>
    <p>Zvanična struktura i unutrašnja organizacija diplomatske misije</p>
</header>

<main>

<nav>
    <h3>Prostorije ambasade</h3>
    <button onclick="showSection('ambasador')">Kabinet ambasadora</button>
    <button onclick="showSection('politicko')">Političko odeljenje</button>
    <button onclick="showSection('ekonomsko')">Ekonomsko odeljenje</button>
    <button onclick="showSection('konzularno')">Konzularno odeljenje</button>
    <button onclick="showSection('vojni')">Vojni ataše</button>
    <button onclick="showSection('ruski-dom')">Ruski dom</button>
</nav>

<section>

<div id="ambasador" class="institution active">
    <h2>Kabinet ambasadora</h2>
    <p><strong>Titula:</strong> Izvanredni i opunomoćeni ambasador Ruske Federacije</p>
    <p>
        Ambasador predstavlja Rusku Federaciju u Republici Srbiji,
        rukovodi radom diplomatske misije i zastupa interese države
        u skladu sa Bečkom konvencijom o diplomatskim odnosima.
    </p>
</div>

<div id="politicko" class="institution">
    <h2>Političko odeljenje</h2>
    <p>
        Političko odeljenje prati unutrašnju i spoljnu politiku Republike Srbije,
        izrađuje političke analize i izveštaje za Ministarstvo spoljnih poslova RF.
    </p>
</div>

<div id="ekonomsko" class="institution">
    <h2>Ekonomsko odeljenje</h2>
    <p>
        Odeljenje razvija trgovinsku, investicionu i energetsku saradnju
        između Ruske Federacije i Republike Srbije.
    </p>
</div>

<div id="konzularno" class="institution">
    <h2>Konzularno odeljenje</h2>
    <p>
        Konzularno odeljenje pruža konzularnu zaštitu državljanima Ruske Federacije,
        izdaje vize i vrši notarske poslove.
    </p>
</div>

<div id="vojni" class="institution">
    <h2>Vojni ataše</h2>
    <p><strong>Institucija:</strong> Ministarstvo odbrane Ruske Federacije</p>
    <p>
        Vojni ataše prati vojno-političke prilike, razvija vojnu saradnju
        i predstavlja Oružane snage Ruske Federacije.
    </p>
</div>

<div id="ruski-dom" class="institution">
    <h2>Ruski dom u Beogradu</h2>
    <p><strong>Institucija:</strong> Rossotrudničestvo</p>
    <p>
        Ruski dom je kulturno-obrazovna institucija koja promoviše ruski jezik,
        kulturu, nauku i humanitarnu saradnju.
    </p>
</div>

</section>

</main>

</body>
</html>
