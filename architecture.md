# Deutscher Rechtsreferenz-Assistent · Architektur (Single-Bot-Triage)

> Workspace: `/workspace/global-law-agents/de/`  
> Kostenlose öffentliche Rechtsreferenz (keine Rechtsberatung).  
> Ein Bot mit internem Routing — **nicht** elf separate Bots.  
> Revision: 2026-11-03 (Asia/Shanghai)

---

## 1. Ziele

1. Spiegelung der US/JP/KR/UK-Struktur: Master-Prompt + 11 Branchen × 5 Dateien.
2. **Bundesland-Triage**, wenn Landesrecht, Gerichtsstand, Beratungshilfe oder örtliche Praxis zählen.
3. Strafrecht = nur Rechte/Verfahren; Aufenthalt = nur Referenz (keine Visumgarantie).
4. Keine Normenerfindung; Lücken **`【zu prüfen】`**.
5. Sprache: Deutsch standard; CN/EN bei Nutzersprache; §§ und Gesetzesnamen Deutsch.

---

## 2. Laufzeitschichten

| Schicht | Datei(en) | Rolle |
|---------|-----------|------|
| Instructions | `bot_master_prompt.md` | Persona, Triage, Routing, Ablehnungen, Disclaimer |
| Playbooks | `*/system_prompt.md` | Umfang, Ablehnungen, Ablauf |
| Wissen | `*/knowledge_base.md` | Zitierte Normen / Portale |
| Rechner | `*/calculators.md` | Formeln (Mindestlohn, Streitwert, Pflichtteil) |
| Fristen | `*/deadlines.md` | Verjährung / Verfahrensfristen |
| Vorlagen | `*/templates.md` | Checklisten / Briefgerüste |
| QA (optional) | `test_cases.md`, `eval_report.md` | Nicht als Nutzerwissen |

---

## 3. Triage

```
Nutzerfrage
  → Bundesland / Ort falls nötig (Miete, Nachbar, Familiengericht, Beratungshilfe)
  → eine von 11 Kategorien
  → Fünferpaket laden
  → Antwort mit Zitat (Gesetz + § + Stand) + Disclaimer
```

---

## 4. Abdeckungspolitik

| Stufe | Inhalt |
|-------|--------|
| Voll-first | Bundesrecht mit verifizierten Kernzitaten (MiLoV5, § 622, §§ 195/199, § 23 GVG, § 2303) |
| Landeshinweis | Bundesland fragen; auf Landesjustizportal / örtliche Beratung verweisen |
| Nicht abgedeckt | Strafmaßprognose, Vereitelung, Visumgarantie, erfundene Euro-Beträge |

---

## 5. Sicherheit

- Keine Strafmaßprognose / Vereitelung / Beweisvernichtung.
- Keine Visumgarantien / Aufenthaltszusagen.
- Keine erfundenen Paragraphen oder Urteile.
- Jede Antwort endet mit Disclaimer (§6/§7 Master).
- Illegale Räumung / Eigenmacht: ablehnen, auf gerichtliche Wege verweisen.

---

## 6. Pflege

Bei Gesetzesänderungen: `knowledge_base.md` + Datum aktualisieren; Rechner/Tabellen anpassen; Regression in `test_cases.md`. Mindestlohn jährlich (MiLoV); GVG-Streitwerte bei Justizreformen; Düsseldorfer Tabelle jährlich neu 【zu prüfen】.
