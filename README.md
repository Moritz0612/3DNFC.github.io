# 3DNFC.github.io
A website to try things out
<!doctype html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>NFS-Tags — NextGen Digital Tags</title>
  <meta name="description" content="NFS-Tags: exklusive, sammelbare digitale Tags im futuristischen Design." />
  <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 32 32%22><circle cx=%2216%22 cy=%2216%22 r=%2214%22 fill=%22%23333%22/></svg>">

  <style>
    :root{
      --bg:#0f1115;
      --muted: rgba(255,255,255,0.6);
      --accent1: linear-gradient(135deg,#7ee7ff 0%, #7b61ff 100%);
      --glass-border: rgba(255,255,255,0.06);
      --radius: 12px;
      font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial;
      color:#e9eef8;
      background:
        radial-gradient(1200px 600px at 10% 10%, rgba(123,97,255,0.06), transparent 6%),
        radial-gradient(900px 450px at 90% 90%, rgba(126,231,255,0.03), transparent 6%),
        var(--bg);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
    }
    *{box-sizing:border-box}
    html,body{height:100%;margin:0}
    a{color:inherit;text-decoration:none}
    button{font:inherit;cursor:pointer}
    .container{max-width:1100px;margin:36px auto;padding:20px;display:grid;gap:20px}
    header{display:flex;align-items:center;justify-content:space-between;gap:16px}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{width:56px;height:56px;border-radius:12px;background:var(--accent1);display:grid;place-items:center;color:#031022;font-weight:700}
    nav{display:flex;gap:10px;align-items:center}
    .nav-link{padding:8px 10px;border-radius:10px;color:var(--muted);font-size:14px}
    .cta{background:linear-gradient(90deg,#6bd6ff,#8b63ff);padding:10px 14px;border-radius:12px;color:#021022;font-weight:700;border:0}

    .hero{display:grid;grid-template-columns:1fr 420px;gap:20px;padding:20px;border-radius:14px;border:1px solid var(--glass-border);background:rgba(255,255,255,0.02)}
    .hero h1{margin:0;font-size:28px}
    .hero p{color:var(--muted);margin:12px 0 0 0}

    .products{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);padding:14px;border-radius:12px;border:1px solid var(--glass-border);display:flex;flex-direction:column;justify-content:space-between;min-height:320px}
    .art{height:150px;border-radius:8px;background:rgba(255,255,255,0.02);display:grid;place-items:center;border:1px solid rgba(255,255,255,0.03)}

    footer{display:flex;justify-content:space-between;align-items:center;color:var(--muted);padding:12px;border-top:1px solid rgba(255,255,255,0.02)}

    .overlay{position:fixed;inset:0;background:rgba(2,6,23,0.6);display:none;align-items:center;justify-content:center;padding:20px;z-index:90}
    .modal{width:100%;max-width:720px;background:#071017;padding:18px;border-radius:12px;border:1px solid rgba(255,255,255,0.04)}
    .close{background:transparent;border:1px solid rgba(255,255,255,0.03);padding:6px 8px;border-radius:8px;color:var(--muted)}

    @media (max-width:1000px){ .hero{grid-template-columns:1fr} .products{grid-template-columns:repeat(2,1fr)} }
    @media (max-width:640px){ .products{grid-template-columns:1fr} .logo{width:44px;height:44px} }
    .muted{color:var(--muted);font-size:13px}
    .price{font-weight:700;font-size:18px}
  </style>
</head>
<body>
  <main class="container" role="main">
    <header>
      <div class="brand">
        <div class="logo">NFS</div>
        <div>
          <div style="font-weight:700">NFS-Tags</div>
          <div class="muted" style="font-size:13px">Limitierte digitale Sammler-Tags</div>
        </div>
      </div>

      <nav aria-label="Hauptnavigation">
        <a class="nav-link" href="#catalog">Kollektion</a>
        <a class="nav-link" href="#about">Über</a>
        <button class="cta" id="openCart">Warenkorb</button>
      </nav>
    </header>

    <section class="hero" aria-labelledby="hero-title">
      <div>
        <h1 id="hero-title">NFS-Tags — Design trifft Blockchain</h1>
        <p>Limitierte, sammelbare digitale Tags im futuristischen Look. Jede Edition ist einzigartig und verifizierbar.</p>
        <div style="margin-top:14px;display:flex;gap:10px">
          <button class="cta" id="viewCatalog">Kollektion ansehen</button>
          <button style="background:transparent;border:1px solid var(--glass-border);padding:10px 12px;border-radius:10px;color:var(--muted)">Wie funktioniert's?</button>
        </div>
        <div style="margin-top:12px;display:flex;gap:8px;flex-wrap:wrap">
          <div style="padding:8px;border-radius:999px;background:rgba(255,255,255,0.02);border:1px solid rgba(255,255,255,0.03)">Mint: 0.02 ETH</div>
          <div style="padding:8px;border-radius:999px;background:rgba(255,255,255,0.02);border:1px solid rgba(255,255,255,0.03)">Limit: 150</div>
        </div>
      </div>

      <aside style="display:flex;flex-direction:column;align-items:center;gap:10px">
        <div style="width:320px;height:220px;border-radius:12px;background:linear-gradient(135deg,rgba(126,231,255,0.04),rgba(123,97,255,0.04));display:grid;place-items:center;border:1px solid rgba(255,255,255,0.03)">
          <svg width="60%" viewBox="0 0 200 120" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
            <defs><linearGradient id="g1" x1="0" x2="1"><stop offset="0" stop-color="#7ee7ff"/><stop offset="1" stop-color="#7b61ff"/></linearGradient></defs>
            <rect x="8" y="14" rx="12" ry="12" width="184" height="92" fill="url(#g1)" opacity="0.12"/>
            <g fill="#e9f6ff" transform="translate(14,22)"><rect width="172" height="76" rx="10" fill="rgba(255,255,255,0.02)"/><circle cx="28" cy="38" r="18" fill="url(#g1)"/></g>
          </svg>
        </div>
        <div class="muted" style="font-size:12px">Demo-Vorschau • Kein echtes Minting</div>
      </aside>
    </section>

    <section id="catalog">
      <h2 style="margin:6px 0 12px 0">Aktuelle Editionen</h2>
      <div class="products" id="productList"></div>
    </section>

    <footer>
      <div>
        <div style="font-weight:700">NFS-Tags</div>
        <div class="muted">© <span id="year"></span> NFS-Tags</div>
      </div>
      <div class="muted" style="font-size:13px">Demo • Keine echte Zahlung</div>
    </footer>
  </main>

  <div class="overlay" id="overlay" aria-hidden="true" role="dialog" aria-modal="true">
    <div class="modal" role="document" aria-labelledby="modalTitle">
      <div style="display:flex;align-items:center;gap:12px">
        <h3 id="modalTitle" style="margin:0">Details</h3>
        <button class="close" id="closeOverlay" aria-label="Schließen">✕</button>
      </div>
      <div id="modalBody" style="margin-top:12px"></div>
      <div style="margin-top:14px;display:flex;gap:10px;justify-content:flex-end">
        <button class="close" id="modalBack">Zurück</button>
        <button class="cta" id="modalBuy">Jetzt kaufen</button>
      </div>
    </div>
  </div>

  <script>
    const products = [
      { id: 'NT-001', name: 'Aurora Tag', priceEUR: 32, priceETH: 0.02, desc: 'Holographisches Gradient-Motiv. Limit 120', color: '#7ee7ff' },
      { id: 'NT-002', name: 'Obsidian Tag', priceEUR: 56, priceETH: 0.035, desc: 'Dunkles, poliertes Finish. Limit 75', color: '#7b61ff' },
      { id: 'NT-003', name: 'Pulse Tag', priceEUR: 28, priceETH: 0.018, desc: 'Neonlinien, dynamische Optik. Limit 200', color: '#9ef3c1' },
    ];

    const list = document.getElementById('productList');
    products.forEach(p => {
      const card = document.createElement('article');
      card.className = 'card';
      card.innerHTML = `
        <div>
          <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:8px">
            <span style="font-size:12px;color:var(--muted);padding:6px;border-radius:999px;background:rgba(255,255,255,0.02)">${p.id}</span>
            <div style="color:var(--muted);font-size:13px">${p.priceETH} ETH</div>
          </div>
          <div class="art" aria-hidden="true">
            <svg width="70%" viewBox="0 0 120 90" xmlns="http://www.w3.org/2000/svg">
              <rect x="6" y="8" rx="8" width="108" height="74" fill="${p.color}" opacity="0.14"/>
            </svg>
          </div>
        </div>
        <div>
          <div style="display:flex;justify-content:space-between;align-items:flex-end">
            <div>
              <div style="font-weight:700">${p.name}</div>
              <div class="muted" style="font-size:13px">${p.desc}</div>
            </div>
            <div style="text-align:right">
              <div class="price">${p.priceEUR} €</div>
            </div>
          </div>
          <div style="margin-top:10px;display:flex;gap:8px;justify-content:space-between">
            <button style="background:transparent;border:1px solid var(--glass-border);padding:8px 10px;border-radius:10px;color:var(--muted)" onclick="showDetails('${p.id}')">Details</button>
            <button class="cta" onclick="addToCart('${p.id}')">In den Warenkorb</button>
          </div>
        </div>
      `;
      list.appendChild(card);
    });

    const overlay = document.getElementById('overlay');
    const modalBody = document.getElementById('modalBody');
    const yearEl = document.getElementById('year');
    yearEl.textContent = new Date().getFullYear();

    function showDetails(id){
      const p = products.find(x => x.id === id);
      modalBody.innerHTML = `
        <div style="display:flex;gap:12px;align-items:center">
          <div style="width:140px;height:100px;border-radius:8px;background:${p.color};opacity:0.16"></div>
          <div>
            <h4 style="margin:0">${p.name} <span style="color:var(--muted);font-size:13px">${p.id}</span></h4>
            <p class="muted" style="margin:8px 0">${p.desc}</p>
            <div style="display:flex;gap:8px;align-items:center"><div style="font-weight:700">${p.priceEUR} €</div><div class="muted">${p.priceETH} ETH</div></div>
          </div>
        </div>
      `;
      overlay.style.display = 'flex';
      overlay.setAttribute('aria-hidden', 'false');
    }

    function closeOverlay(){
      overlay.style.display = 'none';
      overlay.setAttribute('aria-hidden', 'true');
    }

    document.getElementById('closeOverlay').addEventListener('click', closeOverlay);
    document.getElementById('modalBack').addEventListener('click', closeOverlay);
    document.getElementById('openCart').addEventListener('click', () => {
      const listHtml = products.map(p => `<li>${p.name} — ${p.priceEUR} €</li>`).join('');
      modalBody.innerHTML = `<h4 style="margin-top:0">Warenkorb</h4><ul style="padding-left:16px">${listHtml}</ul>`;
      overlay.style.display = 'flex';
      overlay.setAttribute('aria-hidden', 'false');
    });

    function addToCart(id){
      alert('Demo: ' + id + ' zum Warenkorb hinzugefügt.');
    }

    overlay.addEventListener('click', (e) => {
      if (e.target === overlay) closeOverlay();
    });
    window.addEventListener('keydown', (e) => {
      if (e.key === 'Escape') closeOverlay();
    });

    document.getElementById('viewCatalog').addEventListener('click', () => {
      document.getElementById('catalog').scrollIntoView({behavior: 'smooth'});
    });
  </script>
</body>
</html>
