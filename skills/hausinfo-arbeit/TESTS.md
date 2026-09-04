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

## Ergebnisse v9 — 5 von 5 Verdikten richtig

| ID | Ergebnis | Dauer | Befund |
|----|----------|-------|--------|
| A2 | ✅ **bestanden** | **1:13** (v7: 3:20) | Alle drei v9-Korrekturen auf einmal belegt: Kurz-Zeile ohne „Nein", BGM ohne Personennamen und ohne ANr., und die Suche brach beim Nachbartreffer ab. |
| B1 | ✅ **bestanden** | 1:39 | ✅ Haken, beide Grenzen, und der in v7 verlorene Vorbehalt ist zurück: „Dienstliche Gründe können die Genehmigung einschränken [Tz. 5.4]". Dazu neu der Genehmigungsschritt aus Tz. 2.5. |
| B7 | ✅ **bestanden** | 1:46 | ❌ richtig, ZES PA mit Aufgabe und Quelle, keine Namen, E-Mail ausgeschrieben. Die längere Dauer kam von zwei Tool-Signaturfehlern, nicht vom Skill. |
| A1 | ⚠️ bestanden mit Verlust | 1:42 | ❌ mit Lückensatz, Z2 Personal, E-Mail. Aber der Hinweis auf Tz. 5.15 aus v7 fehlt. |
| D1 | ⚠️ bestanden mit Verlust | 3:27 | ❌ richtig. Aber **OH 2.2.2 kommt in der Antwort nicht mehr vor**, und die genannte Stelle „Personalbereich des Hessischen Finanzressorts" steht so in keiner Datei — der Geschäftsverteilungsplan beschreibt die HZD, nicht das Finanzressort. |

### Ein Befund, zwei Symptome

A1 und D1 verloren beide genau das, was die Unterlagen zum Fall **doch** sagen,
ohne ihn zu regeln: bei A1 den Geltungsbereich von Tz. 5.15, bei D1 den Namen
der zuständigen Dienstvereinbarung OH 2.2.2. Für den Nutzer ist gerade das die
wertvollste Zeile — sie sagt ihm, nach welchem Dokument er fragen muss.

Ursache ist dieselbe Bauart wie die Widersprüche in v6: **die feste Kreuz-Reihenfolge
in §6 hatte für so eine Zeile keinen Platz**, und §2 verlangte sie trotzdem
(„nenne Tz. 5.15 höchstens als Hinweis"). Wo das Format keinen Ort vorsieht,
fällt der Inhalt weg.

Dazu ein zweiter Befund aus D1: fehlt eine passende Einheit, erfindet das Modell
eine plausible statt zu sagen, dass sie nicht in den Unterlagen steht.
Seitenzahlen im Geschäftsverteilungsplan driften ebenfalls (23/25, 23/152, 19, 21).

## Änderungen v10 (17 932 Zeichen)

- **§6** neuer optionaler **Hinweis**-Block bei ❌: ein bis zwei Sätze für das,
  was die Unterlagen zum Fall sagen, ohne ihn zu regeln. Mit Quelle, mit dem
  Zusatz, dass es keine Regel für den gefragten Fall ist, und ohne dass ❌ dadurch
  zu 🟡 wird.
- **§9** keine erfundenen Organisationseinheiten; fehlt eine, wird das gesagt.
  Der Geschäftsverteilungsplan beschreibt die HZD und gilt nicht für ein Finanzamt —
  dort Personalbereich des jeweiligen Finanzamts und örtlicher Personalrat.
- **§2** im Geschäftsverteilungsplan statt der Seitenzahl die Organisationskennung
  nennen (Z2, ZES PA).
- **§11** zwei neue Prüfungen.

## Ergebnisse v10 — beide Rückschritte behoben

| ID | Ergebnis | Dauer | Befund |
|----|----------|-------|--------|
| D1 | ✅ **bestanden** | **1:04** (v9: 3:27) | Hinweis-Block da und nennt **OH 2.2.2** samt Geltungsbereich der HZD-DA. Zuständige Stelle jetzt „Personalbereich des jeweiligen Finanzamts" und örtlicher Personalrat — keine erfundene Einheit mehr. |
| A1 | ⚠️ bestanden, ein neuer Fehler | 1:16 | Hinweis auf Tz. 5.15 ist zurück, mit Wortlaut und der Einordnung „gilt nur für mobiles Arbeiten". Aber die Vorlage endet mit **`E-Mail-Adresse: Personalbereich@hzd.hessen.de`** — diese Adresse steht in keiner Datei. |
| B1 | ✅ **bestanden** | 1:14 | ✅ Haken unverändert, der neue Hinweis-Block fasst ✅-Antworten nicht an. Inhaltlich die bisher vollständigste Fassung: beide Grenzen, Vorbehalt in Regel und Wichtig, vier Schritte mit Quellen, Begriff „Vertretung" ergänzt. |

### Ein neuer Fehler

Erfundene Kontaktdaten. §9 verlangte eine fertige E-Mail und sagte nichts über
die Empfängeradresse, also ergänzte das Modell eine plausibel aussehende. Eine
falsche Adresse ist schlimmer als keine: die Mail sieht abgeschickt aus und kommt
nirgends an.

## Änderungen v11 (18 329 Zeichen)

- **§9** keine E-Mail-Adresse, Telefonnummer oder Anschrift ohne Beleg. Ohne Beleg
  bleibt die Empfängerzeile weg, mit dem Hinweis, sie im Intranet nachzuschlagen.
- **§11** eine neue Prüfung.

## Ergebnisse v11 — A1 zweimal

| Prüfpunkt | Lauf 1 (1:58) | Lauf 2 (1:27) |
|-----------|---------------|---------------|
| keine erfundene Adresse | ✅ | ✅ |
| sagt, wo die Adresse steht | ✅ Intranet-Zeile | ❌ **fehlt** |
| E-Mail ausgeschrieben | ✅ | ✅ |
| Hinweis auf Tz. 5.15 mit Geltungsbereich | ✅ | ✅ |
| Stelle ohne Personennamen | ✅ Z2 Personal, Aufgabengebiet Zeitwirtschaft | ✅ Personalbereich, Quelle als `[…, Z2]` |

Das Verbot hielt zweimal. Die positive Hälfte derselben Regel feuerte nur einmal.
In Lauf 2 steht eine fertige Mail da, ohne dass der Nutzer erfährt, wohin damit.

Ursache: die Intranet-Zeile hing als Nebensatz am Verbot
(„lass die Empfängerzeile weg **und schreib, dass** …"). Der auffällige Teil war
das Weglassen; der nachgestellte Auftrag fiel weg. Dasselbe Muster wie bei
„Biete eine E-Mail an": was am Satzende hängt, wird optional gelesen.

Nebenbefund: die neuen Zusatzzeilen kamen in der Sie-Form heraus, während der
Rest der Antworten duzt. Die Skill hatte die Anrede nie festgelegt.

Zweiter Nebenbefund, noch nicht behoben: Lauf 2 öffnete den
Geschaeftsverteilungsplan gar nicht, zitierte ihn aber trotzdem als
`[Geschaeftsverteilungsplan_HZD, Z2]`. Die Kennung Z2 steht nirgends in der
Skill, kam also aus dem Gedächtnis. Das erklärt zugleich die fehlende
Intranet-Zeile: Abschnitt 9 beginnt mit dem Auftrag, im
Geschäftsverteilungsplan zu suchen — wer den Schritt überspringt, überspringt
den ganzen Block. Die Bibliothek war erreichbar, Lauf 2 las zwei PDFs im
Volltext und zitierte Tz. 5.15 wörtlich; es war also kein Zugriffsproblem.

Bewusst **keine** neue Regel dafür. §4, §9 und §11 verlangen die frische Suche
bereits an drei Stellen; eine vierte Wiederholung ändert nichts. Stattdessen
Beobachtungspunkt für die v12-Runde: zitiert die Antwort eine Datei, die sie im
selben Lauf nicht geöffnet hat? Tritt das erneut auf, wird es gezielt behoben.

## Änderungen v12 (18621 Zeichen)

- **§9** die Intranet-Zeile ist keine Nebenbedingung mehr, sondern eine eigene
  Pflichtzeile mit vorgegebenem Wortlaut: „Die Adresse von [Stelle] findest du
  im Intranet."
- **§7** Anrede festgelegt: du gegenüber dem Nutzer, förmlich nur innerhalb der
  E-Mail-Vorlage.
- **§11** Prüfung erweitert.

## Ergebnisse v12 — A1 zweimal

| Prüfpunkt | Lauf 1 (1:19) | Lauf 2 (0:56) |
|-----------|---------------|---------------|
| Intranet-Zeile | ✅ | ✅ |
| durchgehend du | ✅ | ✅ |
| Internet-Zeile aus §8 | ❌ **fehlt** | ❌ **fehlt** |
| Quelle selbst geöffnet | ✅ GVP gelesen, Z2 Personal daraus | ❌ GVP nicht geöffnet |
| keine erfundene Adresse | ✅ | ✅ |
| Hinweis auf Tz. 5.15 | ✅ | ✅ |

### Selbst verursachter Rückschritt

Die Intranet-Zeile sitzt jetzt zuverlässig, aber sie hat die Internet-Zeile
verdrängt — in **beiden** Läufen. Ursache ist das Wort in v12: „Dann **endet**
die Vorlage immer mit dieser eigenen Zeile". Das Modell las „endet" als Ende der
Antwort und ließ die Zeile aus Abschnitt 8 weg, obwohl Abschnitt 6 sie als letzte
Zeile vorschreibt. Zwei Vorschriften über dieselbe Position, die spätere gewinnt.

### Erfundene Quelle, zweites Mal und schlimmer

Lauf 2 schrieb: `Z2 (Personal und Soziales, Tz. 11 in DA_Arbeitszeit_OH_2.2.1)`.
Der Geschäftsverteilungsplan wurde in diesem Lauf nicht geöffnet. Zitiert ist
eine **andere Datei**: eine Dienstanweisung über Arbeitszeit, die keine
Organisationseinheiten benennt. Auch der Name ist ausgeschmückt — im
Geschäftsverteilungsplan heißt die Einheit „Z2 Personal", nicht „Personal und
Soziales". In der v11-Runde war die Quelle wenigstens noch die richtige Datei.

Damit ist die in der v11-Runde gesetzte Schwelle erreicht: der Fehler ist
wiederholt aufgetreten und hat sich verschlechtert, also wird er jetzt gezielt
behoben — nicht durch eine vierte Wiederholung von „such frisch", sondern durch
eine Zuordnung plus erlaubten Ausweg.

## Änderungen v13 (19 302 Zeichen)

- **§9** die Intranet-Zeile folgt direkt nach der Vorlage und ist ausdrücklich
  **nicht** die letzte Zeile der Antwort.
- **§6** die Kreuz-Reihenfolge ist jetzt vollständig durchnummeriert, alle sieben
  Elemente, mit dem Satz „Keine dieser Zeilen ersetzt eine andere".
- **§9** Quelle für eine Organisationseinheit ist immer der
  Geschaeftsverteilungsplan_HZD und nie eine Dienstanweisung. Wurde er in dieser
  Antwort nicht geöffnet, wird die Stelle **ohne** Quellenangabe genannt, statt
  eine zu konstruieren.
- **§11** neue Prüfung: jede zitierte Datei in dieser Antwort selbst geöffnet?

## Stand

Alle neun Testfälle liefern seit v9 das richtige Verdikt. Was seither noch
auftrat, betraf ausnahmslos die Vollständigkeit und Belegbarkeit der Antwort,
nicht ihre Richtigkeit.

Wiederkehrendes Muster über alle Runden: **eine Anweisung wird nur so zuverlässig
befolgt, wie sie im Dokument positioniert ist.** Was als Nebensatz hängt, wird
optional gelesen (v12). Was eine Position beansprucht, die schon vergeben ist,
verdrängt die ältere Regel (v13). Was keinen Platz im Format hat, fällt weg (v10).

Gegenprobe zu v13: **A1 zweimal**, beide Male müssen Intranet-Zeile **und**
Internet-Zeile stehen, in dieser Reihenfolge, und jede eckige Klammer muss zu
einer in diesem Lauf geöffneten Datei gehören.

## Runde v14 — die Themenkarte schlug vier Mal den gelesenen Text

Vier Kontrollfragen, alle vier mit **Kreuz** beantwortet, alle vier falsch.
Der Suchverlauf desselben Laufs zeigt jedes Mal einen echten Fund:

| Frage | Fund im Lauf | ausgegeben |
|---|---|---|
| Kann ich IT-Ausstattung bestellen? | `Z7 Beschaffung, Lizenzmanagement` — „Beantragungs- und Beschaffungsprozesse für IT- und Non-IT-Bedarfe" | Kreuz |
| Gibt es einen Fortbildungskatalog? | `K2 IT-Fortbildung` — „Organisation und Koordination der Seminarplanung" | Kreuz |
| Gibt es einen Betriebsarzt? | Betriebsarzt namentlich im Geschäftsverteilungsplan, Arbeitsschutzausschuss ASA | Kreuz |
| Gibt es eine Kantine? | Kantinenausschuss im Geschäftsverteilungsplan | Kreuz |

Die Begründung im Lauf benennt die Ursache selbst: *„Laut der Themenkarte sind
alle vier Fragen explizit in der Liste ‚Nicht in der Bibliothek' … Das bedeutet,
ich muss für jede Frage mit Kreuz antworten."*

### Ursache: drei Regeln, die zusammen jeden Fund entwerten

1. Die Negativliste enthielt alle vier Themen und schrieb vor: „Suche höchstens
   zweimal, dann antworte mit Kreuz."
2. Der Satz, der nach dem Sportkurs-Fehler dazukam — „Findest du dabei nur eine
   thematisch benachbarte Organisationseinheit, ist das kein Treffer … Hör dort
   auf zu suchen" — machte aus **jedem** Fund im Geschäftsverteilungsplan einen
   Nicht-Treffer.
3. §5 „Nachbarthema erkennen" bestätigte das ein drittes Mal.

Der zweite Satz stammt aus der vorigen Runde und war als Bremse gegen einen
falschen Haken gedacht. Er bremste stattdessen die richtige Antwort weg. Das ist
derselbe Mechanismus wie bei v13: eine neu eingesetzte Regel verdrängt die
ältere, die an derselben Stelle stand.

### Die fehlende Unterscheidung

Keine der drei Regeln fragt, **was gefragt war**. Dieselbe Fundstelle beantwortet
„Gibt es eine Kantine?" wörtlich und „Wie bestelle ich IT-Ausstattung?" gar
nicht. Ohne diese Unterscheidung muss jede Regel, die für den einen Fall richtig
ist, im anderen falsch sein.

## Änderungen v14 (23 079 Zeichen)

- **§5 Existenzfrage.** Fragt der Nutzer, ob es etwas gibt, ist die Frage
  wörtlich beantwortet, sobald eine Datei die Sache, ein Gremium dafür oder eine
  Organisationseinheit nennt, deren Aufgabe sie ist. Ein Kantinenausschuss belegt
  eine Kantine. Das ist Haken, mit dem Zusatz, was die Unterlagen **nicht** sagen.
- **§5 Abgrenzung.** Ein Satz, der beide Fälle nebeneinanderstellt: wer nach dem
  Verfahren fragt, bekommt bei dieser Fundstelle Gelb; wer nach der Existenz
  fragt, bekommt Haken. „Lies die Frage, bevor du den Modus wählst."
- **§5 Kreuz-Voraussetzung.** Kreuz setzt voraus, dass **keine** Datei die Sache
  erwähnt. „Der gelesene Text schlägt die Themenkarte, immer."
- **§2 Negativliste.** Fünf widerlegte Einträge gestrichen (Kantine,
  Gesundheitsmanagement, Sportkurse, Betriebsarzt, Fortbildungskatalog,
  Bestellung von IT-Ausstattung). Der Satz „Hör dort auf zu suchen" ist ersetzt
  durch einen **Pflichtblick** in den Geschäftsverteilungsplan nach den zwei
  Suchen: findet er etwas, entscheidet der Fund und nicht die Liste.
- **§2 Themenkarte.** Vier neue Zeilen für Beschaffung, Fortbildung,
  Arbeitsschutz und Kantine, jede mit dem ausdrücklichen Zusatz, was die Datei
  **nicht** enthält.
- **§2 Nicht für Arbeitsfragen.** `bisher keine` ersetzt durch das
  Gesundheitstage-Programm plus die Regel: eine Datei ohne Regelungsinhalt ist
  keine Quelle für eine Regel, aber ein Beleg dafür, dass es die Sache gibt.
- **§9 Namensverbot.** Stand bisher nur als Falle in §2 mit Querverweis; der
  Verweis wurde ignoriert. Jetzt vollständig in §9 selbst, samt `ANr.`, samt der
  Anweisung, die Organisationskennung statt der Seitenzahl zu nennen.
- **§11** drei neue Prüffragen dazu.

### Gegenprobe zu v14

Dieselben vier Fragen. Erwartet: Betriebsarzt und Kantine **Haken**,
IT-Ausstattung und Fortbildungskatalog **Haken für die Existenz** mit dem Satz,
dass Bestellweg beziehungsweise Katalog nicht in den Unterlagen stehen. In keiner
der vier Antworten darf ein Personenname, eine `ANr.` oder eine Seitenzahl aus
dem Geschäftsverteilungsplan stehen.
