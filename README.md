<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#080808">

<title>Emir'in Mezuniyet Partisi 🎓</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:Arial, Helvetica, sans-serif;
    background:#080808;
    color:#fff;
    overflow-x:hidden;
}

/* ANA ALAN */
.hero{
    min-height:100svh;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:35px 18px;
    position:relative;
    overflow:hidden;

    background:
        radial-gradient(
            circle at 50% 0%,
            #3b300d 0%,
            #171205 25%,
            #080808 55%,
            #000 100%
        );
}

/* IŞIK EFEKTLERİ */
.hero::before{
    content:"";
    position:absolute;
    width:280px;
    height:280px;
    border-radius:50%;
    background:#d4af37;
    filter:blur(120px);
    opacity:.15;
    top:-100px;
    left:-100px;
}

.hero::after{
    content:"";
    position:absolute;
    width:250px;
    height:250px;
    border-radius:50%;
    background:#d4af37;
    filter:blur(120px);
    opacity:.10;
    bottom:-100px;
    right:-100px;
}

/* KART */
.card{
    width:100%;
    max-width:500px;
    position:relative;
    z-index:2;
}

/* KEPLİ EMOJI */
.cap{
    font-size:76px;
    display:inline-block;
    animation:float 3s ease-in-out infinite;
    filter:drop-shadow(0 10px 20px rgba(212,175,55,.2));
}

@keyframes float{

    0%,100%{
        transform:translateY(0) rotate(0deg);
    }

    50%{
        transform:translateY(-10px) rotate(-3deg);
    }
}

/* ÜST BAŞLIK */
.small{
    color:#d4af37;
    letter-spacing:4px;
    font-size:12px;
    font-weight:bold;
    margin-top:15px;
}

/* İSİM */
h1{
    font-family:Georgia, "Times New Roman", serif;
    font-size:52px;
    line-height:1.1;
    margin:15px 0 8px;

    background:
        linear-gradient(
            90deg,
            #ffffff,
            #d4af37,
            #fff2a8,
            #d4af37,
            #ffffff
        );

    -webkit-background-clip:text;
    background-clip:text;
    color:transparent;

    background-size:250% auto;
    animation:goldText 5s linear infinite;
}

@keyframes goldText{
    to{
        background-position:250% center;
    }
}

.subtitle{
    color:#ccc;
    font-size:16px;
    line-height:1.6;
    margin-bottom:25px;
}

/* AYRAÇ */
.divider{
    width:80px;
    height:2px;
    background:#d4af37;
    margin:20px auto;
    box-shadow:0 0 15px rgba(212,175,55,.5);
}

/* GERİ SAYIM */
.countdown-title{
    color:#aaa;
    font-size:12px;
    letter-spacing:2px;
    margin-bottom:10px;
}

.countdown{
    display:flex;
    justify-content:center;
    gap:8px;
    margin:10px 0 28px;
}

.time{
    width:68px;
    min-width:0;
    padding:12px 5px;

    background:
        linear-gradient(
            145deg,
            rgba(255,255,255,.07),
            rgba(255,255,255,.02)
        );

    border:1px solid rgba(212,175,55,.35);
    border-radius:14px;

    box-shadow:
        inset 0 0 20px rgba(212,175,55,.03),
        0 8px 25px rgba(0,0,0,.3);
}

.time b{
    display:block;
    color:#d4af37;
    font-size:24px;
    line-height:1.2;
}

.time small{
    color:#999;
    font-size:10px;
}

/* BİLGİ KUTULARI */
.info{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:10px;
    margin-top:10px;
}

.box{
    min-height:105px;
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:center;

    border:1px solid rgba(212,175,55,.3);

    background:
        linear-gradient(
            145deg,
            rgba(255,255,255,.055),
            rgba(255,255,255,.015)
        );

    border-radius:18px;
    padding:15px 8px;

    backdrop-filter:blur(10px);
}

.icon{
    font-size:27px;
    margin-bottom:8px;
}

.box strong{
    color:#d4af37;
    font-size:13px;
    margin-bottom:5px;
}

.box span{
    color:#ddd;
    font-size:13px;
    line-height:1.3;
}

/* KONUM BUTONU */
.map{
    display:inline-flex;
    align-items:center;
    justify-content:center;

    margin-top:20px;
    padding:14px 25px;

    border-radius:30px;

    background:#d4af37;
    color:#080808;

    text-decoration:none;
    font-size:14px;
    font-weight:bold;

    box-shadow:
        0 8px 25px rgba(212,175,55,.15);

    transition:.3s;
}

.map:active{
    transform:scale(.96);
}

/* MESAJ */
.message{
    margin-top:30px;
    color:#ccc;
    font-family:Georgia, serif;
    font-size:15px;
    line-height:1.8;
}

/* ALT YAZI */
.footer{
    margin-top:30px;
    padding-bottom:10px;

    color:#777;
    font-size:12px;
    line-height:1.7;
}

/* KONFETİ */
.confetti{
    position:fixed;

    width:7px;
    height:7px;

    top:-15px;

    z-index:20;

    pointer-events:none;

    animation:fall linear forwards;
}

@keyframes fall{

    0%{
        transform:
            translateY(0)
            rotate(0deg);
    }

    100%{
        transform:
            translateY(110vh)
            rotate(720deg);
    }
}

/* MOBİL */
@media(max-width:420px){

    .hero{
        padding:30px 14px;
    }

    h1{
        font-size:42px;
    }

    .cap{
        font-size:65px;
    }

    .small{
        font-size:11px;
        letter-spacing:3px;
    }

    .subtitle{
        font-size:15px;
    }

    .countdown{
        gap:6px;
    }

    .time{
        width:62px;
        padding:10px 4px;
    }

    .time b{
        font-size:21px;
    }

    .info{
        gap:8px;
    }

    .box{
        min-height:100px;
    }
}

@media(max-width:350px){

    h1{
        font-size:36px;
    }

    .time{
        width:56px;
    }

    .time b{
        font-size:19px;
    }
}
</style>
</head>

<body>

<section class="hero">

<div class="card">

    <!-- KEPT -->
    <div class="cap">🎓</div>

    <div class="small">
        MEZUNİYET PARTİSİ
    </div>

    <!-- İSİM -->
    <h1>
        Emir Yılmaz
    </h1>

    <div class="divider"></div>

    <p class="subtitle">
        Bir dönemin sonu,<br>
        yepyeni bir başlangıç! ✨
    </p>


    <!-- GERİ SAYIM BAŞLIK -->
    <div class="countdown-title">
        BÜYÜK GÜNE KALAN SÜRE
    </div>


    <!-- GERİ SAYIM -->
    <div class="countdown">

        <div class="time">
            <b id="days">00</b>
            <small>GÜN</small>
        </div>

        <div class="time">
            <b id="hours">00</b>
            <small>SAAT</small>
        </div>

        <div class="time">
            <b id="minutes">00</b>
            <small>DAKİKA</small>
        </div>

        <div class="time">
            <b id="seconds">00</b>
            <small>SANİYE</small>
        </div>

    </div>


    <!-- ETKİNLİK BİLGİLERİ -->
    <div class="info">

        <div class="box">

            <div class="icon">
                📅
            </div>

            <strong>
                TARİH
            </strong>

            <span>
                20 Haziran 2027
            </span>

        </div>


        <div class="box">

            <div class="icon">
                ⏰
            </div>

            <strong>
                SAAT
            </strong>

            <span>
                19:00
            </span>

        </div>


        <div class="box">

            <div class="icon">
                📍
            </div>

            <strong>
                MEKÂN
            </strong>

            <span>
                Ordu Garden Davet
            </span>

        </div>


        <div class="box">

            <div class="icon">
                👔
            </div>

            <strong>
                KIYAFET
            </strong>

            <span>
                Şık & Rahat
            </span>

        </div>

    </div>


    <!-- HARİTA -->
    <a
        class="map"
        href="https://www.google.com/maps/search/?api=1&query=Ordu+Garden+Davet"
        target="_blank"
        rel="noopener"
    >
        📍 Konumu Gör
    </a>


    <!-- DAVET MESAJI -->
    <p class="message">

        Yıllarca süren emeğin ardından
        bu özel günü birlikte kutlamak
        için seni de mezuniyet partime
        bekliyorum. 🎓✨

        <br><br>

        Bu güzel gecede birlikte eğlenelim,
        fotoğraflar çekilelim ve unutulmaz
        anılar biriktirelim! 🥂

    </p>


    <!-- FOOTER -->
    <div class="footer">

        🎓 Emir'in Mezuniyet Partisi

        <br>

        Seni aramızda görmek dileğiyle ❤️

    </div>

</div>

</section>


<script>

/* =====================================
   GERİ SAYIM
   ===================================== */

/*
   BURADAN TARİHİ DEĞİŞTİREBİLİRSİN.

   Örnek:
   20 Haziran 2027 - 19:00
*/

const targetDate =
    new Date("June 20, 2027 19:00:00").getTime();


function countdown(){

    const now =
        new Date().getTime();

    const distance =
        targetDate - now;


    /* TARİH GEÇTİYSE */

    if(distance <= 0){

        document.getElementById("days").innerHTML = "00";

        document.getElementById("hours").innerHTML = "00";

        document.getElementById("minutes").innerHTML = "00";

        document.getElementById("seconds").innerHTML = "00";

        return;
    }


    /* HESAPLAMA */

    const days =
        Math.floor(
            distance /
            (1000 * 60 * 60 * 24)
        );


    const hours =
        Math.floor(
            (distance %
            (1000 * 60 * 60 * 24))
            /
            (1000 * 60 * 60)
        );


    const minutes =
        Math.floor(
            (distance %
            (1000 * 60 * 60))
            /
            (1000 * 60)
        );


    const seconds =
        Math.floor(
            (distance %
            (1000 * 60))
            /
            1000
        );


    /* EKRANA YAZDIR */

    document.getElementById("days").innerHTML =
        String(days).padStart(2,"0");


    document.getElementById("hours").innerHTML =
        String(hours).padStart(2,"0");


    document.getElementById("minutes").innerHTML =
        String(minutes).padStart(2,"0");


    document.getElementById("seconds").innerHTML =
        String(seconds).padStart(2,"0");

}


/* HER SANİYE GÜNCELLE */

setInterval(
    countdown,
    1000
);

countdown();



/* =====================================
   KONFETİ
   ===================================== */

function createConfetti(){

    const confetti =
        document.createElement("div");


    confetti.className =
        "confetti";


    /* RASTGELE KONUM */

    confetti.style.left =
        Math.random() * 100 + "vw";


    /* ALTIN / BEYAZ TONLARI */

    const colors = [

        "#d4af37",
        "#ffffff",
        "#f5d76e",
        "#b8860b"

    ];


    confetti.style.background =
        colors[
            Math.floor(
                Math.random() *
                colors.length
            )
        ];


    /* RASTGELE HIZ */

    confetti.style.animationDuration =
        (Math.random() * 3 + 3) + "s";


    /* RASTGELE ŞEFFAFLIK */

    confetti.style.opacity =
        Math.random() * .8 + .2;


    document.body.appendChild(
        confetti
    );


    /* TEMİZLE */

    setTimeout(
        () => {

            confetti.remove();

        },
        6000
    );

}


/* KONFETİ ÜRET */

setInterval(
    createConfetti,
    180
);

</script>

</body>
</html>
