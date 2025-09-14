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
      background: url("lop.jpg") no-repeat center center/cover;
      color:var(--text);
      display:flex;
      align-items:center;
      justify-content:center;
    }
    .card{
      width:min(980px,94vw);
      height:100vh;width:100vw;
      box-sizing:border-box;
      background:rgba(0,0,0,0.4); /* nền mờ để nhìn rõ chữ */
      backdrop-filter:blur(2px);
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
    p.lead{margin:0 0 20px 0;font-size:20px;animation:rainbow 5s linear infinite;}
    @keyframes rainbow{
      0%{color:#e6194B}
      14%{color:#f58231}
      28%{color:#ffe119}
      42%{color:#bfef45}
      57%{color:#3cb44b}
      71%{color:#42d4f4}
      85%{color:#4363d8}
      100%{color:#e6194B}
    }
    .flower{position:absolute;top:-10%;left:50%;width:20px;height:20px;background:radial-gradient(circle,#ffe6f0 20%,#ff99cc 80%);border-radius:50%;opacity:0.9}
    @keyframes fall{0%{transform:translateY(-20vh) rotate(0) translateX(0);opacity:1}100%{transform:translateY(120vh) rotate(360deg) translateX(120px);opacity:0}}
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
    <p class="lead" style="color:pink">Thay mặt toàn thể các bạn nam trong lớp chúng tớ xin chúc các bạn nữ và cô giáo của chúng em một ngày 20/10 tràn ngập niềm vui,hạnh phúc và ý nghĩa. Chúng tớ mong các cậu cũng như là cô giáo luôn đồng hành cùng chúng tớ trên quãng đường còn lại ! 🌹 ❤️</p>
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

    function makeFlower(){
      const f = document.createElement('div');
      f.className = 'flower';
      const size = Math.random()*16 + 12;
      f.style.width = size+'px'; f.style.height = size+'px';
      f.style.left = Math.random()*100+'%';
      f.style.top = (Math.random()*-20)+'%';
      f.style.opacity = (0.6 + Math.random()*0.4);
      f.style.transform = 'rotate('+ (Math.random()*360) +'deg)';
      const dur = 6 + Math.random()*8;
      f.style.animation = `fall ${dur}s linear forwards`;
      document.body.appendChild(f);
      setTimeout(()=>f.remove(), (dur+1)*1000);
    }
    setInterval(makeFlower, 600);
  </script>
</body>
</html>

