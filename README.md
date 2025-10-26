
<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Kelas 92 — kelas paling awkoawkoawko</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#07060a;
      --card-bg: rgba(255,255,255,0.04);
      --glass: rgba(255,255,255,0.06);
      --accent: rgba(255,255,255,0.12);
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:"Poppins",system-ui,-apple-system,Segoe UI,Roboto,"Helvetica Neue",Arial;
      background: linear-gradient(180deg,#050406 0%, #0a0a12 100%);
      color:#e9eef8;
      overflow:hidden;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
    }

    /* Background lights */
    .lights-wrap{
      position:fixed;
      inset:0;
      pointer-events:none;
      z-index:0;
      overflow:hidden;
      mix-blend-mode: normal;
    }
    .light{
      position:absolute;
      width:40vmax;
      height:40vmax;
      filter: blur(120px) saturate(140%);
      opacity:.9;
      border-radius:50%;
      mix-blend-mode: screen;
      animation: float 18s ease-in-out infinite alternate;
      transform-origin:center;
      will-change:transform, filter;
    }
    .light.purple{ background: radial-gradient(circle at 30% 30%, rgba(179, 67, 255,0.95) 0%, rgba(98, 45, 196,0.7) 25%, transparent 50%); left:-10%; top:-15%; animation-duration:22s;}
    .light.blue  { background: radial-gradient(circle at 40% 40%, rgba(90,180,255,0.95) 0%, rgba(40,120,255,0.7) 25%, transparent 50%); right:-12%; top:5%; animation-duration:20s; }
    .light.red   { background: radial-gradient(circle at 60% 40%, rgba(255,100,120,0.95) 0%, rgba(220,40,60,0.7) 25%, transparent 50%); left:10%; bottom:-10%; animation-duration:24s; }
    .light.green { background: radial-gradient(circle at 60% 60%, rgba(120,255,160,0.95) 0%, rgba(20,200,100,0.7) 25%, transparent 50%); right:8%; bottom:-18%; animation-duration:26s; }

    @keyframes float{
      0%{ transform: translate3d(0,0,0) scale(1); filter: blur(120px) saturate(120%); }
      50%{ transform: translate3d(6vw,-4vh,0) scale(1.08); filter: blur(100px) saturate(160%); }
      100%{ transform: translate3d(-6vw,6vh,0) scale(.96); filter: blur(140px) saturate(140%); }
    }

    /* Main content */
    .wrap{
      position:relative;
      z-index:2;
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:48px;
    }

    .card{
      width:100%;
      max-width:980px;
      padding:48px;
      border-radius:18px;
      background: linear-gradient(135deg, rgba(255,255,255,0.02), rgba(255,255,255,0.015));
      box-shadow: 0 10px 40px rgba(3,6,12,0.6), inset 0 1px 0 rgba(255,255,255,0.02);
      backdrop-filter: blur(6px) saturate(110%);
      border: 1px solid rgba(255,255,255,0.03);
      display:flex;
      gap:28px;
      align-items:center;
      flex-wrap:wrap;
    }

    .hero{
      flex:1 1 420px;
    }

    /* Glowing translucent blurred text */
    .title{
      font-size: clamp(36px, 6.6vw, 72px);
      line-height: .95;
      margin:0 0 12px 0;
      font-weight:800;
      position:relative;
      letter-spacing: -.02em;
      color: rgba(255,255,255,0.92);
      -webkit-font-smoothing:antialiased;
    }

    /* duplicate pseudo glow behind text for blurred white shine */
    .title::after{
      content:attr(data-text);
      position:absolute;
      left:0; top:0;
      z-index:-1;
      color: rgba(255,255,255,0.65);
      filter: blur(10px) saturate(120%);
      transform: translateZ(0) scale(1.02);
      opacity:0.7;
      width:100%;
      pointer-events:none;
    }

    /* animated white shine sweep */
    .title::before{
      content:"";
      position:absolute;
      inset:0;
      z-index:3;
      background: linear-gradient(120deg, rgba(255,255,255,0) 0%, rgba(255,255,255,0.45) 50%, rgba(255,255,255,0) 100%);
      transform: translateX(-120%) skewX(-12deg);
      mix-blend-mode: overlay;
      opacity:.85;
      animation: shine 4.5s ease-in-out infinite;
      pointer-events:none;
    }

    @keyframes shine{
      0%{ transform: translateX(-120%) skewX(-12deg); opacity:0; }
      20%{ opacity:.7; }
      50%{ transform: translateX(120%) skewX(-12deg); opacity:1; }
      80%{ opacity:.6; }
      100%{ transform: translateX(120%) skewX(-12deg); opacity:0; }
    }

    .subtitle{
      margin:0 0 22px 0;
      color: rgba(255,255,255,0.7);
      font-weight:300;
      max-width:70ch;
      font-size:clamp(14px,1.8vw,18px);
    }

    .meta{
      display:flex;
      gap:12px;
      align-items:center;
      flex-wrap:wrap;
    }
    .badge{
      padding:8px 14px;
      background: linear-gradient(90deg, rgba(255,255,255,0.03), rgba(255,255,255,0.02));
      border-radius:999px;
      color: rgba(255,255,255,0.9);
      font-weight:600;
      font-size:13px;
      letter-spacing:.02em;
      border:1px solid rgba(255,255,255,0.04);
      backdrop-filter: blur(6px);
    }

    /* right column example */
    .aside{
      width:300px;
      min-width:220px;
      padding:18px;
      border-radius:12px;
      background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border:1px solid rgba(255,255,255,0.03);
      box-shadow: 0 8px 30px rgba(3,6,12,0.55);
      backdrop-filter: blur(6px);
    }
    .list{ margin:0; padding:0; list-style:none; display:flex; flex-direction:column; gap:10px;}
    .list li{
      padding:10px 12px;
      border-radius:10px;
      background: rgba(255,255,255,0.02);
      font-weight:600;
      color:rgba(255,255,255,0.9);
      border:1px solid rgba(255,255,255,0.02);
    }

    /* responsive */
    @media (max-width:760px){
      .card{ padding:28px; gap:18px; }
      .aside{ width:100%; min-width:unset; order:2; }
      .hero{ order:1; }
    }

    /* reduce motion preference */
    @media (prefers-reduced-motion: reduce){
      .light{ animation: none; }
      .title::before{ animation: none; opacity: .8; }
    }
  </style>
</head>
<body>
  <div class="lights-wrap" aria-hidden="true">
    <div class="light purple"></div>
    <div class="light blue"></div>
    <div class="light red"></div>
    <div class="light green"></div>
  </div>

  <div class="wrap">
    <main class="card" role="main">
      <section class="hero">
        <h1 class="title" data-text="KELAS 92">KELAS 92</h1>
        <p class="subtitle">Selamat datang di web kelas 92 yang keren kwkwk,kelas ini tuh yahh paling kalem lah menurut pembuat web ini kwkwk
            banyak yang cantik ganteng behh seru deh kwkwk, kadang ngeselin tapi yahh begitu lah kelas 92.
            onex.mix</p>
        <div class="meta">
          <span class="badge">2025.</span>
          <span class="badge">pembuat web:si F lah• akwoakwoakeo</span>
          <span class="badge">Kontak • kelas92,smp muhammadiyah 37.id</span>
        </div>
      </section>

      <aside class="aside" aria-labelledby="aside-title">
        <h3 id="aside-title" style="margin:0 0 12px 0; font-size:16px; font-weight:700; color:rgba(255,255,255,0.95)">Agenda Mendatang</h3>
        <ul class="list">
          <li>kapan jalan jalan? — gak tau kwkwk</li>
          <li>kapan makan makan nya? — gak tau kwkwk</li>
          <li>yuk ah kita bangakan 92 — gaskun</li>
        </ul>
      </aside>
    </main>
  </div>
</body>
</html>
