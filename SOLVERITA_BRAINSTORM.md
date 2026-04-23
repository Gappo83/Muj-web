# 💭 Brainstorm Solverita Web

> **Účel:** Sbírka myšlenek, nápadů a konceptů pro vývoj webu Solverita  
> **Formát:** Markdown (.md) – upravitelné v jakémkoliv textovém editoru  
> **Status:** Živý dokument – aktualizuje se průběžně

---

## 📋 Obsah
1. [Navigace & Menu](#navigace--menu)
2. [Information Architecture (IA)](#information-architecture-ia)
3. [Content & Copy](#content--copy)
4. [Design & UX](#design--ux)
5. [Technické nápady](#technické-nápady)
6. [Backlog myšlenek](#backlog-myšlenek)

---

## 🗂️ Navigace & Menu

### Problém současného stavu
- Menu je jednoduchý, ale mohl by být lépe strukturován
- Návštěvník neví hned, co je „Co řešíme" vs. „Portfolio"
- Příliš mnoho položek v hlavní navigaci (7 položek)

### Návrh: Hierarchie 3 vrstev
```
Solverita (logo)
├── O nás
│   ├── Náš přístup
│   ├── Tým (v budoucnu)
│   └── Kariéra
├── Naše práce
│   ├── Co řešíme (services)
│   ├── Case Studies
│   └── Portfolio
├── Řešení
│   ├── IT Správa
│   ├── Proxmox VE
│   ├── Videokonference
│   └── ... (jednotlivé služby)
└── Kontakt
```

### Alternativa: Sticky dropdown menu
- Hover na "Naše práce" → slide-down submenu
- Lepší pro desktop, neruší mobile menu
- Ikony vedle jednotlivých položek?

### Mobile menu
- Zachovat hamburger (aktuálně OK)
- Accordion položky místo submenu (expandovat "Naše práce")
- Sticky CTA button "Ozvěte se" dole

---

## 📐 Information Architecture (IA)

### Potenciální URL struktura
```
/ (homepage)
├── /o-nas/                    # O nás, team, values
├── /nase-prace/               # Přehled všech služeb
│   ├── /nase-prace/it-sprava/
│   ├── /nase-prace/proxmox/
│   ├── /nase-prace/videokonference/
│   ├── /nase-prace/wifi/
│   └── ...
├── /case-studies/             # Přehled všech případů
│   ├── /case-studies/proxmox-prumysl/
│   ├── /case-studies/videokonference/
│   └── ...
├── /portfolio/                # Fotogalerie (aktuálně na homepage)
├── /reference/                # Logos klientů (aktuálně na homepage)
└── /kontakt/                  # Kontaktní formulář (aktuálně na homepage)
```

### Pozorování
- Case studies a Services jsou nyní v jednom místě
- Portfolio je jen fotogalerie bez context
- Mohli bychom mít dedikované podstránky

---

## 📝 Content & Copy

### Homepage: 3 hlavní sekce
- **Hero:** Problém → Řešení (aktuálně OK)
- **Why us:** Náš přístup (máme, ale krátké)
- **CTA:** Proč nás vybrat?

### Texty co chybí/mají být lépe
- [ ] O týmu – kdo jsme? (Teď chybí)
- [ ] Procesy – jak pracujeme? (Zmínka v approachu, ale není detailní)
- [ ] Ceny – jsou skryté (OK tak, ale jsou obavy?)
- [ ] FAQ – co se ptáte nejčastěji?

### Blog ideje (budoucnost)
- Technické články: Proxmox tipy, Wi-Fi audit, ...
- Case study deep-dives: Jak jsme vyřešili X
- Industry news: Co se děje v IT

### Messaging
- **Aktuálně:** "Nehrajeme si na buzzwords. Řešíme IT"
- **Silné:** Transparentnost, prevence, konzultace
- **Slabé:** Chybí evidence úspěchu (%) – např. "Ušetřili jsme klientům X Kč"

---

## 🎨 Design & UX

### Co funguje
- Glassmorphism design je moderní a čitelný
- Barvy #00ea9a (zelená) a #00a9ff (modrá) jsou pěkné
- Case study stránky jsou responsivní

### Co zlepšit
- [ ] **Ikony** – používáme emoji, ale mohly by být SVG ikony (Feather, Heroicons)
- [ ] **Consistency** – Service cards mají emoji, case studies mají text → sjednotit
- [ ] **Dark mode toggle** – pro ty co upřednostňují light mode?
- [ ] **Animations** – Scroll reveal efekty? (Intersection Observer)

### Komponenty na zlepšení
- [ ] Service cards – přidat colored left border (dnes mají, OK)
- [ ] Case study hero – přidat background image (dnes mají, OK)
- [ ] Portfolio – lightbox je skvělý, ale mobil scrolluje vpravo

---

## ⚙️ Technické nápady

### Aktuální stack
- HTML + Tailwind (dnes)
- → Astro (budoucnost)

### Co řešit
- [ ] Kontaktní formulář – validace + email notifikace
- [ ] Lazy loading obrázků (performance)
- [ ] Service worker pro offline fallback?
- [ ] Analytics – Google Analytics? Plausible?

### Astro migration
- [ ] Rozdělit HTML do komponent
- [ ] Case studies jako `.astro` stránky (místo SPA)
- [ ] Možnost přidat CMS později (Keystatic, Decap)

### SEO
- [ ] Meta tagy (title, description, OG image)
- [ ] JSON-LD schema pro firmu + services
- [ ] Sitemap.xml + robots.txt
- [ ] Open Graph tagzy pro sociální sítě

---

## 🚀 Backlog myšlenek

### Vysoká priorita
- [ ] Kontaktní formulář – opravdu fungující
- [ ] Menu reorganizace – zjednoduší UX
- [ ] Case studies kompletní text – některé jsou half-baked

### Střední priorita
- [ ] Blog – dlouhodobý content marketing
- [ ] Video testimonials – klienti vypráví
- [ ] Interaktivní service finder – "Co řešíte?"

### Nízká priorita (nice to have)
- [ ] Dark/Light mode toggle
- [ ] Multi-language (CZ/EN)
- [ ] Chatbot (AI support)
- [ ] Scheduling systém (Calendly integration)

---

## 💡 Diskusní body (rozpracováno)

### Otázka 1: Menu struktura
**Problém:** Máme 7 položek v navigaci, je to moc?  
**Návrh:** Zkombinovat "Co řešíme" + "Case Studies" pod "Naše práce"  
**Status:** 🔄 Čeká na diskusi

### Otázka 2: Case studies lokace
**Problém:** Case studies jsou na homepage sekci, ale mohly by mít vlastní stránku  
**Návrh:** /case-studies/ s filtry (podle typu, branže)  
**Status:** 🔄 Čeká na diskusi

### Otázka 3: Portfolio smysl
**Problém:** Portfolio je jen fotogalerie bez textu – proč je tam?  
**Návrh:** Buď přidat descriptions, nebo sloučit s case studies  
**Status:** 🔄 Čeká na diskusi

---

## 📌 Poznámky & Linky

- Současné služby: IT Správa, Proxmox, Videokonference, Wi-Fi, Access Control, Kamery
- Case studies máme: Proxmox, Videokonference, IT Správa, AV Sál, Instalace monitorů
- Aktuální srovnání: Services ≠ Case Studies (ne všechny mají studiì)

---

**Poslední update:** Dnes  
**Editor:** Solverita Team  
**Format:** Markdown (.md) – edituj klidně v Notepad++, VS Code, nebo jakémkoliv textáku

