# Feature Log (laufend, append-only)

> **Wie benutzen:** Neue Eintraege **oben** anhaengen. Jeder Eintrag folgt der Vorlage. Abgeschlossene Eintraege bleiben stehen — sind Futter fuer spaetere Content-Serien.
> **Quelle Sprints:** `~/Projects/handwerker-app/docs/sprints/`

---

## Vorlage pro Eintrag

```
- Datum:
- Feature-Name:
- Typ: (neu | verbessert | bugfix)
- Problem vorher:
- Loesung jetzt:
- Nutzer-Impact:
- Zielgruppe:
- Beleg: (Commit/PR/Release/Screenshot/URL)
- Rohideen fuer Content (optional):
```

---

## Initial-Eintraege (abgeleitet aus abgeschlossenen Sprints)

---

### 2026-04-04 — Firmenlogo Upload & Branding
- Typ: neu
- Problem vorher: PDF-Auftragsberichte sahen generisch aus, Firmen konnten sich darauf nicht wiedererkennen
- Loesung jetzt: Firma kann Logo hochladen (Supabase Storage, public bucket `firma-logos`), erscheint im Header und auf PDF-Berichten
- Nutzer-Impact: Professionelle Aussenwirkung ohne Designer-Aufwand
- Zielgruppe: Admins, Handwerker die Kunden PDFs schicken
- Beleg: Sprint 19 `docs/sprints/sprint-19-firmenlogo-branding.md`
- Rohideen: "Vorher / Nachher PDF mit Logo", Karussell "Dein Logo in jedem Auftragsbericht"

---

### 2026-03-29 — Mobile UX Optimierung
- Typ: verbessert
- Problem vorher: Bedienung auf dem Handy auf der Baustelle war fummelig, Buttons zu klein
- Loesung jetzt: Groessere Touch-Targets, MobileNav, optimierte Kanban-Karten auf Smartphones
- Nutzer-Impact: Funktioniert jetzt wirklich einhaendig auf der Baustelle
- Zielgruppe: Handwerker, Projektleiter unterwegs
- Beleg: Sprint 18 `docs/sprints/sprint-18-mobile-ux.md`
- Rohideen: Reel "Auftrag per Daumen erfassen — in 10 Sekunden"

---

### 2026-03-20 — Rebranding HandwerkerHub → myTekton
- Typ: neu
- Problem vorher: Name "HandwerkerHub" war generisch, schwer merkbar, nicht schuetzbar
- Loesung jetzt: Rebranding zu myTekton (griechisch: Handwerker), neue Domains mytekton.app + mytekton.de, neue Farbpalette (Cream + Orange)
- Nutzer-Impact: Starke, merkbare Marke mit Geschichte
- Zielgruppe: Alle
- Beleg: `docs/sprints/rebranding-mytekton.md`
- Rohideen: Story "Der Name — woher kommt 'Tekton'?", Karussell Brand-Reveal

---

### 2026-03-15 — Stripe SaaS-Abonnement
- Typ: neu
- Problem vorher: Keine Monetarisierung, unklar wer zahlt
- Loesung jetzt: Ein Beta-Plan fuer 25 EUR/Monat, 30 Tage Trial, Stripe-Checkout + Customer-Portal, Hard-Lockout bei CANCELED/UNPAID
- Nutzer-Impact: Fairer, einfacher Preis fuer den ganzen Betrieb
- Zielgruppe: Alle
- Beleg: Sprint 20 `docs/sprints/sprint-20-stripe-abo.md`
- Rohideen: Post "25 Euro im Monat fuer den ganzen Betrieb — das war's"

---

### 2026-03-10 — Dashboard Interaktiv + Kalender-Sync
- Typ: verbessert
- Problem vorher: Dashboard war statisch, Kalender-Events mussten manuell gepflegt werden
- Loesung jetzt: Dashboard mit Recharts (Auftraege nach Phase, Aktivitaeten), Kalender als zentrale Termin-Uebersicht mit iCal-Sync
- Nutzer-Impact: Meister sieht auf einen Blick was laeuft, Termine synchronisieren sich in Google/Apple Kalender
- Zielgruppe: Admins, Projektleiter
- Beleg: Sprint 17 `docs/sprints/sprint-17-dashboard-interaktiv-kalender-sync.md`
- Rohideen: Reel "Dashboard als erstes am Morgen", Post "iCal-Sync in 2 Klicks"

---

### 2026-03-05 — Finanzen + Kundennummer
- Typ: neu
- Problem vorher: Buchhaltung hatte keinen eigenen Blick auf Abrechnungsrelevante Daten
- Loesung jetzt: Kundennummer (unique pro Firma), Finanz-Ansicht fuer Buchhaltungs-Rolle, Auftraege in Abrechnung uebersichtlich sortiert
- Nutzer-Impact: Buchhaltung arbeitet schneller, nichts faellt durchs Raster
- Zielgruppe: Buchhaltung, Admins
- Beleg: Sprint 16 `docs/sprints/sprint-16-finanzen-kundennummer.md`
- Rohideen: Post "4 Rollen — jeder sieht was er braucht"

---

### 2026-02-25 — Zeiterfassung mit Start/Stop-Timer
- Typ: neu
- Problem vorher: Arbeitszeiten per Stift/Zettel/Erinnerung, Stunden gingen verloren
- Loesung jetzt: Handwerker startet Timer direkt am Auftrag, Zeit laeuft im Hintergrund, Stop schreibt Zeiteintrag
- Nutzer-Impact: Keine vergessenen Stunden, faire Abrechnung, weniger Konflikt mit Kunden
- Zielgruppe: Handwerker, Projektleiter, Buchhaltung
- Beleg: Sprint 14 `docs/sprints/sprint-14-zeiterfassung.md`
- Rohideen: Reel "Timer starten, arbeiten, Timer stoppen — fertig", Post "Wie viele Stunden sind dir letztes Jahr durch die Lappen gegangen?"

---

### 2026-02-18 — PDF-Export Auftragsberichte
- Typ: neu
- Problem vorher: Kunden wollten nachvollziehbare Berichte, Handwerker schrieben sie per Hand
- Loesung jetzt: Server-seitige PDF-Generierung mit @react-pdf/renderer, Firmenlogo, alle Auftragsdaten + Fotos
- Nutzer-Impact: Professioneller Bericht auf Knopfdruck
- Zielgruppe: Admins, Projektleiter
- Beleg: Sprint 12 `docs/sprints/sprint-12-pdf-export.md`
- Rohideen: Karussell "Vom Auftrag zum Bericht in 1 Klick"

---

### 2026-02-12 — Kalenderansicht + iCal-Sync
- Typ: neu
- Problem vorher: Termine waren ueber viele Auftraege verstreut, keine Gesamtuebersicht
- Loesung jetzt: Monatskalender mit allen Terminen, iCal-Feed pro Firma (HMAC-gesicherter Token) fuer Google/Apple/Outlook
- Nutzer-Impact: Termine landen automatisch auf dem privaten Kalender
- Zielgruppe: Meister, Projektleiter
- Beleg: Sprint 10 `docs/sprints/sprint-10-kalender-ical.md`
- Rohideen: Reel "Alle Baustellentermine auf einem Blick"

---

### 2026-02-05 — Rollenbasierte Sichtbarkeit
- Typ: neu
- Problem vorher: Jeder sah alles — Handwerker wurden von irrelevanten Auftraegen zugeschuettet
- Loesung jetzt: 4 Rollen (Admin, Projektleiter, Handwerker, Buchhaltung) mit eigenen Sichten und Rechten
- Nutzer-Impact: Weniger Ablenkung, klare Verantwortung, bessere Datensicherheit
- Zielgruppe: Alle
- Beleg: Sprint 11 `docs/sprints/sprint-11-rollenbasierte-sichtbarkeit.md`
- Rohideen: Karussell "4 Rollen — was jeder sieht"

---

### 2026-01-28 — Fotos, Dokumente, Kommentare am Auftrag
- Typ: neu
- Problem vorher: Baustellenfotos auf 5 verschiedenen Handys, nachher keiner weiss wo was liegt
- Loesung jetzt: Fotos und Dokumente direkt am Auftrag in Supabase Storage (private Bucket), Bildkompression auf max. 2 MB, Kommentare (mit `istIntern`-Flag)
- Nutzer-Impact: "Wo ist das Foto von der Steckdose?" — nie wieder
- Zielgruppe: Alle, vor allem Handwerker auf Baustelle
- Beleg: Sprint 5 `docs/sprints/sprint-05-fotos-dokumente-kommentare.md`
- Rohideen: Reel "Foto machen — fertig", Post "Wo ist das Foto von der Steckdose?"

---

### 2026-01-20 — Mitarbeiterboard (Kanban #3)
- Typ: neu
- Problem vorher: "Wer macht morgen was?" — haeufige Frage im Betrieb
- Loesung jetzt: Dynamisches Board mit einer Spalte pro Mitarbeiter, Drag & Drop zur Zuweisung, phaseBadge zeigt Planung/Ausfuehrung
- Nutzer-Impact: Klare Zuweisung, jeder weiss wo er morgen hin muss
- Zielgruppe: Meister, Projektleiter
- Beleg: Sprint 4 `docs/sprints/sprint-04-ausfuehrung-mitarbeiterboard.md`
- Rohideen: Reel "Mitarbeiter per Drag & Drop zuweisen", Post "Montag 6:45 — jeder weiss wo er hin muss"

---

### 2026-01-15 — Planungsboard + Ausfuehrungsboard (Kanban #1/#2)
- Typ: neu
- Problem vorher: Keine Uebersicht welcher Auftrag in welcher Phase ist — Zettelwirtschaft
- Loesung jetzt: Zwei Kanban-Boards, Phasen `PLANUNG → AUSFUEHRUNG → ARCHIVIERT`, Statuswechsel per Drag & Drop
- Nutzer-Impact: Auf einen Blick sichtbar: was ist offen, in Planung, bereit zur Ausfuehrung, in Abrechnung
- Zielgruppe: Meister, Projektleiter
- Beleg: Sprints 3+4 `docs/sprints/sprint-03-planungsboard.md`, `sprint-04-ausfuehrung-mitarbeiterboard.md`
- Rohideen: Karussell "So sieht Ordnung aus", Reel "Auftrag von Eingang bis Abrechnung — Drag & Drop"
