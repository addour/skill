# hausinfo-arbeit — Testfälle und Ergebnisse

Bibliothek "Arbeit docs", 9 Dateien, ID `01a05c67-7950-744a-adab-232bcb7d9b24`.
Plattform: Vibe (vibe-hs.steuercloud-hessen.de).

## Testfälle

| ID | Frage | Erwarteter Modus | Worauf es ankommt |
|----|-------|------------------|-------------------|
| A1 | Ich habe gestern vergessen zu stempeln. Was mache ich? | ❌ oder 🟡 **mit Lückensatz** | Tz. 5.15 gilt nur für mobil erbrachte Arbeitszeit, ist kein Korrekturweg für ZKS. Lücke muss im Antworttext stehen. Personalbereich nennen. |
| A2 | Kann ich bei uns einen Sportkurs machen? | ❌ | Gesundheitsmanagement ist ein Nachbarthema, kein Beleg. |
| B1 | Ich möchte diesen Monat mehrere Gleittage nehmen. Was gilt für mich? | ✅ | Beide Grenzen (3/Monat **und** 24/Jahr). Zwei Dateien nebeneinander bleiben ✅. |
| B3 | — | sauber | |
| B7 | Gibt es bei uns ein Jobticket oder Fahrradleasing? | ❌ | Kurz-Zeile darf **nicht** "Es gibt kein…" sagen. Zuständige Stelle + E-Mail sind Pflicht. |
| C2 | — | sauber | |
| D1 | Ein Kollege im Finanzamt fragt, ob er mobil arbeiten darf. Was gilt für ihn? | ❌ | DA gilt nur für HZD. Verweis auf OH 2.2.2, die nicht vorliegt → ❌, nicht ✅. |
| E1 | — | sauber | |
| E2 | TV-H … (mit Wort *Internet*) | 🌐 | Widersprüchliche Webquellen offenlegen, nicht still eine wählen. |

## Ergebnisse v6 (13 090 Zeichen)

| ID | Ergebnis | Befund |
|----|----------|--------|
| A1 | 🟡 **Teilfehler** | Modus richtig, aber die Lücke wurde **nicht benannt**. Das Modell schrieb im Denkprotokoll selbst „Die Regelung könnte allgemein für alle Fälle von Zeiterfassungskorrekturen gelten (auch für ZKS)" — erfunden. Begründet mit der **Themenkarte**, nicht mit gelesenem Text. Dauer 3:13. |
| A2 | ✅ | ❌ statt ✅, Kreuz im arabischen Block nicht abgeschwächt. |
| B1 | ✅ | Beide Grenzen, Wichtig-Block vollständig belegt. |
| B3 | ✅ | |
| B7 | ⚠️ **Teilfehler** | Modus ❌ richtig, „Es gibt kein…" ist weg. Aber Abschnitt 9 hat **nicht gefeuert**: keine zuständige Stelle, keine E-Mail. Dauer 2:37 bei 9 Suchläufen. |
| C2 | ✅ | |
| D1 | ✅ | ❌ statt ✅, mit Personalbereich und E-Mail. |
| E1 | ✅ | |
| E2 | ✅ | „Achtung: Eine andere Quelle gibt an, dass 100 %…" |

## Ursachenanalyse

Drei Widersprüche **im Dokument**, nicht im Modell:

1. **Abschnitt 2 befahl, was Abschnitt 5 verbot.** Die Themenkarte schickte bei *Stempeln vergessen* ausdrücklich zu `DA_Mobiles_Arbeiten Tz. 5.15 für den Korrekturweg`; Abschnitt 5 nannte genau diese Übertragung einen Geltungsbereichsfehler. Das Modell zitierte die Themenkarte als Beleg — obwohl Abschnitt 2 sich selbst „keine Faktenquelle" nennt. → **A1**
2. **✅ war theoretisch unerreichbar.** Abschnitt 2 verlangte für fünf Kernthemen zwei Dateien, Abschnitt 5 erklärte „zwei Stellen kombinieren" zu 🟡. B1 kam nur durch eine großzügige Auslegung durch. → **B1 war Glück, keine Regel**
3. **Bei ❌ gaben Abschnitt 6, 8 und 9 drei verschiedene Antworten**, ohne Vorrang. B7 folgte nur Abschnitt 8, D1 nur Abschnitt 9. → **B7**

## Änderungen v7 (15 974 Zeichen)

- **§2** Tz. 5.15 aus dem Stempel-Pfad entfernt; als *Falle* mit Lückenbenennung und Personalbereich neu gefasst. Themenkarte ausdrücklich als Nicht-Beleg markiert. Block „zwei Dateien" in die Zeilen selbst gezogen (`beide lesen`).
- **§2** neuer Block **Nicht in der Bibliothek** (Jobticket, Fahrradleasing, Kantine, TV-H, Sportkurse …): höchstens zwei Suchen, dann ❌ + §9. Mit Schutzsatz: sagt nichts über die Wirklichkeit.
- **§5** Addition ≠ Ableitung: zwei Fundstellen, die je einen anderen Teil beantworten, bleiben ✅.
- **§5** **Bei 🟡 ist ein Lückensatz im Antworttext Pflicht.** Das Zeichen allein genügt nicht.
- **§5** Geltungsbereich wird am Wortlaut der Fundstelle geprüft, nicht an der Themenkarte.
- **§6** feste Reihenfolge bei ❌; ohne zuständige Stelle ist die Antwort unvollständig.
- **§8** die Internet-Zeile ist eine Schlusszeile, kein Ersatz für §9.
- **§9** „bei **jedem** Kreuz"; Personalbereich für Arbeitszeit und Abwesenheiten; Auffanglösung Personalbereich + Personalrat.
- **§11** zwei neue Prüfungen: Lückensatz bei 🟡, Begründung aus gelesenem Text statt aus der Themenkarte.

## Nächste Testrunde (v7)

1. **B7 Jobticket** — muss in **unter 30 Sekunden** ❌ + Personalbereich + E-Mail liefern. Doppeltest: prüft die Negativliste (Mitte der Datei) **und** §9 (hinten) → beweist zugleich, dass die Datei vollständig geladen ist.
2. **A1 Stempeln** — muss einen Satz enthalten wie „Für eine vergessene Stempelung am Dienstgebäude steht in den Unterlagen keine Korrekturregel."
3. **B1 Gleittage** — muss ✅ bleiben, mit beiden Grenzen.
4. **D1 Finanzamt** — muss ❌ bleiben.
5. **A2 Sportkurs** — muss ❌ bleiben, jetzt sofort über die Negativliste.
