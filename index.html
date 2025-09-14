<!doctype html>
<html lang="vi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Chúc mừng 20/10</title>
  <style>
    :root{--bg:#f0fff9;--accent:#009e73;--text:#1f3b2d}
    html,body{height:100%;margin:0;font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,"Helvetica Neue",Arial}
    body{background:radial-gradient(circle at 20% 20%, #f6fffb 0%, var(--bg) 35%), linear-gradient(180deg,#fff 0%, #f0fff9 100%);color:var(--text);display:flex;align-items:center;justify-content:center}
    .card{width:min(980px,94vw);height:100vh;width:100vw;box-sizing:border-box;background:linear-gradient(180deg,rgba(255,255,255,0.6),rgba(255,255,255,0.3));backdrop-filter:blur(6px);border-radius:0;padding:36px 28px;box-shadow:none;position:relative;overflow:hidden;display:flex;flex-direction:column;justify-content:flex-start;align-items:center;text-align:center;padding-top:80px}
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
    /* falling flowers */
    .flower{position:absolute;top:-10%;left:50%;width:20px;height:20px;background:radial-gradient(circle,#ffe6f0 20%,#ff99cc 80%);border-radius:50%;opacity:0.9}
    @keyframes fall{0%{transform:translateY(-20vh) rotate(0) translateX(0);opacity:1}100%{transform:translateY(120vh) rotate(360deg) translateX(120px);opacity:0}}
    /* controls */
    .controls{position:absolute;right:18px;bottom:14px;display:flex;gap:8px;align-items:center}
    .btn{background:rgba(255,255,255,0.8);border:1px solid rgba(0,0,0,0.06);padding:8px 10px;border-radius:999px;cursor:pointer;font-weight:600;backdrop-filter:blur(4px)}
    .btn:active{transform:translateY(1px)}
    .music-btn{width:44px;height:44px;display:grid;place-items:center;border-radius:50%;}
    @media (max-width:520px){h1{font-size:40px} .card{padding:20px;padding-top:60px}}
  </style>
</head>
<body>
  <div class="card" id="card">
    <h1>Chúc mừng 20/10</h1>
    <p class="lead">Chúc toàn thể các bạn nữ trong lớp 9B và cô giáo chủ nhiệm có một ngày 20/10 thật nhiều niềm vui, sức khỏe và hạnh phúc! 🌹</p>

    <div class="controls">
      <button class="btn music-btn" id="toggleMusic" title="Phát / Tắt nhạc">▶</button>
    </div>
  </div>

  <!-- background music (replace src with your file) -->
  <audio id="bgm" loop>
    <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_d3d6c3a1df.mp3?filename=romantic-background-140079.mp3" type="audio/mpeg">
    Trình duyệt của bạn không hỗ trợ thẻ audio.
  </audio>

  <script>
    // music control
    const bgm = document.getElementById('bgm');
    const btn = document.getElementById('toggleMusic');
    let playing = false;
    btn.addEventListener('click', ()=>{
      if(!playing){
        bgm.play().catch(()=>{});
        btn.textContent = '⏸';
        playing = true;
      } else {
        bgm.pause();
        btn.textContent = '▶';
        playing = false;
      }
    });

    // auto full screen ngay khi tải
    window.addEventListener('load', async ()=>{
      try{
        if(!document.fullscreenElement) await document.documentElement.requestFullscreen();
      }catch(e){console.log('Không thể tự động full màn hình:', e.message)}
    });

    // generate flowers
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
