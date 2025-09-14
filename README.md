<!doctype html>
<html lang="vi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Chúc mừng 20/10</title>
  <style>
    :root{--accent:#009e73;--text:#fff}
    html,body{
      height:100%;margin:0;
      font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,"Helvetica Neue",Arial;
    }
    body{
      background-color: #d88a92; /* màu hồng như trong ảnh bạn gửi */
      color:var(--text);
      display:flex;
      align-items:center;
      justify-content:center;
    }
    .card{
      width:min(980px,94vw);
      height:100vh;width:100vw;
      box-sizing:border-box;
      background:rgba(255,255,255,0.15); /* nền sáng để chữ dễ nhìn */
      backdrop-filter:blur(1px);
      border-radius:0;
      padding:36px 28px;
      box-shadow:none;
      position:relative;
      overflow:hidden;
      display:flex;
      flex-direction:column;
      justify-content:flex-start;
      align-items:center;
      text-align:center;
      padding-top:80px;
    }
    h1{font-size:58px;margin:0 0 20px 0;color:var(--accent);letter-spacing:1px}
    p.lead{margin:0 0 20px 0;font-size:20px;}

    /* hiệu ứng chữ trắng nhấp nháy */
    .blink-white {
      color:white;
      animation: blink 1.5s infinite;
    }
    @keyframes blink {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.6; }
    }

    /* trái tim rơi */
    .heart {
      position:absolute;
      top:-10%;
      color:#ffb6c1; /* hồng nhạt */
      font-size:20px;
      opacity:0.9;
      animation: fall linear forwards;
    }
    @keyframes fall{
      0%{transform:translateY(-20vh) rotate(0) translateX(0);opacity:1}
      100%{transform:translateY(120vh) rotate(360deg) translateX(120px);opacity:0}
    }

    @media (max-width:520px){h1{font-size:40px} .card{padding:20px;padding-top:60px}}
    #music-btn {
      position: fixed;
      bottom: 20px;
      right: 20px;
      width: 25px;
      height: 25px;
      border-radius: 50%;
      border: none;
      background-color: black;
      color: white;
      font-size: 14px;
      cursor: pointer;
      box-shadow: 0 4px 10px rgba(0,0,0,0.3);
      transition: transform 0.2s;
      z-index: 9999;
    }
    #music-btn:hover {
      transform: scale(1.1);
      background-color: #333;
    }
  </style>
</head>
<body>
  <div class="card" id="card">
    <h1>Chúc mừng 20/10</h1>
    <p class="lead blink-white">
      Thay mặt toàn thể các bạn nam trong lớp chúng tớ xin chúc các bạn nữ và cô giáo của chúng em một ngày 20/10 tràn ngập niềm vui,hạnh phúc và ý nghĩa. Chúng tớ mong các cậu cũng như là cô giáo luôn đồng hành cùng chúng tớ trên quãng đường còn lại ! 🌹 ❤️
    </p>
  </div>

  <audio id="bg-music" src="nhac.mp3" loop></audio>
  <button id="music-btn">🎵</button>

  <script>
    const music = document.getElementById('bg-music');
    const btn = document.getElementById('music-btn');
    let playing = false;
    btn.addEventListener('click', ()=>{
      if(playing){
        music.pause();
        btn.textContent = "🎵";
      }else{
        music.play();
        btn.textContent = "🔊";
      }
      playing = !playing;
    });

    function makeHeart(){
      const h = document.createElement('div');
      h.className = 'heart';
      h.textContent = '❤';
      const size = Math.random()*16 + 14;
      h.style.fontSize = size+'px';
      h.style.left = Math.random()*100+'%';
      h.style.top = (Math.random()*-20)+'%';
      h.style.opacity = (0.6 + Math.random()*0.4);
      const dur = 6 + Math.random()*8;
      h.style.animationDuration = dur+'s';
      document.body.appendChild(h);
      setTimeout(()=>h.remove(), (dur+1)*1000);
    }
    setInterval(makeHeart, 600);
  </script>
</body>
</html>
