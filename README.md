* {
  box-sizing: border-box;
}

:root {
  --bg: #120d0a;
  --bg-soft: #1c1512;
  --panel: rgba(255,255,255,0.03);
  --card: rgba(18, 15, 12, 0.82);
  --text: #f6ebdb;
  --muted: #d8c8b0;
  --primary: #d9b06d;
  --secondary: #b87b4a;
  --gold: #f4d99a;
  --border: rgba(255,255,255,0.08);
  --shadow: 0 20px 45px rgba(0,0,0,0.22);
  --radius: 24px;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  font-family: "Cairo", sans-serif;
  background:
    radial-gradient(circle at top right, rgba(217,176,109,0.14), transparent 22%),
    radial-gradient(circle at bottom left, rgba(184,123,74,0.12), transparent 25%),
    linear-gradient(135deg, var(--bg), #1a1411 50%, #120d0a 100%);
  color: var(--text);
  line-height: 1.9;
}

a {
  color: inherit;
  text-decoration: none;
}

img {
  max-width: 100%;
  display: block;
}

.container {
  width: min(1120px, calc(100% - 32px));
  margin: 0 auto;
}

.site-header {
  position: sticky;
  top: 0;
  z-index: 100;
  background: rgba(18, 13, 10, 0.7);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid var(--border);
}

.nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  min-height: 76px;
  gap: 18px;
}

.brand-wrap {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  font-weight: 800;
}

.brand-mark {
  display: inline-grid;
  place-items: center;
  width: 38px;
  height: 38px;
  border-radius: 12px;
  background: linear-gradient(135deg, var(--primary), var(--secondary));
  color: #1a120b;
  font-size: 1.2rem;
}

.brand-name {
  font-size: 1.08rem;
}

.nav-links {
  display: flex;
  flex-wrap: wrap;
  gap: 18px;
  color: var(--muted);
}

.nav-links a {
  transition: color 0.2s ease;
}

.nav-links a:hover,
.nav-links a:focus-visible {
  color: var(--text);
}

.hero {
  padding: 96px 0 64px;
}

.hero-grid {
  display: grid;
  grid-template-columns: 1.3fr 0.9fr;
  gap: 40px;
  align-items: center;
}

.kicker {
  margin: 0 0 8px;
  color: var(--gold);
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  font-size: 0.75rem;
}

.hero-copy h1 {
  margin: 0;
  font-size: clamp(2.5rem, 5vw, 4.8rem);
  font-weight: 800;
  line-height: 1.15;
}

.hero-copy h2 {
  margin: 14px 0 18px;
  font-size: clamp(1.18rem, 2vw, 1.9rem);
  color: var(--muted);
  font-weight: 600;
}

.lead {
  max-width: 640px;
  margin: 0;
  color: var(--muted);
  font-size: 1.08rem;
}

.actions {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
  margin-top: 28px;
}

.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border-radius: 999px;
  padding: 0.9rem 1.5rem;
  font-weight: 700;
  border: 1px solid transparent;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.btn:hover {
  transform: translateY(-2px);
}

.btn-primary {
  background: linear-gradient(135deg, var(--primary), var(--secondary));
  box-shadow: 0 18px 35px rgba(184,123,74,0.28);
}

.btn-secondary {
  background: transparent;
  border-color: var(--border);
  color: var(--text);
}

.mini-links {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  padding: 0;
  margin: 28px 0 0;
}

.mini-links a {
  display: inline-block;
  padding: 0.6rem 0.9rem;
  border-radius: 999px;
  border: 1px solid var(--border);
  background: rgba(255,255,255,0.02);
  color: var(--muted);
}

.hero-panel {
  display: grid;
  gap: 22px;
}

.profile-box {
  background: linear-gradient(180deg, rgba(255,255,255,0.05), rgba(255,255,255,0.02));
  border: 1px solid var(--border);
  border-radius: 28px;
  padding: 28px 20px 20px;
  box-shadow: var(--shadow);
  text-align: center;
}

.avatar {
  width: 188px;
  height: 188px;
  border-radius: 50%;
  margin: 0 auto 22px;
  display: grid;
  place-items: center;
  background: linear-gradient(135deg, var(--primary), var(--secondary));
  color: #150f0b;
  font-weight: 800;
  font-size: 4rem;
  box-shadow: 0 0 0 12px rgba(217,176,109,0.12);
}

.status-tag {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border-radius: 999px;
  padding: 0.55rem 0.9rem;
  color: var(--gold);
  background: rgba(217,176,109,0.08);
  border: 1px solid rgba(217,176,109,0.16);
  font-weight: 700;
}

.stats {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 14px;
}

.stat-item {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 18px 12px;
  text-align: center;
}

.stat-item strong {
  display: block;
  font-size: 1.5rem;
}

.stat-item span {
  color: var(--muted);
  font-size: 0.8rem;
}

.section {
  padding: 88px 0;
}

.section-alt {
  background: rgba(255,255,255,0.02);
  border-top: 1px solid var(--border);
  border-bottom: 1px solid var(--border);
}

.section-heading {
  margin-bottom: 32px;
}

.section-heading h3 {
  margin: 0;
  font-size: clamp(1.8rem, 3vw, 2.7rem);
}

.about-grid,
.works-grid,
.themes-grid,
.poetry-grid {
  display: grid;
  gap: 22px;
}

.about-grid {
  grid-template-columns: repeat(2, minmax(0, 1fr));
}

.card,
.work-card,
.theme-card,
.article-item,
.cta-box,
.poetry-card {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  box-shadow: var(--shadow);
}

.card {
  padding: 28px 24px;
}

.card p {
  margin: 0;
  color: var(--text);
}

.accent-card {
  background: linear-gradient(135deg, rgba(217,176,109,0.08), rgba(184,123,74,0.06));
}

.works-grid {
  grid-template-columns: repeat(3, minmax(0, 1fr));
}

.work-card,
.theme-card {
  padding: 26px 22px;
}

.tag,
.poetry-tag {
  display: inline-block;
  margin-bottom: 16px;
  padding: 0.42rem 0.8rem;
  border-radius: 999px;
  background: rgba(184,123,74,0.12);
  color: var(--gold);
  border: 1px solid rgba(184,123,74,0.18);
  font-size: 0.72rem;
  font-weight: 700;
}

.work-card h4,
.theme-card h4,
.article-item h4,
.poetry-card h4 {
  margin: 0 0 10px;
  font-size: 1.4rem;
}

.work-card p,
.theme-card p,
.article-item p,
.poetry-card p {
  margin: 0;
  color: var(--muted);
}

.poetry-grid {
  grid-template-columns: repeat(3, minmax(0, 1fr));
}

.poetry-card {
  display: block;
  padding: 22px 20px;
  transition: transform 0.2s ease, border-color 0.2s ease;
}

.poetry-card:hover,
.poetry-card:focus-visible {
  transform: translateY(-3px);
  border-color: rgba(217,176,109,0.28);
}

.themes-grid {
  grid-template-columns: repeat(4, minmax(0, 1fr));
}

.icon {
  width: 52px;
  height: 52px;
  display: grid;
  place-items: center;
  border-radius: 14px;
  background: rgba(217,176,109,0.1);
  color: var(--gold);
  font-weight: 800;
  margin-bottom: 18px;
}

.articles-list {
  display: grid;
  gap: 18px;
}

.article-item {
  display: grid;
  grid-template-columns: 110px 1fr;
  gap: 16px;
  padding: 20px 22px;
}

.article-date {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-height: 54px;
  background: rgba(217,176,109,0.1);
  border: 1px solid rgba(217,176,109,0.14);
  border-radius: 14px;
  color: var(--gold);
  font-weight: 800;
}

.cta-section {
  padding-bottom: 100px;
}

.cta-box {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 22px;
  padding: 28px 24px;
  background: linear-gradient(135deg, rgba(217,176,109,0.1), rgba(184,123,74,0.08));
}

.cta-box h3 {
  margin: 0;
  font-size: clamp(1.6rem, 3vw, 2.4rem);
}

.contact-links {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
}

.contact-links a {
  border: 1px solid var(--border);
  background: rgba(255,255,255,0.02);
  border-radius: 999px;
  padding: 0.75rem 1rem;
  color: var(--muted);
}

.site-footer {
  padding: 28px 0 42px;
  color: var(--muted);
  text-align: center;
  border-top: 1px solid var(--border);
}

@media (max-width: 980px) {
  .hero-grid,
  .about-grid,
  .works-grid,
  .themes-grid,
  .poetry-grid,
  .cta-box {
    grid-template-columns: 1fr;
    display: grid;
  }

  .nav {
    flex-direction: column;
    justify-content: center;
    padding: 14px 0;
  }
}

@media (max-width: 620px) {
  .stats,
  .works-grid,
  .themes-grid,
  .about-grid,
  .poetry-grid {
    grid-template-columns: 1fr;
  }

  .article-item {
    grid-template-columns: 1fr;
  }

  .nav-links {
    justify-content: center;
    gap: 10px 14px;
    font-size: 0.92rem;
  }

  .hero {
    padding-top: 72px;
  }
}

