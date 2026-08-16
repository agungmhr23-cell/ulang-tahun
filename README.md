<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Happy Birthday 💙</title>

<link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@500;600;700&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

<style>

/* =========================
   RESET
========================= */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    min-height: 100vh;
    overflow: hidden;

    font-family: 'Poppins', sans-serif;

    display: flex;
    justify-content: center;
    align-items: center;

    background:
        linear-gradient(
            180deg,
            #91edff 0%,
            #38c4e7 35%,
            #087ba8 70%,
            #023b5c 100%
        );

    color: white;
}


/* =========================
   BACKGROUND
========================= */

.ocean-bg {
    position: fixed;
    inset: 0;
    overflow: hidden;
    z-index: 0;
}

.light {
    position: absolute;

    width: 500px;
    height: 700px;

    top: -350px;
    left: 50%;

    transform: translateX(-50%);

    background:
        linear-gradient(
            100deg,
            transparent,
            rgba(255,255,255,.18),
            transparent
        );

    filter: blur(8px);

    animation: lightMove 6s ease-in-out infinite alternate;
}

@keyframes lightMove {

    from {
        transform:
            translateX(-100px)
            rotate(-8deg);
    }

    to {
        transform:
            translateX(100px)
            rotate(8deg);
    }
}


/* =========================
   BUBBLE
========================= */

.bubble {
    position: absolute;

    bottom: -50px;

    border-radius: 50%;

    border:
        1px solid
        rgba(255,255,255,.65);

    background:
        rgba(255,255,255,.08);

    animation:
        bubbleUp
        linear
        forwards;
}

@keyframes bubbleUp {

    0% {
        transform:
            translateY(0)
            translateX(0);

        opacity: 0;
    }

    15% {
        opacity: .8;
    }

    50% {
        transform:
            translateY(-50vh)
            translateX(30px);
    }

    100% {
        transform:
            translateY(-120vh)
            translateX(-30px);

        opacity: 0;
    }
}


/* =========================
   LUMBA-LUMBA
========================= */

.dolphin {
    position: fixed;

    top: 10%;
    left: -220px;

    width: 150px;

    z-index: 2;

    pointer-events: none;

    animation:
        dolphinSwim
        18s
        linear
        infinite;
}

.dolphin img {
    width: 100%;
    display: block;

    filter:
        drop-shadow(
            0 8px 15px
            rgba(0,0,0,.25)
        );
}

@keyframes dolphinSwim {

    0% {
        left: -220px;
        transform: rotate(5deg);
    }

    50% {
        left: 110%;
        transform: rotate(-5deg);
    }

    100% {
        left: 110%;
        transform: rotate(-5deg);
    }
}


/* =========================
   HIU
========================= */

.shark {
    position: fixed;

    top: 68%;
    right: -280px;

    width: 210px;

    z-index: 2;

    opacity: .8;

    pointer-events: none;

    animation:
        sharkSwim
        23s
        linear
        infinite;
}

.shark img {
    width: 100%;
    display: block;

    filter:
        drop-shadow(
            0 10px 20px
            rgba(0,0,0,.35)
        );
}

@keyframes sharkSwim {

    0% {
        right: -280px;
    }

    50% {
        right: 110%;
    }

    100% {
        right: -280px;
    }
}


/* =========================
   KARTU
========================= */

.card {
    position: relative;

    width: 92%;
    max-width: 430px;

    height: 680px;
    max-height: 90vh;

    overflow: hidden;

    border-radius: 30px;

    background:
        linear-gradient(
            180deg,
            rgba(5,100,145,.96),
            rgba(1,45,75,.99)
        );

    border:
        1px solid
        rgba(255,255,255,.3);

    box-shadow:
        0 25px 70px
        rgba(0,20,50,.6),

        0 0 35px
        rgba(80,220,255,.2);

    z-index: 10;
}


/* =========================
   SLIDE
========================= */

.slide {
    position: absolute;

    inset: 0;

    display: flex;
    flex-direction: column;

    opacity: 0;
    visibility: hidden;

    transform: translateX(100%);

    transition:
        .7s ease;
}

.slide.active {
    opacity: 1;
    visibility: visible;

    transform: translateX(0);
}

.slide.previous {
    transform: translateX(-100%);
}


/* =========================
   CONTENT
========================= */

.content {
    flex: 1;

    padding:
        25px
        25px
        85px;

    display: flex;

    flex-direction: column;

    justify-content: center;
    align-items: center;

    text-align: center;

    overflow-y: auto;
}

.content::-webkit-scrollbar {
    width: 0;
}


/* =========================
   TEXT
========================= */

.small-title {
    font-size: 10px;

    letter-spacing: 3px;

    text-transform: uppercase;

    color: #8feaff;

    margin-bottom: 5px;
}

h1 {
    font-family:
        'Dancing Script',
        cursive;

    font-size: 43px;

    line-height: 1.1;

    color: white;

    text-shadow:
        0 0 20px
        rgba(100,225,255,.7);

    margin-bottom: 8px;
}

h2 {
    font-family:
        'Dancing Script',
        cursive;

    font-size: 28px;

    color: #8eeaff;

    margin-bottom: 10px;
}

p {
    max-width: 340px;

    font-size: 13px;

    line-height: 1.8;

    color: #d9f7ff;

    margin: 5px 0;
}


/* =========================
   ICON
========================= */

.icon {
    font-size: 55px;

    margin-bottom: 5px;

    animation:
        floatIcon
        3s
        ease-in-out
        infinite;
}

@keyframes floatIcon {

    0%,100% {
        transform: translateY(0);
    }

    50% {
        transform: translateY(-8px);
    }
}


/* =========================
   VIDEO KECIL DI TENGAH
========================= */

.video-box {
    position: relative;

    width: 60%;

    max-width: 230px;

    height: 125px;

    margin: 12px auto;

    overflow: hidden;

    border-radius: 17px;

    background: #023b5c;

    border:
        2px solid
        rgba(140,235,255,.6);

    box-shadow:
        0 8px 20px
        rgba(0,0,0,.35),

        0 0 15px
        rgba(80,220,255,.2);

    flex-shrink: 0;
}

.video-box video {

    width: 100%;
    height: 100%;

    object-fit: cover;

    display: block;
}


/* =========================
   FOTO
========================= */

.photo {

    width: 180px;
    height: 180px;

    object-fit: cover;

    border-radius: 22px;

    margin:
        10px 0
        15px;

    border:
        3px solid
        rgba(130,235,255,.55);

    box-shadow:
        0 12px 30px
        rgba(0,0,0,.4);
}


/* =========================
   PIN
========================= */

.pin-box {

    display: flex;

    justify-content: center;

    gap: 7px;

    margin:
        10px 0;
}

.pin-box input {

    width: 48px;
    height: 55px;

    border-radius: 12px;

    border:
        1px solid
        #72e6ff;

    background:
        rgba(0,45,70,.8);

    color: white;

    text-align: center;

    font-size: 23px;

    outline: none;
}


/* =========================
   KEYBOARD
========================= */

.keyboard .row {

    display: flex;

    justify-content: center;
}

.keyboard button {

    width: 55px;
    height: 43px;

    margin: 3px;

    border: none;

    border-radius: 11px;

    background:
        linear-gradient(
            135deg,
            #16c5ec,
            #05628f
        );

    color: white;

    font-size: 16px;

    cursor: pointer;

    box-shadow:
        0 4px 10px
        rgba(0,0,0,.3);

    transition: .2s;
}

.keyboard button:hover {

    transform:
        translateY(-2px);

    box-shadow:
        0 0 18px
        rgba(90,225,255,.5);
}

.keyboard button:active {

    transform:
        scale(.9);
}


/* =========================
   ERROR
========================= */

#errorMsg {

    min-height: 20px;

    color: #ff9db8;

    font-size: 11px;
}

.clue {

    font-size: 10px;

    color: #9cc7d6;

    margin-top: 2px;
}


/* =========================
   NAVIGASI
========================= */

.nav-btns {

    position: absolute;

    bottom: 0;

    left: 0;
    right: 0;

    padding:
        13px 18px;

    display: flex;

    justify-content: space-between;

    background:
        rgba(1,30,50,.94);

    border-top:
        1px solid
        rgba(255,255,255,.12);

    z-index: 20;
}

.btn {

    padding:
        9px 16px;

    border: none;

    border-radius: 13px;

    background:
        linear-gradient(
            135deg,
            #17c8ee,
            #05648e
        );

    color: white;

    font-size: 12px;

    cursor: pointer;

    transition: .2s;
}

.btn:hover {

    transform:
        translateY(-2px);

    box-shadow:
        0 0 18px
        rgba(80,220,255,.4);
}


/* =========================
   TOMBOL MUSIK
========================= */

#musicToggle {

    position: fixed;

    bottom: 12px;

    left: 50%;

    transform:
        translateX(-50%);

    z-index: 100;

    border:
        1px solid
        rgba(150,235,255,.4);

    border-radius: 30px;

    padding:
        9px 19px;

    background:
        rgba(0,45,70,.95);

    color: white;

    font-family:
        'Poppins',
        sans-serif;

    font-size: 12px;

    cursor: pointer;

    box-shadow:
        0 8px 25px
        rgba(0,0,0,.4);
}


/* =========================
   HP
========================= */

@media (max-width: 500px) {

    .card {

        width: 94%;

        height: 650px;
    }

    h1 {
        font-size: 38px;
    }

    h2 {
        font-size: 25px;
    }

    .video-box {

        width: 60%;

        max-width: 220px;

        height: 115px;

        margin: 10px auto;
    }

    .photo {

        width: 160px;
        height: 160px;
    }

    .dolphin {
        width: 110px;
    }

    .shark {
        width: 160px;
    }
}


/* =========================
   HP KECIL
========================= */

@media (max-width: 380px) {

    .card {
        height: 620px;
    }

    .content {
        padding:
            18px
            18px
            75px;
    }

    h1 {
        font-size: 34px;
    }

    .icon {
        font-size: 45px;
    }

    .video-box {

        width: 58%;

        max-width: 200px;

        height: 105px;
    }

    .photo {

        width: 145px;
        height: 145px;
    }

    .keyboard button {

        width: 50px;
        height: 40px;
    }

}

</style>
</head>


<body>


<!-- =========================
     BACKGROUND
========================= -->

<div class="ocean-bg">

    <div class="light"></div>

</div>


<!-- =========================
     LUMBA-LUMBA
========================= -->

<div class="dolphin">

    <img
        src="mhrjr5.png"
        alt="Lumba-lumba"
    >

</div>


<!-- =========================
     HIU
========================= -->

<div class="shark">

    <img
        src="mhrjr6.png"
        alt="Hiu"
    >

</div>


<!-- =========================
     KARTU
========================= -->

<div class="card">


    <!-- =====================
         SLIDE 1
    ====================== -->

    <section
        class="slide active"
        id="slide1"
    >

        <div class="content">

            <div class="icon">
                🐬
            </div>

            <div class="small-title">
                A Little Surprise For You
            </div>

            <h1>
                Untukmu 💙
            </h1>

            <p>
                Ada sebuah kejutan kecil
                yang aku siapkan khusus
                untukmu.
            </p>

            <p>
                Masukkan PIN rahasianya
                untuk membuka kejutan ini.
            </p>


            <!-- VIDEO -->

            <div>

            <img
                class="photo"
                src="mhrjr2.jpeg"
                alt="Foto"
            >
            </div>


            <!-- PIN -->

            <div class="pin-box">

                <input
                    type="password"
                    maxlength="1"
                    readonly
                >

                <input
                    type="password"
                    maxlength="1"
                    readonly
                >

                <input
                    type="password"
                    maxlength="1"
                    readonly
                >

                <input
                    type="password"
                    maxlength="1"
                    readonly
                >

            </div>


            <!-- KEYBOARD -->

            <div class="keyboard">

                <div class="row">

                    <button onclick="pressNum(1)">
                        1
                    </button>

                    <button onclick="pressNum(2)">
                        2
                    </button>

                    <button onclick="pressNum(3)">
                        3
                    </button>

                </div>

                <div class="row">

                    <button onclick="pressNum(4)">
                        4
                    </button>

                    <button onclick="pressNum(5)">
                        5
                    </button>

                    <button onclick="pressNum(6)">
                        6
                    </button>

                </div>

                <div class="row">

                    <button onclick="pressNum(7)">
                        7
                    </button>

                    <button onclick="pressNum(8)">
                        8
                    </button>

                    <button onclick="pressNum(9)">
                        9
                    </button>

                </div>

                <div class="row">

                    <button onclick="deleteNum()">
                        ⌫
                    </button>

                    <button onclick="pressNum(0)">
                        0
                    </button>

                    <button onclick="checkPin()">
                        💙
                    </button>

                </div>

            </div>


            <div id="errorMsg"></div>

            <div class="clue">
                ✨ Clue: tahun lahirmu
            </div>

        </div>

    </section>



    <!-- =====================
         SLIDE 2
    ====================== -->

    <section
        class="slide"
        id="slide2"
    >

        <div class="content">

            <div class="icon">
                🎂
            </div>

            <div class="small-title">
                Today Is Your Special Day
            </div>

            <h1>
                Happy Birthday
            </h1>

            <h2>
                Selamat Ulang Tahun 💙
            </h2>


            <div>

       <div class="video-box">

                <video
                    autoplay
                    muted
                    loop
                    playsinline
                >

                    <source
                        src="mhrjr11.mp4"
                        type="video/mp4"
                    >

                </video>

            </div>


            </div>


            <p>
                Semoga hari ini dipenuhi
                senyum, tawa dan
                kebahagiaan.
            </p>

            <p>
                Semoga setiap detik
                hari ini menjadi
                kenangan yang indah.
            </p>

        </div>


        <div class="nav-btns">

            <button
                class="btn"
                onclick="prevSlide()"
            >
                ← Kembali
            </button>

            <button
                class="btn"
                onclick="nextSlide()"
            >
                Lanjut →
            </button>

        </div>

    </section>



    <!-- =====================
         SLIDE 3
    ====================== -->

    <section
        class="slide"
        id="slide3"
    >

        <div class="content">

            <div class="icon">
                🐚
            </div>

            <div class="small-title">
                My Wish For You
            </div>

            <h1>
                Doa & Harapan
            </h1>

 <div class="video-box">

                <video
                    autoplay
                    muted
                    loop
                    playsinline
                >

                    <source
                        src="mhrjr10.mp4"
                        type="video/mp4"
                    >

                </video>

            </div>


            <p>
                Semoga selalu diberikan
                kesehatan, kebahagiaan,
                dan keberkahan.
            </p>

            <p>
                Semoga semua impian yang
                kamu simpan perlahan
                menjadi kenyataan.
            </p>

            <p>
                Dan semoga senyummu
                selalu ada. ✨
            </p>

        </div>


        <div class="nav-btns">

            <button
                class="btn"
                onclick="prevSlide()"
            >
                ← Kembali
            </button>

            <button
                class="btn"
                onclick="nextSlide()"
            >
                Lanjut →
            </button>

        </div>

    </section>



    <!-- =====================
         SLIDE 4
    ====================== -->

    <section
        class="slide"
        id="slide4"
    >

        <div class="content">

            <div class="icon">
                💙
            </div>

            <div class="small-title">
                A Message From My Heart
            </div>

            <h1>
                Untuk Kamu
            </h1>


             <div class="video-box">

                <video
                    autoplay
                    muted
                    loop
                    playsinline
                >

                    <source
                        src="mhrjr9.mp4"
                        type="video/mp4"
                    >

                </video>

            </div>


            <p>
                Di antara luasnya lautan,
                ada satu hal yang ingin
                aku sampaikan.
            </p>

            <p>
                Terima kasih sudah hadir
                dan menjadi bagian
                dari cerita hidupku.
            </p>

            <p>
                Kamu adalah salah satu
                hal indah yang patut
                disyukuri. 💙
            </p>

        </div>


        <div class="nav-btns">

            <button
                class="btn"
                onclick="prevSlide()"
            >
                ← Kembali
            </button>

            <button
                class="btn"
                onclick="nextSlide()"
            >
                Lanjut →
            </button>

        </div>

    </section>



    <!-- =====================
         SLIDE 5
    ====================== -->

    <section
        class="slide"
        id="slide5"
    >

        <div class="content">

            <div class="icon">
                🐬💙
            </div>

            <div class="small-title">
                One Last Message
            </div>

            <h1>
                Terima Kasih
            </h1>


            <div class="video-box">

                <video
                    autoplay
                    muted
                    loop
                    playsinline
                >

                    <source
                        src="mhrjr8.mp4"
                        type="video/mp4"
                    >

                </video>

            </div>

            <p>
                Terima kasih sudah
                membuka kejutan kecil ini.
            </p>

            <p>
                Semoga perjalanan hidupmu
                selalu indah seperti
                lautan yang luas.
            </p>

            <p>
                Tetap tersenyum,
                tetap kuat,
                dan jangan pernah berhenti
                mengejar impianmu.
            </p>

            <h2>
                Happy Birthday 💙
            </h2>

            <p>
                Semoga bahagia selalu.
                🐬🌊🦈
            </p>

        </div>


        <div
            class="nav-btns"
            style="justify-content:center;"
        >

            <button
                class="btn"
                onclick="prevSlide()"
            >
                ← Kembali
            </button>

        </div>

    </section>

</div>



<!-- =========================
     MUSIC
========================= -->

<button
    id="musicToggle"
    onclick="toggleMusic()"
>
    🔇 Musik OFF
</button>



<script>

/* =========================
   PIN
========================= */

const CORRECT_PIN = "2001";

const inputs =
    document.querySelectorAll(
        ".pin-box input"
    );

let pinIndex = 0;


function pressNum(num) {

    if (pinIndex >= 4) {
        return;
    }

    inputs[pinIndex].value = num;

    pinIndex++;
}


function deleteNum() {

    if (pinIndex <= 0) {
        return;
    }

    pinIndex--;

    inputs[pinIndex].value = "";
}


function checkPin() {

    const pin =
        Array.from(inputs)
        .map(input => input.value)
        .join("");

    if (pin === CORRECT_PIN) {

        document.getElementById(
            "errorMsg"
        ).innerText = "";

        startMusic();

        createBubbleBurst();

        setTimeout(
            function() {
                showSlide(2);
            },
            400
        );

    } else {

        document.getElementById(
            "errorMsg"
        ).innerText =
            "💔 PIN salah, coba lagi.";

        inputs.forEach(
            input => {
                input.value = "";
            }
        );

        pinIndex = 0;
    }
}


/* =========================
   SLIDE
========================= */

let currentSlide = 1;

const slides =
    document.querySelectorAll(
        ".slide"
    );


function showSlide(number) {

    if (
        number < 1 ||
        number > slides.length
    ) {
        return;
    }

    slides.forEach(
        slide => {
            slide.classList.remove(
                "active",
                "previous"
            );
        }
    );

    if (number > currentSlide) {

        slides[
            currentSlide - 1
        ].classList.add(
            "previous"
        );
    }

    slides[
        number - 1
    ].classList.add(
        "active"
    );

    currentSlide = number;
}


function nextSlide() {

    if (
        currentSlide <
        slides.length
    ) {

        showSlide(
            currentSlide + 1
        );
    }
}


function prevSlide() {

    if (
        currentSlide > 2
    ) {

        showSlide(
            currentSlide - 1
        );
    }
}


/* =========================
   MUSIK
========================= */

const music =
    new Audio("musik.mp3");

music.loop = true;

music.volume = 1;

let isPlaying = false;


function startMusic() {

    music.play()
        .then(
            function() {

                isPlaying = true;

                document.getElementById(
                    "musicToggle"
                ).innerText =
                    "🔊 Musik ON";

            }
        )
        .catch(
            function() {

                document.getElementById(
                    "musicToggle"
                ).innerText =
                    "▶️ Putar Musik";

            }
        );
}


function toggleMusic() {

    if (isPlaying) {

        music.pause();

        isPlaying = false;

        document.getElementById(
            "musicToggle"
        ).innerText =
            "🔇 Musik OFF";

    } else {

        music.play()
            .then(
                function() {

                    isPlaying = true;

                    document.getElementById(
                        "musicToggle"
                    ).innerText =
                        "🔊 Musik ON";

                }
            );
    }
}


/* =========================
   BUBBLE
========================= */

function createBubble() {

    const bubble =
        document.createElement(
            "div"
        );

    bubble.className =
        "bubble";

    const size =
        5 +
        Math.random() * 18;

    bubble.style.width =
        size + "px";

    bubble.style.height =
        size + "px";

    bubble.style.left =
        Math.random() * 100 + "%";

    bubble.style.animationDuration =
        5 +
        Math.random() * 6 +
        "s";

    document
        .querySelector(
            ".ocean-bg"
        )
        .appendChild(
            bubble
        );

    setTimeout(
        function() {
            bubble.remove();
        },
        12000
    );
}


setInterval(
    createBubble,
    600
);


function createBubbleBurst() {

    for (
        let i = 0;
        i < 35;
        i++
    ) {

        setTimeout(
            createBubble,
            i * 50
        );
    }
}


for (
    let i = 0;
    i < 15;
    i++
) {

    setTimeout(
        createBubble,
        i * 200
    );
}

</script>

</body>
</html>
.video-box {
    position: relative;

    width: 70%;
    max-width: 280px;

    height: 150px;

    margin: 12px auto;

    overflow: hidden;

    border-radius: 18px;

    background: #023b5c;

    border: 2px solid rgba(140, 235, 255, 0.6);

    box-shadow:
        0 8px 20px rgba(0, 0, 0, 0.3),
        0 0 15px rgba(80, 220, 255, 0.2);

    flex-shrink: 0;
}

.video-box video {
    width: 100%;
    height: 100%;

    object-fit: cover;

    display: block;
}


/* HP */

@media (max-width: 500px) {

    .video-box {
        width: 60%;
max-width: 230px;
height: 125px;
        margin: 10px auto;
        border-radius: 16px;
    }

}
