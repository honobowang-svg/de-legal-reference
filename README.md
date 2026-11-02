# Deutscher Rechtsreferenz-Assistent — Knowledge Base

Kostenlose, öffentliche **deutsche** Rechts**referenz**-Wissensbasis für einen einzelnen Grok Bot mit internem Routing (Spiegelung der US/JP/KR/UK-Packs).

**Keine Rechtsberatung. Kein Anwalt.** Normen und Beträge ändern sich; stets amtliche Quellen prüfen ([gesetze-im-internet.de](https://www.gesetze-im-internet.de/), [bmj.de](https://www.bmj.de/), BMAS, Landesjustizportale) und eine zugelassene Anwaltschaft bzw. örtliche Rechtsberatung / Beratungshilfe konsultieren.

## Was das ist

- **Bundesrecht** plus Hinweis auf das **Bundesland**, wenn Landesrecht, Gerichtsstand, Beratungshilfe oder örtliche Familiengerichtspraxis zählen.
- **11 Branchen**, jeweils fünf Dateien: `system_prompt.md`, `knowledge_base.md`, `calculators.md`, `deadlines.md`, `templates.md`.
- Standardsprache: **Deutsch**. Antwortet der Nutzer auf Chinesisch oder Englisch, darf die Antwort so erfolgen — **Gesetzesnamen und §§ bleiben Deutsch**.

## Branchen

| Dir | Thema |
|-----|--------|
| `family/` | Familie / Scheidung / Sorgerecht / Unterhalt |
| `inheritance/` | Erbrecht / Pflichtteil / Ausschlagung |
| `contracts/` | Vertragsrecht (BGB AT 1–3 Überblick) |
| `torts/` | Delikt / Schadensersatz (§§ 823 ff.) |
| `property/` | Miete / Wohnung / Eigentum |
| `employment/` | Arbeitsrecht / Mindestlohn / Kündigung |
| `criminal/` | Straf **Rechte & Verfahren nur** |
| `business/` | Gesellschaft & IP |
| `admin/` | Verwaltung / Aufenthalt (**nur Referenz**) |
| `consumer/` | Verbraucher & Online / Widerruf |
| `procedure/` | Zivilverfahren / Amtsgericht |

## Bot-Zusammenbau

1. Root-`bot_master_prompt.md` als Instructions.
2. Je Branche die fünf Dateien als Knowledge.
3. `test_cases.md` / `eval_report.md` nur für QA, nicht als Nutzerwissen.

## Verifikationsregel

Nur amtliche Texte zitieren. Gesetz + Paragraph + Stand. Ungeprüftes: **`【zu prüfen】` / `[TO VERIFY]`**. Keine erfundenen Normen, Euro-Beträge oder Urteile.

## Verifizierte Kernzahlen (Stand Abruf 2026-11-03 Asia/Shanghai)

| Thema | Wert | Quelle |
|-------|------|--------|
| Mindestlohn ab 1.1.2026 | **13,90 €**/h | MiLoV5 / BMAS |
| Mindestlohn ab 1.1.2027 | **14,60 €**/h | MiLoV5 |
| Regelkündigung § 622 Abs. 1 | 4 Wochen zum 15. oder Monatsende | BGB |
| Probezeitkündigung | 2 Wochen (§ 622 Abs. 3) | BGB |
| Regelmäßige Verjährung | **3 Jahre** (§ 195) | BGB |
| Verjährungsbeginn | § 199 Abs. 1 | BGB |
| AG-Zuständigkeit Streitwert | **bis 10.000 €** ab 1.1.2026 | § 23 Nr. 1 GVG |
| Pflichtteil | Hälfte des gesetzlichen Erbteils | § 2303 BGB |

## Haftung (jede Antwort)

Nur **Referenzinformationen**. **Keine Rechtsberatung**, Assistent ist **kein Anwalt**; Nutzer sollen **zugelassene Anwaltschaft / Rechtsberatung / Beratungshilfe** konsultieren.

## Lizenz / Kosten

Kostenlose öffentliche Referenzmaterialien. Keine Markenaffiliation. Kein Repo-Push vorgesehen.

Revision: 2026-11-03 (Asia/Shanghai)
