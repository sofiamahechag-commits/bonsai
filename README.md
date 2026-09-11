```html
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>盆栽 | El arte del Bonsái</title>

<style>

@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@500;600;700&family=Klee+One:wght@400;600&display=swap');

:root{
    --ink:#20221d;
    --ink-soft:#4c5148;
    --paper:#f3ead9;
    --paper-light:#fbf7ee;
    --sage:#667762;
    --sage-dark:#3f5142;
    --terracotta:#a94a38;
    --red:#8f2529;
    --gold:#b78b4a;
    --line:rgba(32,34,29,.15);
    --shadow:0 24px 70px rgba(45,34,20,.18);
}

*{
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    margin:0;
    color:var(--ink);
    background:
        radial-gradient(circle at 15% 10%,rgba(183,139,74,.10),transparent 22%),
        radial-gradient(circle at 85% 55%,rgba(102,119,98,.10),transparent 25%),
        var(--paper);
    font-family:Arial, Helvetica, sans-serif;
    overflow-x:hidden;
}

body::before{
    content:"";
    position:fixed;
    inset:0;
    pointer-events:none;
    z-index:50;
    opacity:.20;
    background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='160' height='160'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.8' numOctaves='3'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.08'/%3E%3C/svg%3E");
}

.topline{
    height:5px;
    background:linear-gradient(
        90deg,
        var(--red),
        var(--terracotta),
        var(--gold),
        var(--sage)
    );
}

/* =========================
   NAVBAR
========================= */

header{
    position:sticky;
    top:0;
    z-index:40;
    background:rgba(243,234,217,.90);
    backdrop-filter:blur(16px);
    border-bottom:1px solid var(--line);
}

nav{
    max-width:1180px;
    margin:auto;
    padding:12px 22px;
    min-height:74px;
    display:flex;
    align-items:center;
    justify-content:space-between;
}

.brand{
    display:flex;
    align-items:center;
    gap:12px;
    color:var(--ink);
    text-decoration:none;
}

.seal{
    width:43px;
    height:43px;
    border:2px solid var(--red);
    color:var(--red);
    display:grid;
    place-items:center;
    font-family:"Klee One", cursive;
    font-size:19px;
    transform:rotate(-4deg);
}

.brand strong{
    font-family:"Klee One", cursive;
    font-size:22px;
    display:block;
    line-height:1;
}

.brand small{
    font-size:10px;
    letter-spacing:.18em;
    text-transform:uppercase;
    color:var(--ink-soft);
}

nav a:not(.brand){
    text-decoration:none;
    color:var(--ink);
    font-weight:700;
    font-size:14px;
}

nav a:not(.brand):hover{
    color:var(--red);
}

/* =========================
   HERO
========================= */

.hero{
    max-width:1180px;
    margin:auto;
    padding:68px 22px 54px;
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:52px;
    align-items:center;
}

.kicker{
    font-size:11px;
    text-transform:uppercase;
    letter-spacing:.25em;
    color:var(--red);
    font-weight:700;
}

h1,h2,h3{
    font-family:"Cormorant Garamond", Georgia, serif;
}

h1{
    font-size:clamp(58px,8vw,100px);
    line-height:.86;
    margin:14px 0 24px;
    font-weight:600;
    letter-spacing:-.045em;
}

h1 span{
    color:var(--terracotta);
}

.hero-copy p{
    max-width:570px;
    color:var(--ink-soft);
    font-family:"Cormorant Garamond", Georgia, serif;
    font-size:22px;
    line-height:1.42;
    margin:0 0 27px;
}

.cta{
    display:inline-flex;
    gap:10px;
    align-items:center;
    padding:13px 19px;
    border-radius:999px;
    background:var(--ink);
    color:white;
    text-decoration:none;
    font-size:14px;
    font-weight:700;
    transition:.25s;
}

.cta:hover{
    background:var(--red);
    transform:translateY(-3px);
}

/* =========================
   IMAGEN PRINCIPAL
========================= */

.hero-photo{
    height:490px;
    border-radius:28px;
    overflow:hidden;
    position:relative;
    box-shadow:var(--shadow);
    background:#ddd;
}

.hero-photo img{
    width:100%;
    height:100%;
    object-fit:cover;
    transition:transform 1.2s ease;
}

.hero-photo:hover img{
    transform:scale(1.045);
}

.hero-photo::after{
    content:"";
    position:absolute;
    inset:0;
    background:linear-gradient(
        180deg,
        transparent 50%,
        rgba(25,24,19,.48)
    );
}

.photo-caption{
    position:absolute;
    z-index:2;
    left:22px;
    bottom:20px;
    color:white;
    font-family:"Klee One", cursive;
    font-size:18px;
}

.ink-stroke{
    width:90px;
    height:5px;
    background:var(--terracotta);
    margin-top:10px;
    transform:rotate(-2deg);
    border-radius:50%;
}

/* =========================
   SECCIONES
========================= */

section{
    max-width:1180px;
    margin:auto;
    padding:65px 22px;
}

.section-title{
    display:flex;
    justify-content:space-between;
    align-items:end;
    gap:30px;
    margin-bottom:28px;
}

.section-title h2{
    font-size:58px;
    line-height:.9;
    margin:6px 0 0;
}

.section-title p{
    max-width:510px;
    color:var(--ink-soft);
    margin:0;
    font-size:14px;
    line-height:1.7;
}

/* =========================
   TARJETAS
========================= */

.styles{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:18px;
}

.card{
    position:relative;
    overflow:hidden;
    cursor:pointer;
    background:rgba(251,247,238,.83);
    border:1px solid var(--line);
    border-radius:19px;
    transition:.28s ease;
    box-shadow:0 7px 25px rgba(45,34,20,.05);
}

.card:hover{
    transform:translateY(-7px);
    box-shadow:var(--shadow);
    border-color:rgba(143,37,41,.28);
}

.card-img{
    height:255px;
    overflow:hidden;
    position:relative;
    background:#d9d0c0;
}

.card-img img{
    width:100%;
    height:100%;
    object-fit:cover;
    transition:transform .7s ease;
}

.card:hover .card-img img{
    transform:scale(1.07);
}

.card-img::after{
    content:"Ver ficha →";
    position:absolute;
    right:13px;
    bottom:13px;
    padding:6px 10px;
    border-radius:999px;
    background:rgba(255,250,240,.9);
    font-size:11px;
    font-weight:700;
    color:var(--ink);
    opacity:0;
    transform:translateY(7px);
    transition:.25s;
}

.card:hover .card-img::after{
    opacity:1;
    transform:none;
}

.card-body{
    padding:18px 19px 20px;
}

.jp{
    font-family:"Klee One", cursive;
    color:var(--red);
    font-size:15px;
}

.card h3{
    font-size:32px;
    margin:0 0 8px;
}

/* =========================
   DESCRIPCIÓN DE TARJETAS
   LETRA CLARA Y ESPACIADA
========================= */

.card p{
    margin:0;
    color:#4a4a46;
    font-family:Arial, Helvetica, sans-serif;
    font-size:15px;
    font-weight:400;
    line-height:1.6;
    letter-spacing:0.4px;
}

.pill{
    display:inline-block;
    margin-top:13px;
    border:1px solid var(--line);
    border-radius:999px;
    padding:4px 9px;
    font-size:10px;
    color:var(--ink-soft);
}

/* =========================
   ANIMACIÓN DE HOJAS
========================= */

.leaves{
    position:fixed;
    inset:0;
    pointer-events:none;
    z-index:5;
    overflow:hidden;
}

.leaf{
    position:absolute;
    width:13px;
    height:7px;
    border-radius:100% 0 100% 0;
    background:rgba(102,119,98,.38);
    animation:fall linear infinite;
}

.leaf:nth-child(1){
    left:8%;
    animation-duration:13s;
    animation-delay:-4s;
}

.leaf:nth-child(2){
    left:27%;
    animation-duration:17s;
    animation-delay:-11s;
}

.leaf:nth-child(3){
    left:51%;
    animation-duration:14s;
    animation-delay:-7s;
}

.leaf:nth-child(4){
    left:76%;
    animation-duration:19s;
    animation-delay:-14s;
}

.leaf:nth-child(5){
    left:91%;
    animation-duration:15s;
    animation-delay:-5s;
}

@keyframes fall{

    0%{
        top:-30px;
        transform:translateX(0) rotate(0);
    }

    50%{
        transform:translateX(65px) rotate(180deg);
    }

    100%{
        top:105vh;
        transform:translateX(-35px) rotate(360deg);
    }
}

/* =========================
   VENTANA DE DETALLE
========================= */

.modal{
    display:none;
    position:fixed;
    inset:0;
    z-index:100;
    background:rgba(20,20,17,.66);
    backdrop-filter:blur(8px);
    padding:18px;
    overflow:auto;
}

.modal.open{
    display:grid;
    place-items:center;
}

.panel{
    width:min(1080px,100%);
    max-height:92vh;
    overflow:hidden;
    border-radius:26px;
    background:var(--paper-light);
    box-shadow:0 40px 110px rgba(0,0,0,.35);
    animation:panelIn .35s ease;
}

@keyframes panelIn{

    from{
        opacity:0;
        transform:translateY(18px) scale(.98);
    }

    to{
        opacity:1;
        transform:none;
    }
}

.panel-grid{
    display:grid;
    grid-template-columns:1.05fr .95fr;
    min-height:620px;
}

.panel-photo{
    position:relative;
    background:#d7cfbf;
    min-height:620px;
}

.panel-photo img{
    width:100%;
    height:100%;
    object-fit:cover;
    display:block;
}

.panel-copy{
    padding:48px 43px;
    overflow:auto;
}

.close{
    position:absolute;
    z-index:3;
    right:16px;
    top:16px;
    width:42px;
    height:42px;
    border:0;
    border-radius:50%;
    background:rgba(32,34,29,.9);
    color:white;
    font-size:22px;
    cursor:pointer;
}

.close:hover{
    background:var(--red);
}

.panel-copy .jp{
    font-size:18px;
}

.panel-copy h2{
    font-size:68px;
    line-height:.86;
    margin:5px 0 3px;
}

.pron{
    font-family:"Klee One", cursive;
    color:var(--ink-soft);
    font-size:13px;
}

/* =========================
   DESCRIPCIÓN DE LA FICHA
   LETRA CLARA Y ESPACIADA
========================= */

.description{
    font-family:Arial, Helvetica, sans-serif;
    font-size:15px;
    font-weight:400;
    line-height:1.7;
    letter-spacing:0.4px;
    color:#4a4a46;
    margin:22px 0;
}

/* =========================
   DATOS
========================= */

.facts{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:10px;
}

.fact{
    padding:13px;
    border:1px solid var(--line);
    border-radius:13px;
    background:rgba(243,234,217,.55);
}

.fact b{
    display:block;
    color:var(--red);
    font-size:10px;
    letter-spacing:.12em;
    text-transform:uppercase;
    margin-bottom:3px;
}

/* =========================
   BOTONES
========================= */

.navbuttons{
    display:flex;
    justify-content:space-between;
    gap:10px;
    margin-top:28px;
}

.navbuttons button{
    border:1px solid var(--line);
    background:transparent;
    padding:10px 14px;
    border-radius:999px;
    cursor:pointer;
    font-weight:700;
    color:var(--ink);
}

.navbuttons button:hover{
    border-color:var(--red);
    color:var(--red);
}

.source{
    font-size:10px;
    color:#81796e;
    margin-top:18px;
}

/* =========================
   FOOTER
========================= */

footer{
    border-top:1px solid var(--line);
    text-align:center;
    padding:35px 20px 55px;
    color:var(--ink-soft);
    fon
```
