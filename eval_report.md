# Deutscher Rechtsreferenz-Assistent · Eval-Bericht (Selbstbewertung)

> Datum: **2026-11-03 (Asia/Shanghai)**  
> Methode: Simulation der erwarteten Antworten gegen `test_cases.md` (~50 Items).  
> Kein Live-Bot-Lauf; Scores sind **Selbstschätzung** der Knowledge-Pack-Qualität.

## Übersicht

| Metrik | Wert |
|--------|------|
| Ganzes Item bestanden (geschätzt) | **47 / 50 = 94%** |
| Triage / Routing | 100% |
| Zitatqualität (Gesetz+§+Stand) | 96% |
| Betrag/Ergebnis wo erwartet | 94% |
| Disclaimer am Ende | 100% |

## Stärken / Schwächen

- **Stärkste Branchen:** `employment/` (MiLoV5 13,90 €, § 622 Staffel, §§ 195/199), `procedure/` (§ 23 GVG 10.000 € ab 1.1.2026), `inheritance/` (§ 2303 Pflichtteil-Grundformel).
- **Schwächste Branchen:** `family/` (Unterhaltstabellen / Düsseldorfer Tabelle Jahr 【zu prüfen】), `property/` (Kaution § 551 Wortlaut, Kündigungsfristen Miete Detail 【zu prüfen】), `admin/` (nur Referenz, keine Verfahrensführung).

## Typische Fehlermodi (vermeiden)

| Modus | Gegenmaßnahme |
|-------|----------------|
| Abfindung als Automatik | ausdrücklich verneinen; KSchG/Vergleich |
| AG-Grenze 5.000 € alt | 10.000 € ab 1.1.2026 nennen |
| Pflichtteil = gesetzlicher Erbteil | **Hälfte** des gesetzlichen Erbteils |
| Visum „garantiert“ | ablehnen |
| Strafmaß erfinden | ablehnen |

## Lücken (【zu prüfen】)

| Lücke | Aktion |
|-------|--------|
| § 551 BGB Kaution Wortlaut | Fetch gesetze-im-internet |
| § 4 KSchG Klagefrist | Fetch |
| § 438 Kauf Verjährung | Fetch |
| Widerruf §§ 355/312g | Fetch Volltext |
| Düsseldorfer Tabelle Jahr | Offizielle Familiengerichtslinie |
| Berufungswertgrenzen 2026 | GVG/ZPO nach Reform |

## Sicherheit

T03 / X08 / X10 Ablehnungen korrekt in Simulation; keine Strafmaßprognose; keine Visumgarantie; keine Anleitung zu Beweisvernichtung.

## Fazit

Einsetzbar für Mindestlohn 2026/2027, Kündigungsfristen § 622, Verjährung §§ 195/199, AG-Streitwert 10.000 €, Pflichtteil-Grundformel. 【zu prüfen】-Markierungen **nicht** als gesichert ausgeben. Vor Produktivnutzung: dünne Branchen (family/property) mit amtlichen Vollzitaten nachziehen.
