<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Bebeğimizi Bekliyoruz 👶</title>

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
    background:#fff8f4;
    color:#4b3a35;
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
            #ffe7df 0%,
            #fff5ef 35%,
            #fffaf7 70%,
            #ffffff 100%
        );
}

/* IŞIK EFEKTLERİ */

.hero::before{
    content:"";

    position:absolute;

    width:280px;
    height:280px;

    border-radius:50%;

    background:#f5b8a8;

    filter:blur(100px);

    opacity:.25;

    top:-100px;
    left:-100px;
}

.hero::after{
    content:"";

    position:absolute;

    width:250px;
    height:250px;

    border-radius:50%;

    background:#e9c8a8;

    filter:blur(100px);

    opacity:.2;

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

/* BEBEK */

.baby{
    font-size:72px;

    display:inline-block;

    animation:
        float 3s ease-in-out infinite;

    filter:
        drop-shadow(
            0 8px 15px
            rgba(180,120,100,.2)
        );
}

@keyframes float{

    0%,100%{
        transform:translateY(0);
    }

    50%{
        transform:translateY(-10px);
    }
}

/* ÜST BAŞLIK */

.small{
    color:#c27d6d;

    letter-spacing:3px;

    font-size:11px;

    font-weight:bold;

    margin-top:15px;
}

/* ANA BAŞLIK */

h1{
    font-family:
        Georgia,
        "Times New Roman",
        serif;

    font-size:44px;

    line-height:1.2;

    margin:15px 0;

    color:#7a5147;
}

/* ALT BAŞLIK */

.subtitle{
    color:#806c66;

    font-family:Georgia, serif;

    font-size:16px;

    line-height:1.7;

    margin-bottom:25px;
}

/* AYRAÇ */

.divider{
    width:75px;

    height:2px;

    background:#d69a8b;

    margin:20px auto;
}

/* TARİH */

.date{
    display:inline-block;

    padding:10px 20px;

    border-radius:30px;

    background:#fff;

    border:1px solid #efd1c8;

    color:#a96859;

    font-size:14px;

    font-weight:bold;

    margin-bottom:20px;

    box-shadow:
        0 8px 25px
        rgba(150,100,80,.08);
}

/* GERİ SAYIM */

.countdown-title{
    color:#a4867e;

    font-size:10px;

    letter-spacing:2px;

    margin-bottom:10px;
}

.countdown{
    display:flex;

    justify-content:center;

    gap:7px;

    margin:10px 0 30px;
}

.time{
    width:68px;

    padding:12px 4px;

    background:
        rgba(255,255,255,.8);

    border:
        1px solid
        #efd1c8;

    border-radius:15px;

    box-shadow:
        0 8px 20px
        rgba(150,100,80,.06);
}

.time b{
    display:block;

    color:#c27d6d;

    font-size:23px;

    line-height:1.2;
}

.time small{
    color:#a38b84;

    font-size:9px;
}

/* BİLGİ KUTULARI */

.info{
    display:grid;

    grid-template-columns:
        1fr 1fr;

    gap:9px;

    margin-top:5px;
}

.box{
    min-height:105px;

    display:flex;

    flex-direction:column;

    align-items:center;

    justify-content:center;

    padding:14px 7px;

    background:
        rgba(255,255,255,.75);

    border:
        1px solid
        #efd1c8;

    border-radius:18px;

    box-shadow:
        0 8px 20px
        rgba(150,100,80,.05);
}

.icon{
    font-size:25px;

    margin-bottom:7px;
}

.box strong{
    color:#b87465;

    font-size:12px;

    margin-bottom:5px;
}

.box span{
    color:#806c66;

    font-size:13px;

    line-height:1.35;
}

/* MESAJ */

.message{
    margin-top:30px;

    color:#806c66;

    font-family:Georgia, serif;

    font-size:15px;

    line-height:1.9;
}

/* ALT */

.footer{
    margin-top:30px;

    padding-bottom:10px;

    color:#a99690;

    font-size:12px;

    line-height:1.8;
}

/* KALPLER */

.heart{
    position:fixed;

    top:-20px;

    z-index:20;

    pointer-events:none;

    font-size:18px;

    animation:
        fall linear forwards;
}

@keyframes fall{

    0%{
        transform:
            translateY(0)
            rotate(0deg);

        opacity:0;
    }

    15%{
        opacity:1;
    }

    100%{
        transform:
            translateY(110vh)
            rotate(25deg);

        opacity:0;
    }
}

/* MOBİL */

@media(max-width:420px){

    .hero{
        padding:30px 14px;
    }

    .baby{
        font-size:62px;
    }

    h1{
        font-size:38px;
    }

    .subtitle{
        font-size:14px;
    }

    .countdown{
        gap:5px;
    }

    .time{
        width:62px;

        padding:10px 3px;
    }

    .time b{
        font-size:20px;
    }

    .info{
        gap:7px;
    }
}

@media(max-width:350px){

    h1{
        font-size:33px;
    }

    .time{
        width:56px;
    }

    .time b{
        font-size:18px;
    }
}
</style>
</head>

<body>

<section class="hero">

<div class="card">

    <!-- BEBEK -->
    <div class="baby">
        👶
    </div>


    <!-- ÜST BAŞLIK -->
    <div class="small">
        BİR MUCİZEYİ BEKLİYORUZ
    </div>


    <!-- ANA BAŞLIK -->
    <h1>
        Bebeğimizi<br>
        Bekliyoruz
    </h1>


    <div class="divider"></div>


    <!-- ÇİFT -->
    <p class="subtitle">

        Elif & Emir

        <br><br>

        Hayatımızın en güzel
        sürprizine kavuşacağımız
        günü sabırsızlıkla bekliyoruz. 🤍

    </p>


    <!-- TAHMİNİ TARİH -->

    <div class="date">

        🍼 Tahmini Doğum:
        15 Aralık 2026

    </div>


    <!-- GERİ SAYIM -->

    <div class="countdown-title">
        BEBEĞİMİZİ KUCAĞIMIZA ALMAYA KALAN SÜRE
    </div>


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


    <!-- BİLGİLER -->

    <div class="info">


        <div class="box">

            <div class="icon">
                🤰
            </div>

            <strong>
                ANNE
            </strong>

            <span>
                Selenay
            </span>

        </div>


        <div class="box">

            <div class="icon">
                👨‍🍼
            </div>

            <strong>
                BABA
            </strong>

            <span>
                Hasan
            </span>

        </div>


        <div class="box">

            <div class="icon">
                🍼
            </div>

            <strong>
                TAHMİNİ TARİH
            </strong>

            <span>
                15 Aralık 2026
            </span>

        </div>


        <div class="box">

            <div class="icon">
                ❤️
            </div>

            <strong>
                DURUM
            </strong>

            <span>
                Seni bekliyoruz
            </span>

        </div>

    </div>


    <!-- MESAJ -->

    <p class="message">

        Minik kalbimizin ilk atışından
        beri hayatımız tamamen değişti.

        <br><br>

        Şimdi tek bir dileğimiz var:

        <br>

        Sağlıkla seni kucağımıza almak. 🤍

        <br><br>

        Seni daha görmeden çok seviyoruz,
        minik mucizemiz. 🍼✨

    </p>


    <!-- FOOTER -->

    <div class="footer">

        👶 Selenay & Hasan

        <br>

        Ailemize hoş geldin minik mucizemiz 🤍

    </div>

</div>

</section>


<script>

/* =====================================
   TAHMİNİ DOĞUM TARİHİ
   ===================================== */

const targetDate =
    new Date(
        "December 15, 2026 00:00:00"
    ).getTime();


/* GERİ SAYIM */

function countdown(){

    const now =
        new Date().getTime();

    const distance =
        targetDate - now;


    /* TARİH GELDİYSE */

    if(distance <= 0){

        document.getElementById(
            "days"
        ).innerHTML = "00";

        document.getElementById(
            "hours"
        ).innerHTML = "00";

        document.getElementById(
            "minutes"
        ).innerHTML = "00";

        document.getElementById(
            "seconds"
        ).innerHTML = "00";

        return;
    }


    /* GÜN */

    const days =
        Math.floor(
            distance /
            (1000 * 60 * 60 * 24)
        );


    /* SAAT */

    const hours =
        Math.floor(
            (
                distance %
                (1000 * 60 * 60 * 24)
            )
            /
            (1000 * 60 * 60)
        );


    /* DAKİKA */

    const minutes =
        Math.floor(
            (
                distance %
                (1000 * 60 * 60)
            )
            /
            (1000 * 60)
        );


    /* SANİYE */

    const seconds =
        Math.floor(
            (
                distance %
                (1000 * 60)
            )
            /
            1000
        );


    /* EKRANA YAZ */

    document.getElementById(
        "days"
    ).innerHTML =
        String(days).padStart(
            2,
            "0"
        );


    document.getElementById(
        "hours"
    ).innerHTML =
        String(hours).padStart(
            2,
            "0"
        );


    document.getElementById(
        "minutes"
    ).innerHTML =
        String(minutes).padStart(
            2,
            "0"
        );


    document.getElementById(
        "seconds"
    ).innerHTML =
        String(seconds).padStart(
            2,
            "0"
        );

}


/* HER SANİYE */

setInterval(
    countdown,
    1000
);

countdown();



/* =====================================
   UÇUŞAN KALPLER
   ===================================== */

function createHeart(){

    const heart =
        document.createElement(
            "div"
        );


    heart.className =
        "heart";


    /* KALP */

    heart.innerHTML =
        Math.random() > .5
        ? "🤍"
        : "🩷";


    /* KONUM */

    heart.style.left =
        Math.random() * 100 +
        "vw";


    /* BOYUT */

    heart.style.fontSize =
        (
            Math.random() * 12 + 12
        ) + "px";


    /* HIZ */

    heart.style.animationDuration =
        (
            Math.random() * 5 + 5
        ) + "s";


    document.body.appendChild(
        heart
    );


    /* TEMİZLE */

    setTimeout(
        () => {
            heart.remove();
        },
        10000
    );

}


/* KALPLER */

setInterval(
    createHeart,
    500
);

</script>

</body>
</html>
