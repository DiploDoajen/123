<!DOCTYPE html>
<html lang="sr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Virtuelna ambasada Ruske Federacije</title>
<style>
    /* CSS ostaje isti kao u prethodnim verzijama, samo proverite putanje */
    body { font-family: sans-serif; margin: 0; background: #f4f6f8; }
    header.ruska-zastava { 
        height: 250px; 
        background: #1f3a5f; /* Fallback boja ako slika ne radi */
        background-image: url('download (10).jfif'); 
        background-size: cover;
        display: flex; align-items: center; justify-content: center; color: white;
    }
    .overlay { background: rgba(0,0,0,0.6); padding: 20px; border-radius: 10px; text-align: center; }
    main { display: flex; flex-wrap: wrap; }
    nav { width: 250px; background: white; padding: 20px; border-right: 1px solid #ddd; min-height: 100vh; }
    nav li { cursor: pointer; padding: 10px; list-style: none; color: #1f3a5f; }
    nav li:hover { background: #eee; }
    section { flex: 1; padding: 20px; }
    .card { background: white; padding: 20px; border-radius: 8px; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
    .img-ruski-dom { width: 250px; height: 180px; display: block; margin: 10px auto; object-fit: contain; }
    .img-izaslanik { width: 80px; height: 100px; display: block; margin: 10px auto; object-fit: contain; }
</style>
</head>
<body>

<header class="ruska-zastava">
    <div class="overlay">
        <h1>Virtuelna ambasada Ruske Federacije</h1>
        <p>Republika Srbija</p>
    </div>
</header>

<main>
    <nav>
        <ul>
            <li onclick="showSection('amb')">Kabinet ambasadora</li>
            <li onclick="showSection('odbr')">Izaslanik odbrane</li>
            <li onclick="showSection('kul')">Ruski dom</li>
        </ul>
    </nav>

    <section id="content">
        <div class="card">
            <h2>Dobrodošli</h2>
            <p>Kliknite na stavku iz menija da biste videli detalje.</p>
        </div>
    </section>
</main>

<script>
const sections = {
    amb: `
        <div class="card">
            <h2>Kabinet ambasadora</h2>
            <p>Nj. E. Aleksandar Bocan-Harčenko</p>
        </div>`,
    odbr: `
        <div class="card">
            <h2>Aparat Izaslanika odbrane</h2>
            <img src="izaslanik_odbrane.png" alt="Izaslanik" class="img-izaslanik">
            <p>General-major Gennady Mozhaev</p>
        </div>`,
    kul: `
        <div class="card">
            <h2>Ruski dom</h2>
            <img src="Ruski dom12345.png" alt="Ruski dom" class="img-ruski-dom">
            <p>Kraljice Natalije 33, Beograd</p>
        </div>`
};

function showSection(key) {
    const content = document.getElementById("content");
    if(sections[key]) {
        content.innerHTML = sections[key];
    }
}
</script>
</body>
</html>
