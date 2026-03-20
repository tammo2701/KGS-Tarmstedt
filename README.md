<div align="center">

<br>

<svg width="72" height="72" viewBox="0 0 42 42" fill="none" xmlns="http://www.w3.org/2000/svg">
  <rect width="42" height="42" rx="10" fill="#1a5e3a"/>
  <path d="M8 26 L10 30 L32 30 L34 26 Z" fill="white" opacity="0.9"/>
  <rect x="14" y="20" width="14" height="6" rx="1" fill="white" opacity="0.85"/>
  <rect x="17" y="16" width="8" height="5" rx="1" fill="white" opacity="0.7"/>
  <rect x="22" y="12" width="4" height="6" rx="1" fill="#c9950e"/>
  <circle cx="24" cy="10" r="2" fill="#c9950e" opacity="0.6"/>
</svg>

<br><br>

# KGS Tarmstedt – Website Redesign

**Eine inoffizielle, moderne Neugestaltung der Schulwebsite der KGS Tarmstedt.**

<br>

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Keine Abhängigkeiten](https://img.shields.io/badge/Abhängigkeiten-keine-1a5e3a?style=for-the-badge)

<br>

> ⚠️ **Inoffizielle Nachbildung** — Dieses Projekt steht in keiner Verbindung zur KGS Tarmstedt oder der Samtgemeinde Tarmstedt. Es dient ausschließlich Demonstrationszwecken. Alle Inhalte basieren auf öffentlich verfügbaren Informationen der offiziellen Website [kgs-tarmstedt.de](https://www.kgs-tarmstedt.de). Die Seite wird selten aktualisiert; für verbindliche Informationen bitte die offizielle Website besuchen.

<br>

</div>

---

## 📸 Vorschau

| Startseite | Stellenangebote | Bücherei & Kombüse |
|:---:|:---:|:---:|
| Hero-Section mit Schulkennzahlen | Farbkodierte Stellenkarten | Vollständige Infos mit Öffnungszeiten |

---

## ✨ Features

### 🎨 Design
- **Waldgrün & Gold** — bewusstes Farbschema statt generischem Blau-Weiß
- **Lora** (Serif-Display) + **Plus Jakarta Sans** (Text) — charakterstarkes Schriftpaar
- **SVG-Logo** — der „Blaue Dampfer" als stilisiertes Schiff, direkt im Code
- **Dark-Feature-Section** auf der Startseite für das Schulprofil
- Konsistentes Design-System mit CSS-Variablen über alle 16 Seiten

### 📱 Responsiv & Zugänglich
- **Hamburger-Menü** — animiertes Slide-in Panel für Mobilgeräte, schließt per Escape oder Overlay-Klick
- **Fokus-Styles** — goldener Outline-Rahmen für Tastaturnavigation (WCAG 2.1 AA)
- **Skip-Link** — springt direkt zum Hauptinhalt für Screenreader
- **ARIA-Rollen** auf allen Hauptbereichen (`banner`, `navigation`, `main`, `contentinfo`)
- **Print-Stylesheet** — Stundenraster und Kontaktdaten druckfreundlich
- `rel="noopener"` auf allen externen Links

### 🔍 SEO & Meta
- Individuelle `<meta name="description">` auf jeder der 16 Seiten
- Open Graph Tags (`og:title`, `og:description`, `og:locale`) für Social-Media-Previews
- `robots: index, follow` — sichtbar für Google
- `<link rel="canonical">` gesetzt
- Semantisches HTML5 (`<main>`, `<header>`, `<footer>`, `<nav>`, `<section>`)

### ⚙️ Technisch
- **Kein Framework, keine npm, kein Build-Step** — reines HTML/CSS/JS
- **Favicon als SVG Data-URI** — kein extra File nötig
- **Smooth Scroll** (`scroll-behavior: smooth`) für Anker-Links
- Alle Seiten teilen eine einzige `style.css` (~14 KB)

---

## 📁 Dateistruktur

```
kgs-tarmstedt/
│
├── index.html              # Startseite
├── unsere-schule.html      # Leitbild, Schulordnung, Geschichte
├── fachbereiche.html       # Alle 10 Fachbereiche
├── jahrgaenge.html         # Jg. 5/6, 7–9, 10, Sek. II
├── ganztag.html            # Stundenraster, AGs, FSJ, Kombüse
├── aktuelles.html          # Neuigkeiten & Ankündigungen
├── teams.html              # Schulleitung, SV, Elternvertretung
├── partner.html            # Bücherei (ausführlich) + Kombüse e.V.
├── stellenangebote.html    # Lehrkräfte, FSJ, Referendariat
├── digitalisierung.html    # iPads, IServ, Medienscouts
├── kontakt.html            # Adressen, Öffnungszeiten, Anfahrt
├── impressum.html          # Rechtlicher Hinweis (inoffizielle Seite)
├── datenschutz.html        # DSGVO-Hinweis
│
├── style.css               # Gesamtes Design-System
├── build2.py               # Python-Build-Skript (generiert alle Seiten)
└── README.md               # Diese Datei
```


---

## 🛠️ Seiten neu generieren

Die HTML-Seiten werden mit einem Python-Build-Skript erzeugt, das gemeinsame Komponenten wie Header, Footer, Favicon und Meta-Tags automatisch in alle Seiten einbettet.

```bash
# Einzelne Seite neu bauen
python3 build2.py

# Alle Seiten auf einmal regenerieren
python3 rebuild_all.py
```

**Warum Python statt einem JS-Framework?** — Bewusste Entscheidung. Keine Node.js-Installation, kein `npm install`, kein Webpack. Ein Skript, fertig.

---

## 🎓 Schulkennzahlen

| | |
|---|---|
| 🏫 **Schulform** | Kooperative Gesamtschule (KGS) |
| 📍 **Adresse** | Kleine Trift 13, 27412 Tarmstedt |
| 🎓 **Oberstufe** | Gartenstraße 12a, 27412 Tarmstedt |
| 📞 **Telefon** | 04283 60834-0 |
| 👩‍🎓 **Schüler\*innen** | 1.189 (Klassen 5–Q2) |
| 🧑‍🏫 **Lehrkräfte** | 112 |
| 📐 **Züge** | 6-zügig |
| 🏆 **Zertifikate** | Europaschule in Niedersachsen, ProBerufsOrientierung, Erasmus+ |
| 📅 **Gegründet** | 01.08.1975 |

---

## ⏰ Stundenraster

| Block | Beginn | Ende |
|---|---|---|
| **1. Stunde** | 07:55 | 08:37 |
| *Pause* | *08:37* | *08:55* |
| **2.–3. Stunde** | 08:55 | 10:19 |
| *2. Pause* | *10:19* | *10:45* |
| **4.–5. Stunde** | 10:45 | 12:09 |
| *Mittagspause* | *12:09* | *13:01* |
| **7.–8. Stunde** | 13:01 | 14:29 |

---

## 📚 Bücherei — Öffnungszeiten

| Tag | Zeit |
|---|---|
| Montag | 14:00 – 17:00 |
| Dienstag | 14:00 – 17:00 |
| Donnerstag | 14:00 – 19:00 |
| Freitag | 10:00 – 12:00 |

📞 04283 / 1773 &nbsp;·&nbsp; ✉️ buecherei@tarmstedt.de &nbsp;·&nbsp; 🌐 [Online-Katalog](https://www.kgs-tarmstedt.de/buecherei-start/buecherei-katalog)

---

## ⚖️ Rechtlicher Hinweis

Dieses Projekt ist eine **private, nicht-kommerzielle Nachbildung** zu Übungszwecken. Es besteht **keine Verbindung** zur KGS Tarmstedt oder der Samtgemeinde Tarmstedt.

- Texte & Inhalte: Eigentum der KGS Tarmstedt / Samtgemeinde Tarmstedt
- Design & technische Umsetzung: Tammo Häbel
- Für verbindliche Informationen: [www.kgs-tarmstedt.de](https://www.kgs-tarmstedt.de)

---

<div align="center">

Gestaltet von **Tammo Häbel** &nbsp;·&nbsp; Keine offizielle Verbindung zur KGS Tarmstedt

</div>
