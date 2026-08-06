*,
*::before,
*::after {
  box-sizing: border-box;
}
:root {
  --bg: #f7f4ef;
  --bg-alt: #ede8df;
  --surface: #ffffff;
  --text: #1a1714;
  --text-muted: #5c564e;
  --accent: #c45c26;
  --accent-hover: #a34a1c;
  --border: rgba(26, 23, 20, 0.08);
  --shadow: 0 24px 60px rgba(26, 23, 20, 0.08);
  --radius: 18px;
  --font-sans: "DM Sans", system-ui, sans-serif;
  --font-serif: "Instrument Serif", Georgia, serif;
  --max-width: 1100px;
  --header-height: 72px;
}
html {
  scroll-behavior: smooth;
}
body {
  margin: 0;
  font-family: var(--font-sans);
  font-size: 1rem;
  line-height: 1.6;
  color: var(--text);
  background: var(--bg);
}
a {
  color: inherit;
  text-decoration: none;
}
img {
  max-width: 100%;
  display: block;
}
.site-header {
  position: sticky;
  top: 0;
  z-index: 100;
  backdrop-filter: blur(12px);
  background: rgba(247, 244, 239, 0.85);
  border-bottom: 1px solid var(--border);
}
.nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 1.5rem;
  height: var(--header-height);
}
.nav__logo {
  display: inline-flex;
  align-items: center;
  gap: 0.65rem;
  font-weight: 700;
  letter-spacing: -0.02em;
}
.nav__logo img {
  width: 36px;
  height: 36px;
  border-radius: 8px;
  object-fit: cover;
}
.nav__menu {
  display: flex;
  gap: 2rem;
  list-style: none;
  margin: 0;
  padding: 0;
}
.nav__menu a {
  color: var(--text-muted);
  font-size: 0.95rem;
  transition: color 0.2s ease;
}
.nav__menu a:hover,
.nav__menu a:focus-visible {
  color: var(--accent);
}
.nav__toggle {
  display: none;
  flex-direction: column;
  justify-content: center;
  gap: 6px;
  width: 44px;
  height: 44px;
  padding: 0;
  border: 0;
  background: transparent;
  cursor: pointer;
}
.nav__toggle span {
  display: block;
  width: 22px;
  height: 2px;
  margin: 0 auto;
  background: var(--text);
  transition: transform 0.25s ease, opacity 0.25s ease;
}
.hero {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr;
  align-items: center;
  gap: 3rem;
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 5rem 1.5rem 4rem;
  min-height: calc(100vh - var(--header-height));
}
.hero__eyebrow {
  margin: 0 0 0.75rem;
  font-size: 0.95rem;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  color: var(--accent);
}
.hero__title {
  margin: 0;
  font-family: var(--font-serif);
  font-size: clamp(3rem, 8vw, 5.5rem);
  font-weight: 400;
  line-height: 1.05;
  letter-spacing: -0.03em;
}
.hero__subtitle {
  max-width: 34rem;
  margin: 1.5rem 0 0;
  font-size: 1.15rem;
  color: var(--text-muted);
}
.hero__actions {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  margin-top: 2.5rem;
}
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-height: 48px;
  padding: 0 1.5rem;
  border-radius: 999px;
  font-weight: 500;
  transition: transform 0.2s ease, background 0.2s ease, color 0.2s ease;
}
.btn:hover {
  transform: translateY(-2px);
}
.btn--primary {
  background: var(--accent);
  color: #fff;
}
.btn--primary:hover {
  background: var(--accent-hover);
}
.btn--ghost {
  border: 1px solid var(--border);
  background: var(--surface);
}
.hero__visual {
  display: flex;
  justify-content: center;
}
.avatar {
  display: grid;
  place-items: center;
  width: min(100%, 320px);
  aspect-ratio: 1;
  border-radius: 50%;
  overflow: hidden;
  background:
    radial-gradient(circle at 30% 30%, rgba(255, 255, 255, 0.35), transparent 55%),
    linear-gradient(145deg, #d9773f, #8b3a12);
  box-shadow: var(--shadow);
}
.avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.avatar__fallback {
  font-family: var(--font-serif);
  font-size: 4rem;
  color: rgba(255, 255, 255, 0.92);
}
.section {
  padding: 5rem 1.5rem;
