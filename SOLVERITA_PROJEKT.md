# 🚀 Solverita Web – Projektový plán

> **Cíl:** Prezentační web s portfoliem a lead generation  
> **Stack:** HTML/Tailwind → Astro  
> **Stav:** Fáze 1-2 rozpracováno

---

## 📊 Přehled fází

| Fáze | Název | Stav | Poznámky |
|------|-------|------|----------|
| 1 | Analýza & Audit | ✅ Hotovo | HTML struktura OK |
| 2 | Opravy & Funkčnost | 🔄 Probíhá | Hamburger ✅, Case Studies ✅ |
| 3 | Obsah & Copy | ⏳ Čeká | Texty, vlastní fotky |
| 4 | HTML Finalizace | ⏳ Čeká | Formulář, accessibility |
| 5 | Migrace → Astro | ⏳ Čeká | Komponenty, routing |
| 6 | Deploy & CMS | ⏳ Čeká | Hosting, doména |

---

## ✅ Fáze 2: Opravy & Funkčnost

### Hotovo
- [x] Hamburger menu – plně funkční s animací ☰ → ✕
- [x] Case Studies navigace – onclick funguje správně
- [x] Mobilní menu – overlay, blur, ESC zavírání

### K dodělání
- [ ] Kontaktní formulář – validace + odesílání
- [ ] Lazy loading obrázků
- [ ] Scroll spy pro aktivní menu položku
- [ ] Smooth scroll na všechny anchor linky

---

## ⏳ Fáze 3: Obsah & Copy

### Texty
- [ ] Zkontrolovat všechny case studies – jsou kompletní?
- [ ] SEO meta tagy (title, description, OG tags)
- [ ] Strukturovaná data (JSON-LD pro firmu)

### Vizuály
- [ ] Nahradit Unsplash placeholdery vlastními fotkami
- [ ] Logo v SVG formátu (ne PNG)
- [ ] Favicon set (ico, apple-touch-icon, etc.)

---

## ⏳ Fáze 4: HTML Finalizace

### Funkčnost
- [ ] Kontaktní formulář s validací
- [ ] Integrace s email službou (Formspree / Netlify Forms)
- [ ] Cookie consent banner
- [ ] 404 stránka

### Accessibility (a11y)
- [ ] ARIA labels na interaktivních prvcích
- [ ] Focus states pro keyboard navigaci
- [ ] Skip to content link
- [ ] Alt texty na všech obrázcích

### Performance
- [ ] Optimalizace obrázků (WebP, srcset)
- [ ] Minifikace CSS/JS
- [ ] Preload kritických fontů

---

## ⏳ Fáze 5: Migrace do Astro

### Struktura projektu
```
solverita-web/
├── src/
│   ├── components/
│   │   ├── Nav.astro
│   │   ├── Footer.astro
│   │   ├── ServiceCard.astro
│   │   ├── CaseStudyCard.astro
│   │   └── ContactForm.astro
│   ├── layouts/
│   │   └── BaseLayout.astro
│   ├── pages/
│   │   ├── index.astro
│   │   ├── case-studies/
│   │   │   ├── proxmox.astro
│   │   │   ├── videokonference.astro
│   │   │   └── it-sprava.astro
│   │   └── 404.astro
│   └── styles/
│       └── global.css
├── public/
│   ├── images/
│   └── fonts/
├── astro.config.mjs
└── package.json
```

### Kroky migrace
- [ ] `npm create astro@latest solverita-web`
- [ ] Přenést globální styly
- [ ] Vytvořit BaseLayout s nav + footer
- [ ] Rozdělit sekce do komponent
- [ ] Case studies jako samostatné stránky (ne SPA)
- [ ] Nastavit Tailwind v Astro

---

## ⏳ Fáze 6: Deploy & CMS

### Hosting (vybrat jeden)
- [ ] Vercel – nejjednodušší pro Astro
- [ ] Netlify – forms zdarma
- [ ] Cloudflare Pages – rychlé CDN

### Volitelně: CMS
- [ ] Keystatic (lokální, git-based)
- [ ] Decap CMS (bývalý Netlify CMS)
- [ ] Contentful / Sanity (headless)

---

## 🎨 Design systém (připraveno)

### Barvy
```css
--primary: #00ea9a;      /* Zelená */
--secondary: #00a9ff;    /* Modrá */
--bg-dark: #0f172a;      /* Pozadí */
--glass-bg: rgba(255, 255, 255, 0.03);
--glass-border: rgba(255, 255, 255, 0.1);
```

### Typografie
- **Headings:** Lexend Deca (700, 400)
- **Body:** Space Grotesk (300, 500, 700)

### Komponenty
- Glass cards (backdrop-blur)
- Gradient buttons
- Service cards s hover efektem
- Portfolio lightbox

---

## 📝 Poznámky z konverzace

### Co funguje
- SPA-style navigace mezi home a case studies
- Responzivní layout (mobile-first)
- Glassmorphism design konzistentní
- Lightbox pro portfolio fotky

### Co vylepšit
- Některé case studies nejsou úplně dokončené
- Placeholder obrázky z Unsplash
- Kontaktní formulář je jen simulace

---

## 🔗 Soubory

| Soubor | Popis |
|--------|-------|
| `index.html` | Hlavní HTML (aktuální verze) |
| `SOLVERITA_PROJEKT.md` | Tento projektový plán |

---

*Poslední aktualizace: Dnes*  
*Další krok: Kontaktní formulář nebo příprava na Astro?*
