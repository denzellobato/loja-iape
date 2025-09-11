<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Discover — Wireframe convertido em HTML/CSS</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">
  <style>
    /* Variáveis e reset */
    :root{
      --bg: #ffffff;
      --muted: #f3f4f6;
      --text: #111827;
      --accent: #111827;
      --radius: 18px; /* tudo arredondado */
      --radius-sm: 12px;
      --container: 1100px;
      --gap: 24px;
      font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
    }
    *{box-sizing:border-box}
    html,body{height:100%;margin:0;background:var(--bg);color:var(--text);}
    a{color:inherit;text-decoration:none}

    /* layout central */
    .wrap{max-width:var(--container);margin:30px auto;padding:32px}

    /* header */
    header{display:flex;align-items:center;justify-content:space-between;gap:16px;padding:8px 0}
    .logo{font-weight:800;font-size:20px}
    nav{display:flex;gap:18px;align-items:center}
    nav a{font-size:14px;padding:8px;border-radius:999px}
    .btn{background:#111827;color:#fff;padding:10px 16px;border-radius:999px;font-weight:600}

    /* hero */
    .hero{display:grid;grid-template-columns:1fr 420px;gap:40px;align-items:start;margin-top:18px}
    .hero .content h1{font-size:44px;line-height:1.02;margin:0 0 12px}
    .hero .content p{color:#374151;margin:0 0 18px}
    .hero .content .cta{display:inline-block;padding:12px 18px;border-radius:999px;background:#111827;color:#fff;font-weight:600}

    /* cards area on right of hero */
    .hero-right{display:flex;flex-direction:column;gap:14px;align-items:flex-end}
    .stack{display:grid;grid-template-columns:1fr;gap:14px}
    .card{background:var(--muted);border-radius:var(--radius);min-height:120px;display:flex;align-items:center;justify-content:center}

    /* Top Destinations */
    .section{margin-top:48px}
    .section h2{font-size:22px;margin:0 0 12px}
    .chips{display:flex;gap:10px;flex-wrap:wrap;margin-bottom:18px}
    .chip{padding:8px 12px;border-radius:999px;border:1px solid #e6e7eb;font-size:13px}

    .dest-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:18px}
    .dest{background:var(--muted);border-radius:var(--radius);padding:10px}
    .dest .thumb{height:160px;border-radius:var(--radius-sm);background:linear-gradient(135deg,#e9ecef,#f8fafc);display:flex;align-items:center;justify-content:center}
    .dest p{font-size:13px;margin:8px 0 0}

    /* Latest Stories */
    .stories{display:grid;grid-template-columns:1fr 320px;gap:20px}
    .story-large{background:var(--muted);padding:16px;border-radius:var(--radius)}
    .story-list{display:flex;flex-direction:column;gap:12px}
    .story-row{display:flex;gap:12px;align-items:center}
    .story-row .s-thumb{width:64px;height:64px;border-radius:12px;background:linear-gradient(135deg,#f3f4f6,#eef2ff)}

    /* Trekker's Highlights */
    .highlights{display:flex;gap:18px;align-items:flex-start}
    .highlight-text{flex:1}
    .highlight-cards{display:flex;flex-direction:column;gap:12px}

    /* newsletter CTA */
    .newsletter{background:#111827;color:#fff;padding:36px;border-radius:20px;margin-top:40px;text-align:center}
    .newsletter input{padding:12px 16px;border-radius:999px;border:0;margin-right:10px;min-width:320px}
    .newsletter button{padding:12px 20px;border-radius:999px;border:0;background:#fff;color:#111827;font-weight:600}

    footer{margin-top:24px;padding-top:28px;border-top:1px solid #e6e7eb}
    .footer-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:16px}

    /* helpers */
    .muted{color:#6b7280}
    .small{font-size:13px}

    /* make everything with rounded corners (global) */
    img,button,input,select,textarea{border-radius:var(--radius-sm)}

    /* responsive */
    @media (max-width:1000px){
      .hero{grid-template-columns:1fr 320px}
      .dest-grid{grid-template-columns:repeat(2,1fr)}
      .wrap{padding:20px}
    }
    @media (max-width:700px){
      .hero{grid-template-columns:1fr;}
      .hero-right{order:-1;flex-direction:row;justify-content:space-between}
      .stories{grid-template-columns:1fr}
      .footer-grid{grid-template-columns:repeat(2,1fr)}
      .dest-grid{grid-template-columns:repeat(1,1fr)}
    }
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="logo">Logo</div>
      <nav>
        <a href="#">Acomodações</a>
        <a href="#">Guias</a>
        <a href="#">Experiências</a>
        <a href="#">Sobre</a>
        <a class="btn" href="#">Entrar</a>
      </nav>
    </header>

    <main>
      <!-- HERO -->
      <section class="hero">
        <div class="content">
          <h1>Discover the World's Hidden Wonders</h1>
          <p>Histórias, guias e inspirações para você explorar o mundo. Encontre os melhores destinos, roteiros e relatos de viajantes para planejar sua próxima aventura.</p>
          <a class="cta" href="#">Explore hoje</a>

          <!-- Top Destinations preview as part of left column for visual parity with wireframe -->
          <div class="section" style="margin-top:28px">
            <div style="display:flex;justify-content:space-between;align-items:center">
              <h2>Top Destinations</h2>
              <button class="chip">Ver mais destinos</button>
            </div>
            <div class="dest-grid" style="margin-top:12px">
              <div class="dest">
                <div class="thumb">Ponte Golden Gate</div>
                <p class="small muted">Golden Bridge, San Francisco — EUA</p>
              </div>
              <div class="dest">
                <div class="thumb">Dubrovnik</div>
                <p class="small muted">Dubrovnik — Croácia</p>
              </div>
              <div class="dest">
                <div class="thumb">Petra</div>
                <p class="small muted">Petra — Jordânia</p>
              </div>
              <div class="dest">
                <div class="thumb">Sydney</div>
                <p class="small muted">Sydney Harbour Bridge — Austrália</p>
              </div>
            </div>
          </div>

        </div>

        <!-- right column: stack of cards like wireframe -->
        <aside class="hero-right">
          <div class="card" style="height:220px;width:300px">Imagem grande</div>
          <div class="stack" style="width:300px">
            <div class="card" style="height:120px">Card 1</div>
            <div class="card" style="height:120px">Card 2</div>
            <div class="card" style="height:80px">Card 3</div>
          </div>
        </aside>
      </section>

      <!-- LATEST STORIES -->
      <section class="section">
        <h2>Latest Stories</h2>
        <div class="stories">
          <article class="story-large">
            <div style="height:180px;border-radius:12px;background:linear-gradient(135deg,#e9ecef,#f8fafc);display:flex;align-items:center;justify-content:center">Thumbnail</div>
            <h3 style="margin:12px 0 6px">Los Angeles food & drinks guide — 10 coisas para experimentar</h3>
            <p class="muted small">Dicas de restaurantes, bares e mercados locais para aproveitar Los Angeles como um morador.</p>
          </article>

          <aside class="story-list">
            <div class="story-row">
              <div class="s-thumb"></div>
              <div>
                <div style="font-weight:600">15 South London Markets You'll Love</div>
                <div class="small muted">Guias • 4 min</div>
              </div>
            </div>

            <div class="story-row">
              <div class="s-thumb"></div>
              <div>
                <div style="font-weight:600">10 Incredible hotels around the world</div>
                <div class="small muted">Hospedagem • 6 min</div>
              </div>
            </div>

            <div class="story-row">
              <div class="s-thumb"></div>
              <div>
                <div style="font-weight:600">Visiting Chicago on a budget</div>
                <div class="small muted">Viagem • 5 min</div>
              </div>
            </div>
          </aside>
        </div>
      </section>

      <!-- TREKKER HIGHLIGHTS -->
      <section class="section">
        <h2>Trekker's Highlights</h2>
        <div class="highlights">
          <div class="highlight-text">
            <div style="display:flex;gap:12px;align-items:center">
              <div style="width:48px;height:48px;border-radius:999px;background:var(--muted)"></div>
              <div>
                <div style="font-weight:700">Maria Angélica</div>
                <div class="small muted">Mais de 120 publicações</div>
              </div>
            </div>
            <p class="muted" style="margin-top:12px">Uma jornada inesquecível pela Turquia: rotas, dicas culturais e dicas de transporte para explorar o país com segurança e economia.</p>
            <button class="chip" style="margin-top:12px">Ler mais histórias</button>
          </div>

          <div class="highlight-cards">
            <div class="card" style="width:220px;height:140px;display:flex;flex-direction:column;justify-content:center;align-items:center">Imagem / Vídeo</div>
            <div class="card" style="width:220px;height:140px;display:flex;flex-direction:column;justify-content:center;align-items:center">Galeria</div>
          </div>
        </div>
      </section>

      <!-- NEWSLETTER -->
      <section class="newsletter">
        <h3 style="margin:0 0 8px;font-size:20px">Get Your Travel Inspiration Straight to Your Inbox</h3>
        <p class="muted small" style="margin:0 0 18px">Assine e receba histórias, guias e ofertas direto na sua caixa de entrada.</p>
        <div>
          <input type="email" placeholder="seu@email.com" aria-label="Email" />
          <button>Assinar</button>
        </div>
      </section>

    </main>

    <footer>
      <div style="display:flex;justify-content:space-between;align-items:flex-start;gap:20px">
        <div>
          <div class="logo">Logo</div>
          <p class="muted small">Siga-nos</p>
        </div>
        <div class="footer-grid" style="flex:1">
          <div>
            <h4>Sobre</h4>
            <ul class="small muted" style="padding-left:0;list-style:none;margin:8px 0 0">
              <li>Quem somos</li>
              <li>Carreiras</li>
              <li>Contato</li>
            </ul>
          </div>
          <div>
            <h4>Guias</h4>
            <ul class="small muted" style="padding-left:0;list-style:none;margin:8px 0 0">
              <li>Destinos</li>
              <li>Roteiros</li>
              <li>Hospedagem</li>
            </ul>
          </div>
          <div>
            <h4>Legal</h4>
            <ul class="small muted" style="padding-left:0;list-style:none;margin:8px 0 0">
              <li>Termos</li>
              <li>Privacidade</li>
            </ul>
          </div>
        </div>
      </div>
      <div style="margin-top:18px" class="small muted">© 2025 Discover. Todos os direitos reservados.</div>
    </footer>
  </div>
</body>
</html>
