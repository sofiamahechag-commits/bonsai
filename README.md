<h1>
```html
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>盆栽 | El arte del Bonsái</title>

<style>

@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@500;600;700&family=DM+Sans:wght@400;500;600;700&family=Klee+One:wght@400;600&display=swap');

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
    font-family:"DM Sans",Arial,sans-serif;
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

/* NAVBAR */

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
    font-family:"Klee One";
    font-size:19px;
    transform:rotate(-4deg);
}

.brand strong{
    font-family:"Klee One";
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

/* HERO */

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
    font-family:"Cormorant Garamond",Georgia,serif;
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
    font-family:"Cormorant Garamond",Georgia,serif;
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

/* IMAGEN PRINCIPAL */

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
    font-family:"Klee One";
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

/* SECCIONES */

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

/* TARJETAS */

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
    font-family:"Klee One";
    color:var(--red);
    font-size:15px;
}

.card h3{
    font-size:32px;
    margin:0 0 5px;
}

/* ==================================================
   CAMBIO SOLICITADO:
   TIPOGRAFÍA DE LAS DESCRIPCIONES
   ================================================== */

.card p{
    margin:0;
    color:#5d5a53;
    font-family:"DM Sans",Arial,sans-serif;
    font-size:14px;
    font-weight:400;
    line-height:1.65;
}

/* ETIQUETA */

.pill{
    display:inline-block;
    margin-top:13px;
    border:1px solid var(--line);
    border-radius:999px;
    padding:4px 9px;
    font-size:10px;
    color:var(--ink-soft);
}

/* ANIMACIÓN DE HOJAS */

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

/* VENTANA DE DETALLE */

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
    font-family:"Klee One";
    color:var(--ink-soft);
    font-size:13px;
}

/* ==================================================
   CAMBIO SOLICITADO:
   DESCRIPCIÓN DENTRO DE LA FICHA
   ================================================== */

.description{
    font-family:"DM Sans",Arial,sans-serif;
    font-size:15px;
    font-weight:400;
    line-height:1.75;
    color:#55534d;
    margin:22px 0;
}

/* DATOS */

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

/* BOTONES */

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

/* FOOTER */

footer{
    border-top:1px solid var(--line);
    text-align:center;
    padding:35px 20px 55px;
    color:var(--ink-soft);
    font-size:12px;
}

/* TABLET */

@media(max-width:900px){

    .hero{
        grid-template-columns:1fr;
    }

    .hero-photo{
        height:400px;
    }

    .styles{
        grid-template-columns:repeat(2,1fr);
    }

    .panel-grid{
        grid-template-columns:1fr;
    }

    .panel-photo{
        height:380px;
        min-height:0;
    }

    .panel-copy{
        max-height:420px;
    }
}

/* CELULAR */

@media(max-width:600px){

    nav{
        min-height:65px;
    }

    nav>a:not(.brand){
        display:none;
    }

    .hero{
        padding-top:50px;
    }

    h1{
        font-size:62px;
    }

    .hero-copy p{
        font-size:19px;
    }

    .hero-photo{
        height:330px;
    }

    section{
        padding:48px 18px;
    }

    .section-title{
        display:block;
    }

    .section-title h2{
        font-size:47px;
    }

    .section-title p{
        margin-top:15px;
    }

    .styles{
        grid-template-columns:1fr;
    }

    .card-img{
        height:260px;
    }

    .panel{
        border-radius:18px;
    }

    .panel-photo{
        height:270px;
    }

    .panel-copy{
        padding:34px 23px;
        max-height:none;
    }

    .panel-copy h2{
        font-size:51px;
    }

    .description{
        font-size:14px;
        line-height:1.7;
    }

    .facts{
        grid-template-columns:1fr;
    }
}

</style>
</head>


<body>

<div class="topline"></div>


<!-- ANIMACIÓN DE HOJAS -->

<div class="leaves">

    <i class="leaf"></i>
    <i class="leaf"></i>
    <i class="leaf"></i>
    <i class="leaf"></i>
    <i class="leaf"></i>

</div>


<!-- MENÚ -->

<header>

<nav>

    <a class="brand" href="#inicio">

        <div class="seal">
            盆栽
        </div>

        <div>

            <strong>
                Camino del Bonsái
            </strong>

            <small>
                Catálogo educativo
            </small>

        </div>

    </a>


    <a href="#estilos">
        Explorar estilos ↓
    </a>

</nav>

</header>


<main id="inicio">


<!-- HERO -->

<section class="hero">

    <div class="hero-copy">

        <div class="kicker">
            盆栽 · Arte vivo japonés
        </div>


        <h1>
            Una forma de
            <span>contar</span>
            historias.
        </h1>


        <p>

            Explora los estilos del bonsái y descubre cómo
            el tronco, las ramas y el paisaje convierten
            un pequeño árbol en una obra de arte.

        </p>


        <a class="cta" href="#estilos">

            Descubrir los estilos →

        </a>

    </div>


    <!-- IMAGEN PRINCIPAL -->

    <div class="hero-photo">

        <img
            src="https://commons.wikimedia.org/wiki/Special:Redirect/file/Pescia%2C%20museo%20del%20bonsai%2C%20pinus%20halepensisa%2C%20stile%20chokkan%20%28eretto%20formale%29%2C%20da%20italia%2C%20circa%2060%20anni.jpg"
            alt="Bonsái estilo Chokkan"
        >

        <div class="photo-caption">

            直幹 · Chokkan

            <div class="ink-stroke"></div>

        </div>

    </div>

</section>



<!-- CATÁLOGO -->

<section id="estilos">

    <div class="section-title">

        <div>

            <div class="kicker">
                El catálogo
            </div>

            <h2>
                Formas del bonsái
            </h2>

        </div>


        <p>

            Haz clic en cualquier tarjeta para abrir
            una ficha visual con una fotografía real,
            características principales y una explicación
            sencilla del estilo.

        </p>

    </div>


    <div class="styles" id="styles"></div>


    <div class="note">

        Consejo: las fotografías se muestran como
        referencias educativas.

    </div>

</section>

</main>



<!-- VENTANA DE DETALLE -->

<div class="modal" id="modal" aria-hidden="true">

    <div class="panel">

        <button
            class="close"
            id="close"
            aria-label="Cerrar"
        >
            ×
        </button>


        <div class="panel-grid">


            <div class="panel-photo">

                <img
                    id="modalImg"
                    src=""
                    alt=""
                >

            </div>


            <div class="panel-copy">


                <div
                    class="jp"
                    id="modalJp"
                ></div>


                <h2 id="modalName"></h2>


                <div
                    class="pron"
                    id="modalPron"
                ></div>


                <p
                    class="description"
                    id="modalDesc"
                ></p>


                <div class="facts">


                    <div class="fact">

                        <b>
                            Forma
                        </b>

                        <span id="modalForm"></span>

                    </div>


                    <div class="fact">

                        <b>
                            Dificultad
                        </b>

                        <span id="modalDifficulty"></span>

                    </div>


                    <div class="fact">

                        <b>
                            Tronco
                        </b>

                        <span id="modalTrunk"></span>

                    </div>


                    <div class="fact">

                        <b>
                            Composición
                        </b>

                        <span id="modalComposition"></span>

                    </div>


                </div>


                <div class="navbuttons">

                    <button id="prev">
                        ← Anterior
                    </button>

                    <button id="next">
                        Siguiente →
                    </button>

                </div>


                <div
                    class="source"
                    id="modalSource"
                ></div>


            </div>

        </div>

    </div>

</div>



<footer>

    <div>
        盆栽 · Camino del Bonsái
    </div>

    <div>
        Catálogo educativo · Diseño inspirado
        en la estética japonesa tradicional
    </div>

</footer>



<script>

/* ==============================
   INFORMACIÓN DE LOS BONSÁIS
================================ */

const styles = [

{
    jp:"直幹",
    name:"Chokkan",
    pron:"cho-kan",
    form:"Vertical formal",
    difficulty:"Intermedio",
    trunk:"Recto y cónico",
    composition:"Equilibrada",

    desc:
    "El tronco crece de manera recta y vertical, siendo más ancho en la base y estrechándose hacia la parte superior. Su silueta transmite estabilidad, orden y equilibrio.",

    img:
    "https://commons.wikimedia.org/wiki/Special:Redirect/file/Pescia%2C%20museo%20del%20bonsai%2C%20pinus%20halepensisa%2C%20stile%20chokkan%20%28eretto%20formale%29%2C%20da%20italia%2C%20circa%2060%20anni.jpg",

    source:
    "Fotografía: Sailko · Wikimedia Commons"
},


{
    jp:"模様木",
    name:"Moyogi",
    pron:"mo-yo-gui",
    form:"Vertical informal",
    difficulty:"Intermedio",
    trunk:"Curvado y sinuoso",
    composition:"Asimétrica",

    desc:
    "El tronco asciende mediante curvas naturales. Aunque se mueve hacia distintos lados, el ápice vuelve a quedar sobre la base del árbol. Es uno de los estilos más populares.",

    img:
    "https://commons.wikimedia.org/wiki/Special:Redirect/file/Pescia%2C%20museo%20del%20bonsai%2C%20ficus%20retusa%2C%20stile%20moyogi%20%28eretto%20informale%29%2C%20dalla%20cina%2C%20circa%2050%20anni.jpg",

    source:
    "Fotografía: Sailko · Wikimedia Commons"
},


{
    jp:"斜幹",
    name:"Shakan",
    pron:"sha-kan",
    form:"Inclinado",
    difficulty:"Intermedio",
    trunk:"Inclinado",
    composition:"Direccional",

    desc:
    "El tronco se inclina claramente hacia un lado, como un árbol que ha crecido buscando luz o soportando la acción constante del viento. Las raíces ayudan a equilibrar la composición.",

    img:
    "https://commons.wikimedia.org/wiki/Special:Redirect/file/Pescia%2C%20museo%20del%20bonsai%2C%20acer%20buergerianum%2C%20stile%20shakan%20%28inclinato%29.jpg",

    source:
    "Fotografía: Sailko · Wikimedia Commons"
},


{
    jp:"懸崖",
    name:"Kengai",
    pron:"ken-gai",
    form:"Cascada",
    difficulty:"Avanzado",
    trunk:"Descendente",
    composition:"Vertical",

    desc:
    "Representa un árbol que crece sobre un acantilado. El tronco sale hacia arriba y después cae por debajo del borde de la maceta, creando una composición dramática.",

    img:
    "https://commons.wikimedia.org/wiki/Special:Redirect/file/Bonsai%20Juniperus%20procumbens.jpg",

    source:
    "Fotografía: Wikimedia Commons"
},


{
    jp:"吹流し",
    name:"Fukinagashi",
    pron:"fu-ki-na-ga-shi",
    form:"Barrido por el viento",
    difficulty:"Avanzado",
    trunk:"Inclinado y dramático",
    composition:"Unilateral",

    desc:
    "Todas las ramas se orientan principalmente hacia una misma dirección, dando la sensación de que fuertes vientos han moldeado el árbol durante años.",

    img:
    "https://commons.wikimedia.org/wiki/Special:Redirect/file/Sargent%20Juniper%20%28Juniperus%20chinesis%20var.%20sargentii%29%20%283501620217%29.jpg",

    source:
    "Fotografía: Wikimedia Commons"
},


{
    jp:"文人木",
    name:"Bunjin",
    pron:"bun-yin",
    form:"Literati",
    difficulty:"Avanzado",
    trunk:"Delgado y sinuoso",
    composition:"Minimalista",

    desc:
    "Es un estilo elegante y minimalista. El tronco es protagonista y tiene pocas ramas, dejando bastante espacio vacío para crear una sensación ligera y artística.",

    img:
    "https://commons.wikimedia.org/wiki/Special:Redirect/file/Bunjin.jpg",

    source:
    "Fotografía: Wikimedia Commons"
},


{
    jp:"寄せ植え",
    name:"Yose-ue",
    pron:"yo-se-u-e",
    form:"Bosque",
    difficulty:"Intermedio",
    trunk:"Múltiple",
    composition:"Paisaje natural",

    desc:
    "Varios árboles se plantan juntos para representar un pequeño bosque. Los ejemplares tienen diferentes alturas y posiciones para crear profundidad y naturalidad.",

    img:
    "https://commons.wikimedia.org/wiki/Special:Redirect/file/Bonsai%20Yose-ue.jpg",

    source:
    "Fotografía: Wikimedia Commons"
},


{
    jp:"石付き",
    name:"Ishitsuki",
    pron:"i-shi-tsu-ki",
    form:"Sobre roca",
    difficulty:"Avanzado",
    trunk:"Variable",
    composition:"Paisajística",

    desc:
    "El bonsái se integra con una roca y sus raíces se adaptan a ella. El conjunto busca representar un paisaje natural donde el árbol parece crecer entre las piedras.",

    img:
    "https://commons.wikimedia.org/wiki/Special:Redirect/file/Ficus%20microcarpa%20bonsai%20Kiev.jpg",

    source:
    "Fotografía: Wikimedia Commons"
},


{
    jp:"双幹",
    name:"Sokan",
    pron:"so-kan",
    form:"Doble tronco",
    difficulty:"Intermedio",
    trunk:"Dos troncos",
    composition:"Asimétrica",

    desc:
    "Dos troncos parten de una misma base y crecen juntos. Normalmente uno es más alto y dominante, mientras el segundo aporta equilibrio y profundidad.",

    img:
    "https://commons.wikimedia.org/wiki/Special:Redirect/file/Bonsa%C3%AF%20sokan%20de%20160%20ans%20dans%20l%27Arboretum%20de%20la%20Vall%C3%A9e-aux-Loups%20%28Chatenay-Malabry%29%20%2844017801604%29.jpg",

    source:
    "Fotografía: Wikimedia Commons"
}

];


/* ==============================
   CREAR TARJETAS
================================ */

const grid =
document.getElementById("styles");


grid.innerHTML =
styles.map((s,i)=>`

<article
    class="card"
    data-i="${i}"
    tabindex="0"
>

    <div class="card-img">

        <img
            src="${s.img}"
            alt="Bonsái estilo ${s.name}"
            loading="lazy"
        >

    </div>


    <div class="card-body">

        <div class="jp">
            ${s.jp}
        </div>


        <h3>
            ${s.name}
        </h3>


        <p>
            ${s.desc}
        </p>


        <span class="pill">
            ${s.form}
        </span>

    </div>

</article>

`).join("");


/* ==============================
   ABRIR FICHA
================================ */

const modal =
document.getElementById("modal");

let current=0;


function openModal(i){

    current=i;

    const s=styles[current];


    document.getElementById("modalImg").src=s.img;

    document.getElementById("modalImg").alt=
        "Bonsái estilo "+s.name;


    document.getElementById("modalJp")
        .textContent=s.jp;


    document.getElementById("modalName")
        .textContent=s.name;


    document.getElementById("modalPron")
        .textContent=
        "Pronunciación: "+s.pron;


    document.getElementById("modalDesc")
        .textContent=s.desc;


    document.getElementById("modalForm")
        .textContent=s.form;


    document.getElementById("modalDifficulty")
        .textContent=s.difficulty;


    document.getElementById("modalTrunk")
        .textContent=s.trunk;


    document.getElementById("modalComposition")
        .textContent=s.composition;


    document.getElementById("modalSource")
        .textContent=s.source;


    modal.classList.add("open");

    modal.setAttribute(
        "aria-hidden",
        "false"
    );

    document.body.style.overflow="hidden";
}


/* ==============================
   CERRAR
================================ */

function closeModal(){

    modal.classList.remove("open");

    modal.setAttribute(
        "aria-hidden",
        "true"
    );

    document.body.style.overflow="";
}


/* ==============================
   NAVEGACIÓN
================================ */

function go(step){

    openModal(
        (current+step+styles.length)
        %styles.length
    );

}


/* ==============================
   EVENTOS
================================ */

document
.querySelectorAll(".card")
.forEach(card=>{

    card.addEventListener(
        "click",
        ()=>{
            openModal(
                Number(card.dataset.i)
            );
        }
    );


    card.addEventListener(
        "keydown",
        e=>{

            if(
                e.key==="Enter" ||
                e.key===" "
            ){

                openModal(
                    Number(card.dataset.i)
                );

            }

        }
    );

});


document
.getElementById("close")
.onclick=closeModal;


document
.getElementById("prev")
.onclick=()=>{
    go(-1);
};


document
.getElementById("next")
.onclick=()=>{
    go(1);
};


modal.addEventListener(
    "click",
    e=>{

        if(e.target===modal){
            closeModal();
        }

    }
);


/* ==============================
   TECLADO
================================ */

document.addEventListener(
    "keydown",
    e=>{

        if(
            !modal.classList.contains("open")
        ){
            return;
        }


        if(e.key==="Escape"){
            closeModal();
        }


        if(e.key==="ArrowLeft"){
            go(-1);
        }


        if(e.key==="ArrowRight"){
            go(1);
        }

    }
);

</script>

</body>
</html>
```

</script>

</body>
</html>
```
</h1>
