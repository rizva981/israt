<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Happy Birthday</title>

<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

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
    font-family:'Poppins',sans-serif;
    overflow-x:hidden;
    background:#dff8ff;
    color:white;
}

/* MAIN CONTENT BLUR EFFECT ON OPEN */
#main-content {
    transition: filter 2.5s ease-in-out;
    filter: blur(15px);
}

#main-content.reveal {
    filter: blur(0px);
}

/* TOP NAVIGATION MENU */
.nav-menu {
    position: fixed;
    top: 20px;
    left: 50%;
    transform: translateX(-50%);
    z-index: 1000;
    background: rgba(255, 255, 255, 0.15);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.3);
    padding: 10px 30px;
    border-radius: 40px;
    display: flex;
    gap: 30px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.nav-menu a {
    color: white;
    text-decoration: none;
    font-size: 16px;
    font-weight: 500;
    transition: 0.3s;
    letter-spacing: 1px;
}

.nav-menu a:hover {
    color: #dff8ff;
    text-shadow: 0 0 10px rgba(255, 255, 255, 0.6);
}

/* FLOATING EMOJIS */
.floating-emoji {
    position: absolute;
    font-size: 55px;
    opacity: 0.25;
    pointer-events: none;
    z-index: 1;
    animation: floatAnimation 8s ease-in-out infinite;
}

.e-cake1 { top: 15%; left: 8%; animation-delay: 0s; }
.e-crown1 { top: 25%; right: 10%; animation-delay: 1.5s; font-size: 65px; }
.e-heart1 { top: 70%; left: 12%; animation-delay: 3s; }
.e-balloon1 { top: 45%; right: 7%; animation-delay: 0.5s; }

.e-cake2 { top: 15%; left: 10%; animation-delay: 2s; }
.e-crown2 { top: 65%; right: 12%; animation-delay: 0.8s; }
.e-heart2 { top: 35%; left: 8%; animation-delay: 3.5s; }
.e-star1 { top: 75%; left: 45%; animation-delay: 1s; }

.e-cake3 { top: 30%; right: 15%; animation-delay: 2.5s; }
.e-balloon2 { top: 65%; left: 15%; animation-delay: 1.2s; }
.e-star2 { top: 15%; left: 25%; animation-delay: 4s; }

@keyframes floatAnimation {
    0% { transform: translateY(0px) rotate(0deg); }
    50% { transform: translateY(-30px) rotate(15deg); }
    100% { transform: translateY(0px) rotate(0deg); }
}

/* INTRO / DOOR */
#intro{
    position:fixed;
    inset:0;
    z-index:99999;
    overflow:hidden;
    background:linear-gradient(135deg,#87ceeb,#4facfe,#00c6ff);
    transition: opacity 1s ease;
}

.door{
    position:absolute;
    width:50%;
    height:100%;
    background:linear-gradient(135deg,#38bdf8,#0ea5e9);
    transition:2.5s cubic-bezier(0.25, 1, 0.5, 1);
    top:0;
}

.left-door{
    left:0;
    border-right:3px solid rgba(255,255,255,.5);
}

.right-door{
    right:0;
    border-left:3px solid rgba(255,255,255,.5);
}

.ribbon{
    position:absolute;
    width:18px;
    height:100%;
    background:white;
    left:50%;
    transform:translateX(-50%);
}

.ribbon::before{
    content:"🎀";
    position:absolute;
    top:45%;
    left:50%;
    transform:translate(-50%,-50%);
    font-size:55px;
}

/* OPEN BUTTON */
#openBtn{
    position:absolute;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    z-index:10;
    border:none;
    background: transparent;
    color:white;
    padding:20px;
    font-size:42px;
    font-family:'Great Vibes',cursive;
    cursor:pointer;
    text-shadow: 0 0 20px rgba(255, 255, 255, 0.6);
    transition:.4s;
}

#openBtn:hover{
    transform:translate(-50%,-50%) scale(1.08);
    text-shadow: 0 0 30px rgba(255, 255, 255, 0.9);
}

.open-left{ transform:translateX(-100%); }
.open-right{ transform:translateX(100%); }

/* BG BOTTOM UP FLOATING EMOJIS */
.bg-emoji{
    position:fixed;
    font-size:35px;
    opacity:.12;
    animation:bgfloat 12s linear infinite;
    z-index:0;
    pointer-events:none;
}
.bg1{ left:5%; animation-duration:10s; }
.bg2{ left:20%; animation-duration:15s; }
.bg3{ left:35%; animation-duration:12s; }
.bg4{ left:50%; animation-duration:9s; }
.bg5{ left:70%; animation-duration:13s; }
.bg6{ left:85%; animation-duration:11s; }

@keyframes bgfloat{
    0%{ transform: translateY(100vh) rotate(0deg); }
    100%{ transform: translateY(-120vh) rotate(360deg); }
}

/* SECTION */
section{
    min-height:100vh;
    position:relative;
    padding:140px 20px 120px 20px;
    z-index:2;
}

/* HOME PAGE */
#home{
    background: linear-gradient(135deg,#87ceeb,#6dd5fa,#4facfe);
    display:flex;
    justify-content:center;
    align-items:center;
}

.home-box{
    width:95%;
    max-width:1200px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:60px;
    flex-wrap:wrap;
}

.left{ flex:1; }

.title{
    font-size:115px;
    font-family:'Great Vibes',cursive;
    line-height:1.1;
    text-shadow:0 0 20px rgba(255,255,255,.35);
}

.name{
    margin-top:20px;
    font-size:35px;
    letter-spacing:3px;
}

/* SHARED SCROLL STYLE */
.scroll, .scroll-page2{
    margin-top:70px;
    font-size:28px;
    font-family:'Great Vibes',cursive;
    animation:updown 2s infinite;
    text-align: center;
}

.scroll-page2 {
    margin-top: 50px;
    width: 100%;
}

@keyframes updown{
    0%, 100%{ transform:translateY(0); }
    50%{ transform:translateY(-10px); }
}

.right{
    flex:1;
    display:flex;
    justify-content:center;
    position:relative;
}

.right img{
    width:380px;
    height:500px;
    object-fit:cover;
    border-radius:35px;
    border:6px solid rgba(255,255,255,.35);
    box-shadow:0 0 40px rgba(255,255,255,.4);
    z-index:5;
}

/* PHOTO HEART ANIMATION */
.right::before, .right::after{
    content:"💙";
    position:absolute;
    font-size:28px;
    animation:heartFly 5s linear infinite;
    opacity:.9;
    z-index:6;
}
.right::before{ left:10%; bottom:0; }
.right::after{ right:10%; bottom:-40px; animation-delay:2s; }

@keyframes heartFly{
    0%{ transform: translateY(0) scale(.8); opacity:0; }
    20%{ opacity:1; }
    100%{ transform: translateY(-350px) scale(1.4); opacity:0; }
}

.love{
    position:absolute;
    font-size:22px;
    animation:miniFly 4s linear infinite;
    opacity:.9;
    z-index:6;
}
.love1{ left:15%; bottom:30px; }
.love2{ right:15%; bottom:10px; animation-delay:1.5s; }
.love3{ left:50%; bottom:-10px; animation-delay:3s; }

@keyframes miniFly{
    0%{ transform: translateY(0) scale(.7); opacity:0; }
    20%{ opacity:1; }
    100%{ transform: translateY(-250px) scale(1.3); opacity:0; }
}

/* PAGE 2 - MESSAGE LAYOUT */
#message {
    background: linear-gradient(135deg,#74ebd5,#6dd5fa,#4facfe);
}

.message-container {
    width: 100%;
    max-width: 1000px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    gap: 80px;
}

.msg-block {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 40px;
    width: 100%;
    position: relative;
    z-index: 5;
}

.msg-text {
    flex: 1.3;
    font-size: 24px;
    line-height: 1.8;
}

.text-right-align { text-align: right; }

/* 👑 PRINCESS CROWN OVER IMAGE CORNERS (ADDED EFFECT) 👑 */
.msg-photo {
    flex: 1;
    display: flex;
    justify-content: center;
    position: relative; /* ক্রাউন পজিশন ঠিক রাখার জন্য */
}

.msg-photo img {
    width: 320px;
    height: 400px;
    object-fit: cover;
    border-radius: 30px;
    border: 5px solid rgba(255,255,255,.35);
    box-shadow: 0 0 30px rgba(255,255,255,.3);
    position: relative;
    z-index: 4;
}

/* ১ম ছবির ক্রাউন (উপরের বাম কোনায় একটু বাঁকানো) */
.crown-left::before {
    content: "👑";
    position: absolute;
    top: -25px;
    left: 20px;
    font-size: 50px;
    z-index: 10;
    transform: rotate(-20deg);
    filter: drop-shadow(0px 5px 5px rgba(0,0,0,0.2));
}

/* ২য় ছবির ক্রাউন (উপরের ডান কোনায় একটু বাঁকানো) */
.crown-right::before {
    content: "👑";
    position: absolute;
    top: -25px;
    right: 20px;
    font-size: 50px;
    z-index: 10;
    transform: rotate(20deg);
    filter: drop-shadow(0px 5px 5px rgba(0,0,0,0.2));
}

/* PAGE 3 - BLUR BACKGROUND */
#wish{
    background: url('israt.jpg') no-repeat center center;
    background-size: cover;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
}

.overlay{
    position: absolute;
    inset: 0;
    backdrop-filter: blur(15px);
    background: rgba(0, 0, 0, 0.25);
}

.wish-box{
    position:relative;
    z-index:5;
    width:90%;
    max-width:900px;
    padding:60px;
    border-radius:40px;
    background:rgba(255,255,255,.12);
    backdrop-filter:blur(12px);
    border:1px solid rgba(255,255,255,.3);
    text-align:center;
}

.wish-title{
    font-size:90px;
    font-family:'Great Vibes',cursive;
}

.wish-text{
    margin-top:30px;
    font-size:28px;
    line-height:2;
}

/* ====== MOBILE RESPONSIVE CHANGES ====== */
@media(max-width:900px){

    .nav-menu {
        width: 85%;
        justify-content: center;
        gap: 15px;
        padding: 8px 15px;
        top: 15px;
    }

    .nav-menu a { font-size: 13px; }

    .floating-emoji {
        font-size: 38px !important;
    }

    .home-box{
        flex-direction: column;
        text-align: center;
        gap: 30px;
    }

    .title{ font-size: 65px; }
    .name{ font-size: 22px; letter-spacing: 2px; }
    .scroll { margin-top: 25px; font-size: 22px; }
    .scroll-page2 { margin-top: 30px; font-size: 22px; }
    .right { order: -1; }
    .right img{ width: 250px; height: 330px; }

    .message-container { gap: 40px; }

    .msg-block {
        display: flex !important;
        flex-direction: row !important;
        gap: 15px;
        align-items: center;
    }

    .msg-text {
        flex: 1.2;
        font-size: 13px;
        line-height: 1.5;
    }

    .msg-photo { flex: 1; }
    .msg-photo img {
        width: 100%;
        max-width: 130px;
        height: 170px;
        border-radius: 15px;
        border: 3px solid rgba(255,255,255,.35);
    }
    
    /* মোবাইলের জন্য ক্রাউনের সাইজ এবং পজিশন অ্যাডজাস্টমেন্ট */
    .crown-left::before {
        font-size: 30px;
        top: -15px;
        left: -2px;
    }
    .crown-right::before {
        font-size: 30px;
        top: -15px;
        right: -2px;
    }

    .wish-box { padding: 30px 20px; width: 95%; }
    .wish-title{ font-size: 48px; }
    .wish-text{ font-size: 18px; line-height: 1.7; }

    #openBtn{
        font-size: 30px;
        padding: 10px;
        width: auto;
        white-space: nowrap;
    }
    
    .ribbon::before { font-size: 45px; }
}

</style>

</head>

<body>

<div id="intro">
    <div class="door left-door">
        <div class="ribbon"></div>
    </div>
    <div class="door right-door">
        <div class="ribbon"></div>
    </div>
    <button id="openBtn">
        Click for Surprise ✨
    </button>
</div>

<div id="main-content">

    <div class="nav-menu">
        <a href="#home">Home</a>
        <a href="#message">Messages</a>
        <a href="#wish">Wishes</a>
    </div>

    <audio id="music" loop preload="auto">
        <source src="her2.mp3" type="audio/mp3">
    </audio>

    <div class="bg-emoji bg1">🎂</div>
    <div class="bg-emoji bg2">🎈</div>
    <div class="bg-emoji bg3">💙</div>
    <div class="bg-emoji bg4">🦋</div>
    <div class="bg-emoji bg5">🎉</div>
    <div class="bg-emoji bg6">✨</div>

    <section id="home">
        <div class="floating-emoji e-cake1">🎂</div>
        <div class="floating-emoji e-crown1">👑</div>
        <div class="floating-emoji e-balloon1">🎈</div>

        <div class="home-box">
            <div class="left">
                <h1 class="title">Happy <br> Birthday</h1>
                <div class="name">𝑺𝒂𝒅𝒊𝒂 𝑰𝒔𝒓𝒂𝒕‪‪❤︎‬<br><small><i><font size="2">Faitytale</font></i></small></div>
                <div class="scroll">Scroll For Next Page ↓</div>
            </div>
            <div class="right">
                <img src="israt.jpeg">
                <div class="love love1">💙</div>
                <div class="love love2">🤍</div>
                <div class="love love3">🩵</div>
            </div>
        </div>
    </section>

    <section id="message">
        <div class="floating-emoji e-cake2">🎂</div>
        <div class="floating-emoji e-crown2">👑</div>
        <div class="floating-emoji e-heart2">💖</div>
        <div class="floating-emoji e-star1">✨</div>

        <div class="message-container">
            <div class="msg-block">
                <div class="msg-text">
                    𝑯𝒊𝒊!<br>
𝑯𝒂𝒑𝒑𝒚 𝑩𝒊𝒓𝒕𝒉𝒅𝒂𝒚 𝑺𝒂𝒅𝒊𝒂...<br><br>

𝑫𝒐 𝒚𝒐𝒖 𝒌𝒏𝒐𝒘 𝒕𝒉𝒂𝒕 𝒐𝒏 𝒕𝒉𝒊𝒔 𝒅𝒂𝒚 𝒊𝒏 𝟐𝟎𝟎𝟖, 𝒂 𝒃𝒆𝒂𝒖𝒕𝒊𝒇𝒖𝒍 𝒍𝒊𝒕𝒕𝒍𝒆 𝒈𝒊𝒓𝒍 𝒘𝒂𝒔 𝒃𝒐𝒓𝒏 𝒊𝒏𝒕𝒐 𝒕𝒉𝒊𝒔 𝒘𝒐𝒓𝒍𝒅...<br><br>

𝑰 𝒘𝒂𝒔𝒏'𝒕 𝒕𝒉𝒆𝒓𝒆, 𝒃𝒖𝒕 𝑰 𝒕𝒉𝒊𝒏𝒌 𝒕𝒉𝒆 𝒘𝒉𝒐𝒍𝒆 𝒉𝒐𝒔𝒑𝒊𝒕𝒂𝒍 𝒎𝒖𝒔𝒕 𝒉𝒂𝒗𝒆 𝒔𝒉𝒐𝒏𝒆 𝒘𝒊𝒕𝒉 𝒍𝒊𝒈𝒉𝒕, 𝒃𝒆𝒄𝒂𝒖𝒔𝒆 𝒚𝒐𝒖 𝒃𝒓𝒐𝒖𝒈𝒉𝒕 𝒉𝒂𝒑𝒑𝒊𝒏𝒆𝒔𝒔 𝒂𝒏𝒅 𝒍𝒊𝒈𝒉𝒕 𝒘𝒊𝒕𝒉 𝒚𝒐𝒖.‪‪❤︎‬
                </div>
                <div class="msg-photo crown-left">
                    <img src="israt2.jpeg">
                </div>
            </div>
            
            <div class="msg-block">
                <div class="msg-photo crown-right">
                    <img src="israt3.jpeg">
                </div>
                <div class="msg-text text-right-align">
                    𝑯𝒂𝒑𝒑𝒚 𝑩𝒊𝒓𝒕𝒉𝒅𝒂𝒚, 𝑰𝒔𝒓𝒂𝒕!<br><br>

𝑻𝒉𝒂𝒏𝒌 𝒚𝒐𝒖 𝒇𝒐𝒓 𝒂𝒍𝒍 𝒕𝒉𝒆 𝒎𝒆𝒎𝒐𝒓𝒊𝒆𝒔, 𝒍𝒂𝒖𝒈𝒉𝒕𝒆𝒓, 𝒂𝒏𝒅 𝒎𝒐𝒎𝒆𝒏𝒕𝒔 𝒘𝒆'𝒗𝒆 𝒔𝒉𝒂𝒓𝒆𝒅.
𝒀𝒐𝒖 𝒎𝒂𝒌𝒆 𝒍𝒊𝒇𝒆 𝒃𝒓𝒊𝒈𝒉𝒕𝒆𝒓 𝒋𝒖𝒔𝒕 𝒃𝒚 𝒃𝒆𝒊𝒏𝒈 𝒚𝒐𝒖𝒓𝒔𝒆𝒍𝒇.<br><br>

𝑴𝒂𝒚 𝒕𝒉𝒊𝒔 𝒚𝒆𝒂𝒓 𝒃𝒓𝒊𝒏𝒈 𝒚𝒐𝒖 𝒆𝒏𝒅𝒍𝒆𝒔𝒔 𝒋𝒐𝒚, 𝒔𝒖𝒄𝒄𝒆𝒔𝒔, 𝒂𝒏𝒅 𝒆𝒗𝒆𝒓𝒚𝒕𝒉𝒊𝒏𝒈 𝒚𝒐𝒖𝒓 𝒉𝒆𝒂𝒓𝒕 𝒅𝒆𝒔𝒊𝒓𝒆𝒔.‪‪❤︎‬
                </div>
            </div>
            
            <div class="scroll-page2">
                Scroll For Final Page ↓
            </div>
        </div>
    </section>

    <section id="wish">
        <div class="overlay"></div>
        
        <div class="floating-emoji e-cake3">🎂</div>
        <div class="floating-emoji e-balloon2">🎈</div>
        <div class="floating-emoji e-star2">✨</div>
        <div class="floating-emoji e-heart1">💙</div>

        <div class="wish-box">
            <div class="wish-title">One Wish</div>
            <div class="wish-text"><small>
𝑰 𝑾𝑰𝑺𝑯 𝒀𝑶𝑼 𝑮𝑬𝑻 𝑬𝑽𝑬𝑹𝒀𝑻𝑯𝑰𝑵𝑮 𝒀𝑶𝑼'𝑽𝑬 𝑬𝑽𝑬𝑹 𝑾𝑰𝑺𝑯𝑬𝑫 𝑭𝑶𝑹....<br><br>

𝑰 𝑾𝑰𝑺𝑯 𝒀𝑶𝑼 𝑵𝑬𝑽𝑬𝑹 𝑭𝑶𝑹𝑮𝑬𝑻 𝑴𝑬, 𝑵𝑶 𝑴𝑨𝑻𝑻𝑬𝑹 𝑾𝑯𝑬𝑹𝑬 𝑳𝑰𝑭𝑬 𝑻𝑨𝑲𝑬𝑺 𝑼𝑺....<br><br>

𝑰 𝑾𝑰𝑺𝑯 𝑾𝑬 𝑪𝑶𝑼𝑳𝑫 𝑩𝑬 𝑪𝑳𝑨𝑺𝑺𝑴𝑨𝑻𝑬𝑺 𝑶𝑵𝑪𝑬 𝑨𝑮𝑨𝑰𝑵 𝑨𝑵𝑫 𝑹𝑬𝑳𝑰𝑽𝑬 𝑻𝑯𝑶𝑺𝑬 𝑩𝑬𝑨𝑼𝑻𝑰𝑭𝑼𝑳 𝑴𝑬𝑴𝑶𝑹𝑰𝑬𝑺....<br><br>

𝑰 𝑾𝑰𝑺𝑯 𝑻𝑯𝑬 𝑨𝑮𝑬 𝑮𝑨𝑷 𝑩𝑬𝑻𝑾𝑬𝑬𝑵 𝑼𝑺 𝑫𝑰𝑫𝑵'𝑻 𝑬𝑿𝑰𝑺𝑻....<br><br>

𝑰 𝑾𝑰𝑺𝑯 𝑰 𝑪𝑶𝑼𝑳𝑫 𝑻𝑬𝑳𝑳 𝒀𝑶𝑼 𝑬𝑽𝑬𝑹𝒀𝑻𝑯𝑰𝑵𝑮 𝑰'𝑽𝑬 𝑨𝑳𝑾𝑨𝒀𝑺 𝑾𝑨𝑵𝑻𝑬𝑫 𝑻𝑶 𝑺𝑨𝒀....<br><br>

𝑨𝑵𝑫 𝑨𝑩𝑶𝑽𝑬 𝑨𝑳𝑳, 𝑰 𝑾𝑰𝑺𝑯 𝒀𝑶𝑼 𝑨 𝑳𝑰𝑭𝑬 𝑭𝑰𝑳𝑳𝑬𝑫 𝑾𝑰𝑻𝑯 𝑯𝑨𝑷𝑷𝑰𝑵𝑬𝑺𝑺, 𝑳𝑶𝑽𝑬, 𝑨𝑵𝑫 𝑬𝑵𝑫𝑳𝑬𝑺𝑺 𝑹𝑬𝑨𝑺𝑶𝑵𝑺 𝑻𝑶 𝑺𝑴𝑰𝑳𝑬....<br><br>

𝑶𝑵𝑪𝑬 𝑨𝑮𝑨𝑰𝑵, 𝑯𝑨𝑷𝑷𝒀 𝑩𝑰𝑹𝑻𝑯𝑫𝑨𝒀, 𝑴𝒚 𝒍𝒐𝒗𝒆 𝒂𝒕 𝒇𝒊𝒓𝒔𝒕 𝒔𝒊𝒈𝒉𝒕....❤️</small>
            </div>
        </div>
    </section>

</div>

<script>

const openBtn = document.getElementById("openBtn");
const intro = document.getElementById("intro");
const leftDoor = document.querySelector(".left-door");
const rightDoor = document.querySelector(".right-door");
const music = document.getElementById("music");
const mainContent = document.getElementById("main-content");

openBtn.addEventListener("click", () => {
    leftDoor.classList.add("open-left");
    rightDoor.classList.add("open-right");
    
    music.play().catch(error => {
        console.log("Audio play failed:", error);
    });

    setTimeout(() => {
        mainContent.classList.add("reveal");
    }, 100);

    setTimeout(() => {
        intro.style.display = "none";
    }, 2500);
});

</script>

</body>
</html>
