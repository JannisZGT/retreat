# Sport & Abenteuerreise — Website

## Projekt-Übersicht
Website für einen Sport- und Adventure-Retreat in Österreich (Tirol, Alpen).
Single-file: alles in `index.html` — kein Framework, kein Build-Tool, nur HTML + eingebettetes CSS + Vanilla JS.

## Sprache
- Website-Inhalt: **Deutsch**
- Kommunikation mit mir: **Deutsch**
- Code-Kommentare: Deutsch

## Technischer Stack
- `index.html` — gesamte Website (HTML + `<style>` + `<script>`)
- `assets/images/` — Bilder (werden vom User selbst eingefügt)
- Google Fonts: **Outfit** (Headlines) + **DM Sans** (Fließtext)
- Keine npm, kein Bundler, keine Dependencies

## Design-System

### Farben (CSS-Variablen)
```
--g:    #1E7A3A  /* Brand-Grün */
--g2:   #27A84F  /* Helleres Grün */
--g3:   #E6F7EC  /* Grün-Tint Hintergrund */
--g4:   #D0F0DB  /* Tieferer Tint */
--acc:  #FF5C2B  /* Orange-Akzent / CTA */
--w:    #FFFFFF
--bg:   #F7FAF8
--s0:   #111827  /* Text primär */
--s1:   #374151  /* Text sekundär */
--s2:   #6B7280  /* Gedämpft */
--s3:   #D1D5DB  /* Border */
```

### Typografie
- Headlines: `Outfit` (weight 400–800)
- Body: `DM Sans` (weight 300–600)
- Keine generischen Fonts (kein Inter, Roboto, Arial)

### Stil
- Hell, modern, luftig — kein dunkles Design
- Glassmorphism für Navigation (backdrop-filter blur)
- Animierte Blobs im Hero
- Scroll-Progress-Bar oben
- Scroll-Reveal mit IntersectionObserver (Klasse `.r` → `.r.in`)
- Counter-Animationen für Zahlen
- Marquee-Band zwischen Sektionen
- Bento-Grid für Aktivitäten
- Kein border-radius > 20px auf Cards, keine Emojis als Icons (nur inline SVG)

## Seitenstruktur

### Hauptseite (`index.html`)
1. Navigation (floating pill, Glassmorphism)
2. Hero (animated blobs, Parallax-Foto-Platzhalter)
3. Marquee-Band
4. Stats (Counter-Animation)
5. Retreat-Übersicht
6. Aktivitäten (Bento-Grid: Klettern, Kajak, Trail Running, Yoga)
7. Aftermovie (YouTube-Embed — Platzhalter vorhanden)
8. Fotogalerie + Lightbox
9. Feedback-Videos (3er-Grid + Video-Lightbox)
10. Programm / Die Woche (Accordion)
11. Anmeldung / CTA
12. Footer

### Subpages (hash-basiertes Routing in derselben Datei)
- `#buchung` → 5-Schritt-Buchungsformular
- `#impressum` → Impressum mit Platzhaltern

## Buchungsformular (5 Schritte)
1. Persönliche Daten (Name, Alter, Wohnort, E-Mail, Telefon)
2. Fitness & Erfahrung (Level 1–5, Dropdowns für Klettern/Kajak/Trail/Yoga)
3. Gesundheit (Verletzungen, Allergien, Medikamente — bedingte Felder)
4. Motivation (Freitext, Herkunft)
5. Paket & Zahlung (Frühbucher 1.490 € / Standard 1.790 €, Stripe-Platzhalter)

## Noch offen / Platzhalter
- Fotos: User legt eigene Bilder in `assets/images/` ab
  - `hero-bg.jpg`, `retreat-main.jpg`
  - `activity-klettern/kajak/trailrun/yoga.jpg`
  - `gallery-01.jpg` bis `gallery-08.jpg`
- YouTube-IDs: Aftermovie + 3 Feedback-Videos (Platzhalter `YOUTUBE_ID_1/2/3`)
- Formspree-ID: Formular schickt noch keine Daten (Integration ausstehend)
- Stripe: Payment-Platzhalter vorhanden, Integration ausstehend
- Impressum: Platzhalter-Texte müssen mit echten Daten gefüllt werden
- E-Mail: `info@deine-email.at` ersetzen
- Social-Links: Instagram, YouTube, Strava noch `href="#"`

## Wichtige Entscheidungen
- Keine Stripe-Integration vorerst — erst wenn Payment Links bereitstehen
- Rechnungen werden manuell erstellt (max. 12 Teilnehmer/Retreat)
- Formspree für Formular-Submissions (User muss Account erstellen)
- Alle Seiten bleiben in einer einzigen `index.html` — keine separaten Dateien

## Skills die verwendet werden
- `frontend-design` — für distinctive, production-grade UI
- `ui-ux-pro-max` — für Design-System, UX-Regeln, Accessibility
