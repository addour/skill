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

## Ergebnisse v7 (15 974 Zeichen)

**Ladeprüfung bestanden.** In beiden Läufen feuerte Abschnitt 9 (hinten in der Datei),
in A1 wurde zusätzlich die E-Mail-Vorlage aus Abschnitt 12 benutzt, und der
Fallen-Block aus Abschnitt 2 wurde im Denkprotokoll wörtlich zitiert.
Die Datei wird bei ~16 000 Zeichen vollständig geladen.

| ID | Ergebnis | Befund |
|----|----------|--------|
| B7 | ⚠️ fast | ❌ richtig, Kurz-Zeile korrekt („steht nichts in den Unterlagen"), Z2 Personal genannt, Internet-Zeile da. Dauer **56 s statt 2:37**. Zwei Fehler: die E-Mail wurde nur **angeboten** („Möchtest du eine E-Mail-Vorlage?") statt geschrieben, und der Personenname kam falsch heraus. |
| A1 | ✅ **bestanden** | ❌ mit dem Lückensatz „Für eine vergessene Stempelung am Dienstgebäude gibt es in den Unterlagen keine Regel.", Tz. 5.15 nur als Hinweis mit Geltungsbereich, Z2 Personal, vollständige E-Mail, Internet-Zeile. Dauer 1:56 statt 3:13. **Der Kernfehler aus v4 bis v6 ist weg.** |

### Zwei neue Befunde

1. **Personennamen werden verstümmelt.** Derselbe Name kam in drei Läufen als
   *Tellschaft*, *Tesellschaft* und *Tgesellschaft* heraus — in B7 schrieb das Modell
   im Denkprotokoll noch die eine Schreibweise und im Antworttext eine andere.
   Ein falscher Name in einer E-Mail an den Personalbereich ist nicht korrigierbar.
2. **„Biete eine E-Mail an" wurde als Rückfrage gelesen.** In B7 fragte das Modell,
   ob eine Vorlage gewünscht sei; in A1 schrieb es sie aus. Dieselbe Regel, zwei
   Verhalten — die Formulierung war mehrdeutig.

## Änderungen v8 (16 335 Zeichen)

- **§2 Fallen** keine Personennamen mehr aus dem Geschäftsverteilungsplan, nur die
  Organisationseinheit mit Aufgabe. Begründung steht in der Regel selbst.
- **§9** „Schreib die E-Mail vollständig aus … Frag nicht, ob der Nutzer eine Vorlage
  möchte, sondern liefere sie fertig zum Kopieren."
- **§6** bei Kreuz „mit vollständig ausgeschriebener E-Mail".
- **§11** zwei neue Prüfungen: E-Mail ausgeschrieben statt angeboten, kein Personenname.

## Testrunde auf v7 (nachgereicht, v8 war noch nicht hochgeladen)

Erkennbar an den Denkprotokollen: sie zitieren „einen Namen nur als Zusatz und nur,
wenn er dort steht" — die v7-Fassung von Abschnitt 9.

| ID | Ergebnis | Dauer | Befund |
|----|----------|-------|--------|
| B1 | ✅ **bestanden** | **0:29** (v6: 1:47) | ✅ Haken mit beiden Grenzen und beiden Quellen. **Die Regel „Addition ist keine Ableitung" aus §5 wirkt** — zwei Dateien machen die Antwort nicht mehr zu Gelb. Kleiner Verlust: der Vorbehalt „soweit dienstliche Gründe nicht entgegenstehen" aus Tz. 5.4 fehlt, v6 hatte ihn noch. |
| D1 | ✅ **bestanden** | 0:53 (v6: 1:15) | ❌ richtig, OH 2.2.2 benannt, Personalbereich des Finanzamts und Personalrat, E-Mail ausgeschrieben. |
| B7 | ✅ Verdikt richtig | 1:05 | ❌ richtig, Kurz-Zeile korrekt, E-Mail diesmal **ausgeschrieben** statt angeboten — dieselbe v7-Regel, anderes Verhalten als um 14:14. Die Mehrdeutigkeit war also echte Varianz, kein Einzelfall. Namen weiterhin verstümmelt: Denkprotokoll „Tellschaft", Antworttext „Tesellschaft" im selben Lauf. |
| A2 | ⚠️ Verdikt richtig, Text falsch | **3:20** | ❌ richtig und BGM ist die beste denkbare Zuständigkeit. Aber: Kurz-Zeile beginnt mit **„Nein,"** — damit ist die Sachfrage doch beantwortet, verboten nach §5. Dazu Personennamen **mit Personalnummer** (ANr. 1915, ANr. 2247). Und die Negativliste sparte hier keine Zeit: das Modell fand mit BGM ein Nachbarthema und rang lange damit. |

### Befunde

1. **„Nein" ist die neue Form des alten Fehlers.** §5 verbietet die Aussage, dass es
   die Sache nicht gibt. Das Modell fand einen Weg, sie in ein einziges Wort zu
   packen, während der Rest des Satzes korrekt blieb.
2. **Personalnummern kamen mit den Namen.** §10 verbietet personenbezogene Daten,
   §2 sprach nur von Namen.
3. **Ein Nachbarthema hebelt die Negativliste aus.** Steht das Thema auf der Liste,
   das Modell findet aber eine thematisch nahe Einheit, sucht es weiter statt
   abzubrechen. Die gefundene Einheit ist in Wahrheit schon die Antwort auf die
   Zuständigkeitsfrage.

## Änderungen v9 (16 916 Zeichen)

- **§5** Kurz-Zeile bei ❌ darf nicht mit Nein oder Ja beginnen.
- **§2** Negativliste: ein benachbarter Treffer ist kein Treffer, sondern die
  zuständige Stelle — dort abbrechen.
- **§2** keine Personalnummern, nicht nur keine Namen.
- **§4** auch nach Vorbehalten suchen („soweit dienstliche Gründe nicht entgegenstehen").
- **§11** zwei neue Prüfungen.

## Nächste Testrunde (v9)

Alles auf **v9** laufen lassen, v8 wurde nie getestet.

1. **A2 Sportkurs** — Kurz-Zeile ohne „Nein", keine Namen, keine ANr., deutlich unter 3:20.
2. **B7 Jobticket** — E-Mail ausgeschrieben, ohne Personennamen.
3. **B1 Gleittage** — muss ✅ bleiben, jetzt **mit** dem Vorbehalt „dienstliche Gründe".
4. **A1 Stempeln** — muss ❌ mit Lückensatz bleiben.
5. **D1 Finanzamt** — muss ❌ bleiben.
