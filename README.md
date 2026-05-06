# myTekton Content Engine

**Zweck:** Automatisierte Content-Produktion fuer Instagram (@mytekton). Aus neuen App-Features, Use Cases und Meilensteinen werden regelmaessig verwertbare Social-Assets erzeugt: Post-Ideen, Captions, Hashtags, Carousel-Outlines, CTAs — mit klarer Ablage pro Jahr/Monat/Woche.

**Primaerkanal:** Instagram (Feed + Reels + Stories). Facebook als Spiegel.
**Frequenz:** 2x pro Woche (Di, Do).
**Beste Zeiten:** 6:30-7:30, 12:00-13:00, 18:00-19:00.

---

## Ordnerlogik

| Ordner | Inhalt |
|--------|--------|
| `00-context/` | Single Source of Truth: Brand, ICP, Messaging, Tonalitaet, Hashtag-Sets |
| `01-input/` | Feature-Log (laufend), Release-Notizen, Rohideen |
| `02-calendar/` | Wochen- und Monatsplanung, Themen-Kalender |
| `03-assets/YYYY/MM/week-WW/` | Visual-Briefs, Screenshots, Carousel-Slides, Exportdateien |
| `04-captions/YYYY/MM/week-WW/` | Captions, CTAs, Hashtags (Markdown, postreif) |
| `05-published/` | Veroeffentlichte Inhalte + Learnings |
| `templates/` | Vorlagen (Weekly Pack, Feature-zu-Post, Caption-Blueprint) |

---

## Produktionsprozess (Loop)

1. **Feature → Input**
   Neues Feature, Release oder Use Case in `01-input/feature-log.md` ergaenzen (append-only).
2. **Input → Draft**
   Agent liest `00-context/mytekton-brief.md` + aktuellen Feature-Log und erzeugt `04-captions/YYYY/MM/week-WW/post-XX.md` plus Asset-Brief in `03-assets/YYYY/MM/week-WW/`.
3. **Draft → Review**
   Qualitaetscheck gegen Brand-Brief (Tonalitaet, CTA-Regeln, Hashtag-Sets, Verbotene Claims).
4. **Review → Freigabe**
   Tobi gibt frei oder korrigiert.
5. **Freigabe → Publish**
   Posten (manuell oder via Scheduler). Veroeffentlichte Variante nach `05-published/` verschieben, Learnings (Reach, Saves, Kommentare) ergaenzen.

---

## Modellverteilung

- Standard-Agenten: **Codex**
- Ausnahmen: **CPO = Claude**, **DSO = Claude**
- Repo-Zugriff: **read-only** fuer Agenten
- Keine autonomen Publikationen ohne Freigabe

---

## Mindest-Inputs (alle in `00-context/`)

1. Produkt-Positionierung (ICP, Problem, Nutzenversprechen)
2. Feature-Changelog (neu / verbessert / bugfix)
3. Belege/Screenshots pro Feature (`03-assets/`)
4. Tonalitaet + Do/Don't (Brand Voice)
5. CTA-Regeln (Demo, DM, Website)
6. Kanalregeln (IG Reels, Carousel, Single, Stories)

---

## Naming-Konvention

- Wochenordner: `week-WW` (ISO-Kalenderwoche, zweistellig)
- Post-Dateien: `post-XX-slug.md` (z. B. `post-01-zettelwirtschaft.md`)
- Assets: `post-XX-<rolle>-<slug>.png` (z. B. `post-01-carousel-slide1.png`)
