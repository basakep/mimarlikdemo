
<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@300;400&family=Barlow:wght@300;400;500&display=swap');
  
  * { box-sizing: border-box; margin: 0; padding: 0; }
  
  .site {
    font-family: 'Barlow', sans-serif;
    font-weight: 300;
    color: var(--color-text-primary);
    background: var(--color-background-primary);
  }
  
  .nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem 2.5rem;
    border-bottom: 0.5px solid var(--color-border-tertiary);
    position: sticky;
    top: 0;
    background: var(--color-background-primary);
    z-index: 10;
  }
  
  .logo {
    font-family: 'Playfair Display', serif;
    font-size: 18px;
    font-weight: 400;
    letter-spacing: 0.1em;
  }
  
  .nav-links {
    display: flex;
    gap: 2rem;
    list-style: none;
  }
  
  .nav-links a {
    font-size: 12px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    text-decoration: none;
    color: var(--color-text-secondary);
    cursor: pointer;
    transition: color 0.2s;
  }
  
  .nav-links a:hover, .nav-links a.active {
    color: var(--color-text-primary);
  }
  
  .page { display: none; }
  .page.active { display: block; }
  
  /* HERO */
  .hero {
    display: grid;
    grid-template-columns: 1fr 1fr;
    min-height: 420px;
  }
  
  .hero-text {
    padding: 4rem 2.5rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    border-right: 0.5px solid var(--color-border-tertiary);
  }
  
  .hero-eyebrow {
    font-size: 11px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--color-text-secondary);
    margin-bottom: 1.5rem;
  }
  
  .hero-title {
    font-family: 'Playfair Display', serif;
    font-size: 42px;
    font-weight: 300;
    line-height: 1.15;
    margin-bottom: 1.5rem;
  }
  
  .hero-sub {
    font-size: 14px;
    color: var(--color-text-secondary);
    line-height: 1.8;
    max-width: 320px;
    margin-bottom: 2.5rem;
  }
  
  .btn-outline {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 20px;
    border: 0.5px solid var(--color-border-primary);
    font-size: 11px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    cursor: pointer;
    background: transparent;
    color: var(--color-text-primary);
    font-family: 'Barlow', sans-serif;
    transition: background 0.2s;
  }
  
  .btn-outline:hover {
    background: var(--color-background-secondary);
  }
  
  .hero-visual {
    background: var(--color-background-secondary);
    position: relative;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .hero-pattern {
    width: 100%;
    height: 100%;
    position: absolute;
    opacity: 0.06;
  }
  
  .hero-label {
    position: absolute;
    bottom: 1.5rem;
    right: 1.5rem;
    font-size: 11px;
    letter-spacing: 0.1em;
    color: var(--color-text-tertiary);
    text-transform: uppercase;
  }

  .hero-placeholder {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.75rem;
    color: var(--color-text-tertiary);
    font-size: 12px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
  }

  .hero-placeholder i { font-size: 32px; opacity: 0.4; }

  /* STATS */
  .stats {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    border-top: 0.5px solid var(--color-border-tertiary);
  }
  
  .stat {
    padding: 2rem 2.5rem;
    border-right: 0.5px solid var(--color-border-tertiary);
  }
  
  .stat:last-child { border-right: none; }
  
  .stat-number {
    font-family: 'Playfair Display', serif;
    font-size: 36px;
    font-weight: 300;
    line-height: 1;
    margin-bottom: 0.5rem;
  }
  
  .stat-label {
    font-size: 11px;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--color-text-secondary);
  }
  
  /* PROJECTS */
  .section-header {
    padding: 3rem 2.5rem 2rem;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    border-bottom: 0.5px solid var(--color-border-tertiary);
  }
  
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: 28px;
    font-weight: 300;
  }
  
  .section-count {
    font-size: 11px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--color-text-secondary);
  }
  
  .projects-grid {
    display: grid;
    grid-template-columns: 2fr 1fr;
  }
  
  .project-card {
    border-right: 0.5px solid var(--color-border-tertiary);
    border-bottom: 0.5px solid var(--color-border-tertiary);
    cursor: pointer;
    transition: background 0.2s;
  }
  
  .project-card:hover { background: var(--color-background-secondary); }
  .project-card:last-child { border-right: none; }
  
  .project-thumb {
    height: 180px;
    background: var(--color-background-secondary);
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--color-text-tertiary);
    font-size: 11px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    border-bottom: 0.5px solid var(--color-border-tertiary);
    position: relative;
    overflow: hidden;
  }
  
  .project-thumb-lg { height: 220px; }
  
  .thumb-overlay {
    position: absolute;
    inset: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .thumb-overlay i { font-size: 28px; opacity: 0.25; }
  .thumb-overlay span { font-size: 10px; opacity: 0.5; }
  
  .project-info {
    padding: 1.25rem 1.5rem;
  }
  
  .project-type {
    font-size: 10px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--color-text-tertiary);
    margin-bottom: 0.4rem;
  }
  
  .project-name {
    font-size: 15px;
    font-weight: 400;
    margin-bottom: 0.35rem;
  }
  
  .project-location {
    font-size: 12px;
    color: var(--color-text-secondary);
  }
  
  /* ABOUT */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
  
  .about-text {
    padding: 3rem 2.5rem;
    border-right: 0.5px solid var(--color-border-tertiary);
  }
  
  .about-text p {
    font-size: 14px;
    line-height: 1.9;
    color: var(--color-text-secondary);
    margin-top: 1rem;
  }
  
  .about-visual {
    padding: 3rem 2.5rem;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }
  
  .service-item {
    padding-bottom: 1.5rem;
    border-bottom: 0.5px solid var(--color-border-tertiary);
  }
  
  .service-item:last-child { border-bottom: none; }
  
  .service-name {
    font-size: 13px;
    font-weight: 400;
    margin-bottom: 0.3rem;
  }
  
  .service-desc {
    font-size: 12px;
    color: var(--color-text-secondary);
  }
  
  /* CONTACT */
  .contact-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
  
  .contact-info {
    padding: 3rem 2.5rem;
    border-right: 0.5px solid var(--color-border-tertiary);
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }
  
  .contact-item-label {
    font-size: 10px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--color-text-tertiary);
    margin-bottom: 0.4rem;
  }
  
  .contact-item-value {
    font-size: 14px;
    line-height: 1.6;
  }
  
  .contact-form {
    padding: 3rem 2.5rem;
    display: flex;
    flex-direction: column;
    gap: 1.25rem;
  }
  
  .form-group label {
    display: block;
    font-size: 10px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--color-text-secondary);
    margin-bottom: 0.5rem;
  }
  
  .form-group input, .form-group textarea {
    width: 100%;
    padding: 10px 12px;
    border: 0.5px solid var(--color-border-secondary);
    background: var(--color-background-primary);
    color: var(--color-text-primary);
    font-family: 'Barlow', sans-serif;
    font-size: 13px;
    font-weight: 300;
    outline: none;
    transition: border-color 0.2s;
  }
  
  .form-group input:focus, .form-group textarea:focus {
    border-color: var(--color-border-primary);
  }
  
  .form-group textarea { height: 100px; resize: none; }
  
  .footer {
    padding: 2rem 2.5rem;
    border-top: 0.5px solid var(--color-border-tertiary);
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .footer-copy {
    font-size: 11px;
    color: var(--color-text-tertiary);
    letter-spacing: 0.05em;
  }
  
  .footer-logo {
    font-family: 'Playfair Display', serif;
    font-size: 14px;
    font-weight: 300;
    letter-spacing: 0.1em;
  }
</style>

<div class="site">
  <nav class="nav">
    <div class="logo">ARAS MİMARLIK</div>
    <ul class="nav-links">
      <li><a href="#" class="active" onclick="showPage('home', this)">Ana Sayfa</a></li>
      <li><a href="#" onclick="showPage('projects', this)">Projeler</a></li>
      <li><a href="#" onclick="showPage('about', this)">Hakkımızda</a></li>
      <li><a href="#" onclick="showPage('contact', this)">İletişim</a></li>
    </ul>
  </nav>

  <!-- HOME -->
  <div class="page active" id="page-home">
    <div class="hero">
      <div class="hero-text">
        <p class="hero-eyebrow">Mimarlık + İç Mekan Tasarımı</p>
        <h1 class="hero-title">Mekânı<br>yeniden<br>düşünmek.</h1>
        <p class="hero-sub">İnsan odaklı tasarım anlayışıyla, işlevsellik ve estetiği bir arada sunan mimari çözümler üretiyoruz.</p>
        <button class="btn-outline" onclick="showPage('projects', document.querySelectorAll('.nav-links a')[1])">
          Projelerimiz <i class="ti ti-arrow-right" aria-hidden="true"></i>
        </button>
      </div>
      <div class="hero-visual">
        <svg class="hero-pattern" viewBox="0 0 400 420" xmlns="http://www.w3.org/2000/svg">
          <line x1="0" y1="0" x2="400" y2="420" stroke="currentColor" stroke-width="1"/>
          <line x1="80" y1="0" x2="480" y2="420" stroke="currentColor" stroke-width="1"/>
          <line x1="160" y1="0" x2="560" y2="420" stroke="currentColor" stroke-width="1"/>
          <line x1="-80" y1="0" x2="320" y2="420" stroke="currentColor" stroke-width="1"/>
          <line x1="0" y1="0" x2="0" y2="420" stroke="currentColor" stroke-width="0.5"/>
          <line x1="100" y1="0" x2="100" y2="420" stroke="currentColor" stroke-width="0.5"/>
          <line x1="200" y1="0" x2="200" y2="420" stroke="currentColor" stroke-width="0.5"/>
          <line x1="300" y1="0" x2="300" y2="420" stroke="currentColor" stroke-width="0.5"/>
          <line x1="400" y1="0" x2="400" y2="420" stroke="currentColor" stroke-width="0.5"/>
          <line x1="0" y1="105" x2="400" y2="105" stroke="currentColor" stroke-width="0.5"/>
          <line x1="0" y1="210" x2="400" y2="210" stroke="currentColor" stroke-width="0.5"/>
          <line x1="0" y1="315" x2="400" y2="315" stroke="currentColor" stroke-width="0.5"/>
        </svg>
        <div class="hero-placeholder">
          <i class="ti ti-building-community" aria-hidden="true"></i>
          <span>Proje görseli</span>
        </div>
        <span class="hero-label">Ankara, 2024</span>
      </div>
    </div>
    
    <div class="stats">
      <div class="stat">
        <div class="stat-number">18+</div>
        <div class="stat-label">Tamamlanan proje</div>
      </div>
      <div class="stat">
        <div class="stat-number">12</div>
        <div class="stat-label">Yıl deneyim</div>
      </div>
      <div class="stat">
        <div class="stat-number">4</div>
        <div class="stat-label">Ödül</div>
      </div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="page" id="page-projects">
    <div class="section-header">
      <h2 class="section-title">Projeler</h2>
      <span class="section-count">6 çalışma</span>
    </div>
    <div class="projects-grid">
      <div class="project-card">
        <div class="project-thumb project-thumb-lg">
          <div class="thumb-overlay">
            <i class="ti ti-building" aria-hidden="true"></i>
            <span>Konut projesi görseli</span>
          </div>
        </div>
        <div class="project-info">
          <p class="project-type">Konut</p>
          <p class="project-name">Çankaya Residence</p>
          <p class="project-location">Ankara — 2023</p>
        </div>
      </div>
      <div style="display: flex; flex-direction: column;">
        <div class="project-card" style="flex: 1;">
          <div class="project-thumb">
            <div class="thumb-overlay">
              <i class="ti ti-building-store" aria-hidden="true"></i>
              <span>Ofis projesi</span>
            </div>
          </div>
          <div class="project-info">
            <p class="project-type">Ofis</p>
            <p class="project-name">Yıldız Towers</p>
            <p class="project-location">Ankara — 2022</p>
          </div>
        </div>
        <div class="project-card" style="flex: 1; border-right: none;">
          <div class="project-thumb">
            <div class="thumb-overlay">
              <i class="ti ti-school" aria-hidden="true"></i>
              <span>Kültür yapısı</span>
            </div>
          </div>
          <div class="project-info">
            <p class="project-type">Kültür</p>
            <p class="project-name">Kızılay Kültür Merkezi</p>
            <p class="project-location">Ankara — 2021</p>
          </div>
        </div>
      </div>
    </div>
    <div class="projects-grid">
      <div class="project-card">
        <div class="project-thumb">
          <div class="thumb-overlay">
            <i class="ti ti-building-hospital" aria-hidden="true"></i>
            <span>Ticari yapı</span>
          </div>
        </div>
        <div class="project-info">
          <p class="project-type">Ticari</p>
          <p class="project-name">Söğütözü Plaza</p>
          <p class="project-location">Ankara — 2021</p>
        </div>
      </div>
      <div class="project-card" style="border-right: none;">
        <div class="project-thumb">
          <div class="thumb-overlay">
            <i class="ti ti-home" aria-hidden="true"></i>
            <span>Villa projesi</span>
          </div>
        </div>
        <div class="project-info">
          <p class="project-type">Konut</p>
          <p class="project-name">Beysukent Villa</p>
          <p class="project-location">Ankara — 2020</p>
        </div>
      </div>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="page" id="page-about">
    <div class="section-header">
      <h2 class="section-title">Hakkımızda</h2>
    </div>
    <div class="about-grid">
      <div class="about-text">
        <p class="hero-eyebrow">Biz kimiz</p>
        <p>Aras Mimarlık, 2012 yılında Ankara'da kurulmuş bir mimarlık ve iç mekan tasarım ofisidir. Konut, ofis, kültürel yapı ve kentsel dönüşüm projelerinde insan odaklı, sürdürülebilir ve estetik açıdan güçlü tasarımlar üretmekteyiz.</p>
        <p>Her projede işlevsellik, sadelik ve uzun ömürlü estetik değerleri bir arada ele alıyoruz. Tasarım sürecimiz, kullanıcı ihtiyaçları ve yerel bağlamla derinlemesine diyaloğa dayanır.</p>
      </div>
      <div class="about-visual">
        <p style="font-size: 10px; letter-spacing: 0.15em; text-transform: uppercase; color: var(--color-text-tertiary); margin-bottom: 0.5rem;">Hizmetlerimiz</p>
        <div class="service-item">
          <p class="service-name">Mimari Tasarım</p>
          <p class="service-desc">Konseptten uygulamaya tüm proje aşamaları</p>
        </div>
        <div class="service-item">
          <p class="service-name">İç Mekan Tasarımı</p>
          <p class="service-desc">Mekan kimliği ve döşeme projeleri</p>
        </div>
        <div class="service-item">
          <p class="service-name">Proje Yönetimi</p>
          <p class="service-desc">İnşaat süreci denetimi ve koordinasyonu</p>
        </div>
        <div class="service-item">
          <p class="service-name">Danışmanlık</p>
          <p class="service-desc">Fizibilite ve kentsel dönüşüm analizi</p>
        </div>
      </div>
    </div>
  </div>

  <!-- CONTACT -->
  <div class="page" id="page-contact">
    <div class="section-header">
      <h2 class="section-title">İletişim</h2>
    </div>
    <div class="contact-grid">
      <div class="contact-info">
        <div>
          <p class="contact-item-label">Adres</p>
          <p class="contact-item-value">Kızılay Mah. Atatürk Bulvarı 42/5<br>Çankaya, Ankara</p>
        </div>
        <div>
          <p class="contact-item-label">E-posta</p>
          <p class="contact-item-value">info@arasmimarlık.com</p>
        </div>
        <div>
          <p class="contact-item-label">Telefon</p>
          <p class="contact-item-value">+90 312 000 00 00</p>
        </div>
        <div>
          <p class="contact-item-label">Çalışma saatleri</p>
          <p class="contact-item-value">Pzt – Cum, 09:00 – 18:00</p>
        </div>
      </div>
      <div class="contact-form">
        <p style="font-size: 10px; letter-spacing: 0.15em; text-transform: uppercase; color: var(--color-text-tertiary);">Mesaj gönderin</p>
        <div class="form-group">
          <label>Ad Soyad</label>
          <input type="text" placeholder="Adınız" />
        </div>
        <div class="form-group">
          <label>E-posta</label>
          <input type="email" placeholder="ornek@mail.com" />
        </div>
        <div class="form-group">
          <label>Mesajınız</label>
          <textarea placeholder="Projenizi kısaca anlatın..."></textarea>
        </div>
        <button class="btn-outline">Gönder <i class="ti ti-arrow-right" aria-hidden="true"></i></button>
      </div>
    </div>
  </div>

  <footer class="footer">
    <span class="footer-copy">© 2025 Aras Mimarlık. Tüm hakları saklıdır.</span>
    <span class="footer-logo">ARAS</span>
  </footer>
</div>

<script>
function showPage(id, clickedLink) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.nav-links a').forEach(a => a.classList.remove('active'));
  document.getElementById('page-' + id).classList.add('active');
  if (clickedLink) clickedLink.classList.add('active');
  return false;
}
</script>
