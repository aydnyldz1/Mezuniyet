<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Emir & Elif 💍</title>

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
    background:#080706;
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
            #4a3218 0%,
            #21170d 25%,
            #0b0907 55%,
            #000 100%
        );
}

/* IŞIKLAR */
.hero::before{
    content:"";
    position:absolute;

    width:300px;
    height:300px;

    border-radius:50%;

    background:#d6b56a;

    filter:blur(130px);

    opacity:.14;

    top:-120px;
    left:-100px;
}

.hero::after{
    content:"";
    position:absolute;

    width:260px;
    height:260px;

    border-radius:50%;

    background:#d6b56a;

    filter:blur(130px);

    opacity:.10;

    right:-100px;
    bottom:-100px;
}

/* KART */
.card{
    width:100%;
    max-width:510px;

    position:relative;
    z-index:2;
}

/* KALP */
.rings{
    font-size:62px;

    display:inline-block;

    animation:
        float 3s ease-in-out infinite;

    filter:
        drop-shadow(
            0 8px 20px
            rgba(214,181,106,.25)
        );
}

@keyframes float{

    0%,100%{
        transform:translateY(0);
    }

    50%{
        transform:translateY(-8px);
    }

}

/* ÜST YAZI */
.small{
    color:#d6b56a;

    letter-spacing:4px;

    font-size:11px;

    font-weight:bold;

    margin-top:15px;
}

/* İSİMLER */
.names{
    font-family:
        Georgia,
        "Times New Roman",
        serif;

    font-size:51px;

    line-height:1.15;

    margin:16px 0;

    background:
        linear-gradient(
            90deg,
            #fff,
            #d6b56a,
            #fff3c4,
            #d6b56a,
            #fff
        );

    -webkit-background-clip:text;

    background-clip:text;

    color:transparent;

    background-size:250% auto;

    animation:
        goldText 5s linear infinite;
}

@keyframes goldText{

    to{
        background-position:
            250% center;
    }

}

/* ALT MESAJ */
.subtitle{
    color:#d4d0ca;

    font-family:Georgia, serif;

    font-size:16px;

    line-height:1.7;

    margin-bottom:25px;
}

/* AYRAÇ */
.divider{
    width:85px;

    height:1px;

    background:#d6b56a;

    margin:20px auto;

    box-shadow:
        0 0 15px
        rgba(214,181,106,.5);
}

/* GERİ SAYIM */
.countdown-title{
    color:#999;

    font-size:10px;

    letter-spacing:2px;

    margin-bottom:10px;
}

.countdown{
    display:flex;

    justify-content:center;

    gap:7px;

    margin:
        10px 0 28px;
}

.time{
    width:68px;

    padding:12px 4px;

    background:
        rgba(255,255,255,.035);

    border:
        1px solid
        rgba(214,181,106,.3);

    border-radius:15px;

    backdrop-filter:blur(10px);
}

.time b{
    display:block;

    color:#d6b56a;

    font-size:23px;

    line-height:1.2;
}

.time small{
    color:#999;

    font-size:9px;
}

/* BİLGİLER */
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

    border:
        1px solid
        rgba(214,181,106,.25);

    background:
        rgba(255,255,255,.035);

    border-radius:18px;

    backdrop-filter:blur(10px);
}

.icon{
    font-size:25px;

    margin-bottom:7px;
}

.box strong{
    color:#d6b56a;

    font-size:12px;

    margin-bottom:5px;
}

.box span{
    color:#ddd;

    font-size:13px;

    line-height:1.35;
}

/* HARİTA */
.map{
    display:inline-flex;

    align-items:center;

    justify-content:center;

    margin-top:20px;

    padding:14px 25px;

    border-radius:30px;

    background:#d6b56a;

    color:#0b0907;

    text-decoration:none;

    font-size:13px;

    font-weight:bold;

    box-shadow:
        0 8px 25px
        rgba(214,181,106,.12);

    transition:.3s;
}

.map:active{
    transform:scale(.96);
}

/* DAVET MESAJI */
.message{
    margin-top:30px;

    color:#ccc;

    font-family:Georgia, serif;

    font-size:15px;

    line-height:1.9;
}

/* ALT */
.footer{
    margin-top:30px;

    padding-bottom:10px;

    color:#777;

    font-size:12px;

    line-height:1.8;
}

/* ÇİÇEK / PARILTILAR */
.sparkle{
    position:fixed;

    width:4px;
    height:4px;

    border-radius:50%;

    background:#d6b56a;

    top:-10px;

    z-index:20;

    pointer-events:none;

    animation:
        fall linear forwards;
}

@keyframes fall{

    0%{
        transform:
            translateY(0)
            rotate(0deg);

        opacity:1;
    }

    100%{
        transform:
            translateY(110vh)
            rotate(360deg);

        opacity:0;
    }

}

/* MOBİL */
@media(max-width:420px){

    .hero{
        padding:30px 14px;
    }

    .names{
        font-size:42px;
    }

    .rings{
        font-size:55px;
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

    .names{
        font-size:36px;
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

    <!-- YÜZÜKLER -->
    <div class="rings">
        💍
    </div>

    <!-- ÜST BAŞLIK -->
    <div class="small">
        DÜĞÜN DAVETİYESİ
    </div>


    <!-- ÇİFT -->
    <div class="names">
        Emir & Elif
    </div>


    <div class="divider"></div>


    <!-- DAVET -->
    <p class="subtitle">

        Bir ömür boyu sürecek
        hikâyemizin en güzel gününde

        <br>

        sizleri de yanımızda görmekten
        mutluluk duyarız. ❤️

    </p>


    <!-- GERİ SAYIM -->
    <div class="countdown-title">
        MUTLULUĞUMUZA KALAN SÜRE
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
                📅
            </div>

            <strong>
                TARİH
            </strong>

            <span>
                26 Eylül 2026
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
                DÜĞÜN YERİ
            </strong>

            <span>
                Ordu Garden Davet
            </span>

        </div>


        <div class="box">

            <div class="icon">
                💃
            </div>

            <strong>
                KONSEPT
            </strong>

            <span>
                Düğün & Eğlence
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
        📍 Düğün Yerini Gör
    </a>


    <!-- MESAJ -->
    <p class="message">

        Sevgiyle başlayan hikâyemizi
        mutlulukla taçlandıracağımız
        bu özel günümüzde

        <br><br>

        sizleri de aramızda görmek
        bizleri çok mutlu edecektir.

        <br><br>

        Birlikte gülmek,
        birlikte eğlenmek
        ve bu güzel günü
        birlikte hatırlamak dileğiyle... 🥂

    </p>


    <!-- FOOTER -->
    <div class="footer">

        💍 Emir & Elif

        <br>

        Bir ömür boyu mutlulukla... ❤️

    </div>

</div>

</section>


<script>

/* =====================================
   DÜĞÜN TARİHİ
   ===================================== */

/*
   TARİHİ BURADAN DEĞİŞTİREBİLİRSİN.

   ÖRNEK:
   26 Eylül 2026
   Saat: 19:00
*/

const targetDate =
    new Date(
        "September 26, 2026 19:00:00"
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
   PARILTI EFEKTİ
   ===================================== */

function createSparkle(){

    const sparkle =
        document.createElement(
            "div"
        );


    sparkle.className =
        "sparkle";


    /* YATAY KONUM */

    sparkle.style.left =
        Math.random() * 100 +
        "vw";


    /* RASTGELE BOYUT */

    const size =
        Math.random() * 4 + 2;

    sparkle.style.width =
        size + "px";

    sparkle.style.height =
        size + "px";


    /* RASTGELE HIZ */

    sparkle.style.animationDuration =
        (
            Math.random() * 4 + 4
        ) + "s";


    /* EKLE */

    document.body.appendChild(
        sparkle
    );


    /* TEMİZLE */

    setTimeout(
        () => {
            sparkle.remove();
        },
        8000
    );

}


/* PARILTILARI ÜRET */

setInterval(
    createSparkle,
    300
);

</script>

</body>
</html>
