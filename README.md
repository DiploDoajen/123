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

/* HEADER */
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

/* LAYOUT */
main { display: flex; }

nav {
    width: 300px;
    background: #ffffff;
    border-right: 1px solid #ddd;
    padding: 20px;
    height: calc(100vh - 320px);
    overflow-y: auto;
}

nav h3 { color: #1f3a5f; }
nav ul { list-style: none; padding-left: 0; }
nav li { margin: 12px 0; cursor: pointer; color: #1f3a5f; font-weight: 500; }
nav li:hover { text-decoration: underline; }

section { flex: 1; padding: 30px; overflow-y: auto; }

.card {
    background: #ffffff;
    padding: 25px;
    margin-bottom: 20px;
    border-radius: 6px;
    box-shadow: 0 2px 6px rgba(0,0,0,0.08);
}

.card h2 { color: #1f3a5f; }

/* DEFINISANE DIMENZIJE ZA SLIKE */

/* 1. Ruski dom - Veća slika */
.img-ruski-dom {
    display: block;
    width: 100px;   /* Širina */
    height: 100px;  /* Visina */
    margin: 20px auto;
    object-fit: contain; /* Čuva proporcije bez razvlačenja */
}

/* 2. Izaslanik odbrane - Manja slika */
.img-izaslanik {
    display: block;
    width: 80px;    /* Širina */
    height: 100px;  /* Visina */
    margin: 15px auto;
    object-fit: contain;
}
</style>
</head>

<body>

<header class="ruska-zastava">
    <div class="overlay">
        <h1>Virtuelna ambasada Ruske Federacije u Republici Srbiji</h1>
        <p>Zvanična struktura i unutrašnja
