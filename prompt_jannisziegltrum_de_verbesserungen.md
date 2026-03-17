# Website-Verbesserungen — jannisziegltrum.de

Bitte analysiere zunächst die Projektstruktur und den Tech-Stack dieser Website,
dann setze die folgenden drei Verbesserungen um.

---

## Schritt 1: Projektstruktur verstehen

Lies die wichtigsten Dateien (HTML, CSS, JS, Framework-Config), damit du den
genauen Aufbau der Seite kennst, bevor du Änderungen vornimmst.

---

## Schritt 2: Drei konkrete Änderungen umsetzen

### Änderung 1 — Sticky WhatsApp-Button (immer sichtbar, unten rechts)

**Was:**
Füge einen sticky WhatsApp-Button ein, der auf jeder Scroll-Position unten rechts
im Viewport fixiert bleibt. Beim Klick öffnet sich direkt ein WhatsApp-Chat.

**Wie:**
- Position: `fixed`, `bottom: 24px`, `right: 24px`, `z-index` hoch genug um
  über allen anderen Elementen zu liegen
- Aussehen: runder Button (circle), WhatsApp-Grün (`#25D366`), weißes WhatsApp-Icon
  (SVG oder Font Awesome). Kein Text — nur das Icon reicht.
- Größe: mindestens 56x56px (auf Mobile gut tippbar)
- Schatten: leichter `box-shadow` damit er sich vom Hintergrund abhebt
- Link: `https://wa.me/49XXXXXXXXXX` — Platzhalter, bitte durch echte Nummer ersetzen
  (`<!-- TODO: WhatsApp-Nummer eintragen -->`)
- Optional: kleiner Hover-Effekt (leicht größer oder heller werden)

**Warum:** Der Sticky-Button ist auf jeder Scroll-Position sichtbar — egal ob
jemand gerade das Programm liest oder die FAQ durchgeht. Er drängt sich nicht
auf (kein Text, kein Banner), ist aber sofort greifbar wenn jemand schreiben will.
Besonders auf Mobile ist das der natürlichste Kontaktweg.

---

### Änderung 2 — Persönliche Vorstellung "Ich bin Jannis"

**Was:**
Füge einen neuen Abschnitt ein, der Jannis als Person vorstellt. Dieser Abschnitt
soll direkt nach dem Hero-Bereich oder vor/nach den Aktivitäten-Karten erscheinen.

**Inhalt des Abschnitts (Platzhalter — Jannis soll den Text selbst anpassen):**
- Überschrift: "Ich bin Jannis." oder "Wer steckt dahinter?"
- Kurzer persönlicher Text (3–5 Sätze): Wer bin ich, warum mache ich dieses Retreat,
  was treibt mich an?
- Ein Foto von Jannis (Platzhalter-Element, falls kein Bild vorhanden — z.B. ein
  `<img>`-Tag mit `src="[FOTO-JANNIS]"` und einem Kommentar `<!-- Bitte Foto einfügen -->`)
- Optional: 2–3 kurze persönliche Fakten (z.B. "Seit 5 Jahren in den Bergen unterwegs",
  "Zertifizierter Bergführer", o.ä.)

**Layout:**
- Zweispaltig auf Desktop: links Foto, rechts Text (oder umgekehrt)
- Auf Mobile: gestapelt (Foto oben, Text unten)
- Visuell warm und persönlich halten — kein steriler "Über uns"-Block

**Warum:** Bei einem Premium-Erlebnis wie einem Retreat kaufen Menschen zuerst
die Person, dann das Angebot. Eine persönliche Vorstellung baut Vertrauen auf
und macht den Unterschied zwischen "interessant" und "ich buche jetzt".

---

### Änderung 3 — Zwischenseitiger CTA nach dem Programm-Abschnitt

**Was:**
Füge direkt nach dem Programm-Abschnitt ("Ein typischer Tag.") einen zusätzlichen
Call-to-Action-Button ein.

**Gestaltung:**
- Überschrift über dem Button: "Klingt gut?" oder "Bereit für deinen Sommer?"
- Button-Text: "Jetzt Platz sichern" oder "Zur Anmeldung"
- Button-Link: Anchor-Link zum bestehenden Buchungs-/Anmeldebereich (`#buchung`
  oder `#anmeldung`)
- Optionaler Subtext unter dem Button: z.B. "Noch X Plätze verfügbar" oder
  "Nächster Termin: [Datum]" (Platzhalter, Jannis soll das aktuell halten)

**Warum:** Interessenten die sich das Programm durchgelesen haben, sind bereits
warm — sie brauchen in diesem Moment eine direkte Handlungsaufforderung.
Ohne CTA scrollen viele weiter, ohne zu buchen, selbst wenn sie es wollten.

---

## Wichtige Hinweise zur Umsetzung

- Halte dich ans bestehende Design-System (Farben, Fonts, Abstände, Klassen)
- Erfinde keine neuen Komponenten wenn bestehende Elemente wiederverwendet
  werden können
- Kommentiere Platzhalter klar (Telefonnummer, Foto, Datum), damit Jannis sie
  leicht findet und austauschen kann
- Teste alle Änderungen gedanklich auf Mobile (Viewport < 400px)
- Kein Over-Engineering: die Änderungen sollen minimal invasiv sein

---

## Nach der Umsetzung

Zeige mir bitte für jede der drei Änderungen:
1. Welche Datei(en) du geändert hast
2. Den genauen Code-Abschnitt der eingefügt/geändert wurde
3. Was ich als Nächstes tun muss (z.B. Foto einfügen, Telefonnummer eintragen)
