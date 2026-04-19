# Feature → Post — Mapping-Anleitung

**Zweck:** Aus einem einzelnen Feature-Log-Eintrag zuverlaessig 1-3 Instagram-Posts erzeugen.

---

## Input

Ein Eintrag aus `01-input/feature-log.md` mit den Feldern:
- Feature-Name
- Typ (neu / verbessert / bugfix)
- Problem vorher
- Loesung jetzt
- Nutzer-Impact
- Zielgruppe
- Rohideen (optional)

---

## Ableitungsregeln

### Variante A — Problem-Post (Montag)
- **Format:** Carousel 5-6 Slides
- **Hook:** Problem zugespitzt formulieren (Frage oder Szenario aus dem Alltag)
- **Slides:** Problem → Konsequenz → Alternativ-Zustand → CTA
- **Beispiel:** "Wo ist das Foto von der Steckdose?" (aus Feature "Fotos am Auftrag")

### Variante B — Feature-Post (Mittwoch)
- **Format:** Reel 15-30 Sek. oder Single Image mit Screenshot
- **Hook:** Ein konkreter Use Case ("Timer starten, arbeiten, Stop")
- **Body:** Wie es funktioniert (3 Schritte), warum es nuetzlich ist
- **CTA:** "30 Tage kostenlos testen — Link in Bio"
- **Beispiel:** "Zeit stoppen direkt am Auftrag" (aus Feature "Zeiterfassung")

### Variante C — Vorher/Nachher (Freitag)
- **Format:** Single Image Split-Screen
- **Hook:** "Links: Chaos. Rechts: myTekton."
- **Body:** Konkreter Vorher-Zustand, konkrete Loesung
- **CTA:** Frage / Umfrage
- **Beispiel:** "Excel-Tabs vs. Kanban-Board"

---

## Do's

- Aus der **Zielgruppen-Perspektive** schreiben (Meister/Projektleiter/Handwerker je nach Rolle)
- Konkrete Szenarien (Uhrzeit, Baustelle, Gewerk) statt abstraktem Nutzen
- **Eine** Kernaussage pro Post — nicht das ganze Feature erklaeren
- Frage am Ende = Kommentare = Reichweite
- Bei Screenshots: realistische Testdaten (Metallbau Weber GmbH, A-2026-00x)

---

## Don'ts

- Keine Feature-Aufzaehlung ("und dann kann man noch ...")
- Kein Marketing-Deutsch, kein "revolutionaer"
- Keine Roadmap-Features bewerben, die noch nicht live sind
- Keine Kundennamen ohne schriftliche Freigabe
- Keine Preisabweichungen (immer 25 EUR/Monat, 30 Tage Trial)

---

## Output-Format

Pro abgeleitetem Post eine Datei unter
`04-captions/YYYY/MM/week-WW/post-XX-slug.md`
nach `templates/post-blueprint.md`.

Plus Asset-Brief in
`03-assets/YYYY/MM/week-WW/post-XX-brief.md`
(oder direkt in der Post-Datei unter "Asset-Brief").
