# skill

Skills für **Vibe** (vibe-hs.steuercloud-hessen.de) — die interne Mistral-Instanz
des hessischen Finanzressorts.

## hausinfo-arbeit

Beantwortet Fragen zum Arbeitsalltag bei der HZD ausschließlich aus der Bibliothek
"Arbeit docs" (9 Dateien), in einfachem Deutsch auf A2/B1-Niveau.

| Datei | Inhalt |
|-------|--------|
| `skills/hausinfo-arbeit/SKILL.md` | aktuelle Fassung (v13) |
| `skills/hausinfo-arbeit/versions/` | v4, v6, v7, v8, v9, v10, v11, v12 zum Vergleich |
| `skills/hausinfo-arbeit/TESTS.md` | Testfälle, Ergebnisse, Ursachenanalyse |

### Versionen

| Version | Zeichen | Was dazukam |
|---------|---------|-------------|
| v4 | 10 547 | Abschnitte 1–10 |
| v5 | 12 025 | + Selbstprüfung, + E-Mail-Vorlagen |
| v6 | 13 090 | Abschnitt 5 neu: Modus bewertet die gestellte Frage, Geltungsbereich, kein Ersatz, Schweigen ist kein Nein |
| v7 | 15 974 | Widersprüche zwischen §2/§5 und zwischen §6/§8/§9 aufgelöst; Negativliste; Lückensatz-Pflicht bei 🟡 |
| v8 | 16 335 | keine Personennamen; E-Mail wird ausgeschrieben statt angeboten |
| v9 | 16 916 | kein „Nein" in der Kurz-Zeile bei ❌; Nachbartreffer beendet die Suche; keine Personalnummern |
| v10 | 17 932 | Hinweis-Block bei ❌ für dokumentierte Verweise; keine erfundenen Organisationseinheiten |
| v11 | 18 329 | keine erfundenen E-Mail-Adressen oder Telefonnummern |
| v12 | 18 621 | Intranet-Zeile als Pflichtzeile statt Nebensatz; Anrede du festgelegt |
| v13 | 19 302 | Kreuz-Reihenfolge vollständig nummeriert; Organisationseinheit nur aus dem Geschäftsverteilungsplan |

## dokumentenkarte-pflegen

Hält Abschnitt 2 von `hausinfo-arbeit` aktuell, wenn Dateien in der Bibliothek
dazukommen, verschwinden oder umbenannt werden. Trägt den neuen Abschnitt nach
Rückfrage selbst ein, per `search_replace` auf
`/home/user/skills/hausinfo-arbeit/SKILL.md`, und ändert nichts anderes.

| Datei | Inhalt |
|-------|--------|
| `skills/dokumentenkarte-pflegen/SKILL.md` | aktuelle Fassung (v8), eine Datei zum Hochladen |

Die Datei wird als Ganzes hochgeladen. Das YAML-Frontmatter mit `name` und
`description` muss deshalb drin bleiben, sonst weist Vibe die Datei zurück.
Der Text darunter kommt dagegen ohne Markdown-Syntax aus: keine Überschriften
mit Raute, keine Aufzählungsstriche. Abschnitte stehen als
Großbuchstabenzeilen, Listen als eingerückte Wortmarken. Grund ist die
Darstellung: beim Zurücklesen aus Vibe verschwanden Überschriften und ganze
Absätze, während Aufzählungen stehen blieben, sodass sich der gespeicherte
Inhalt nicht mehr prüfen ließ. Ohne Markdown-Zeichen ist das Angezeigte gleich
dem Gespeicherten. Prüfzeile am Ende: `ENDE dokumentenkarte-pflegen v8`.

Der vierte Lauf kam erstmals bis zur Rückfrage, lieferte aber einen Abschnitt 2,
der nicht eingetragen werden durfte. Drei Fehler, die alle dieselbe Wurzel haben
— eine Zahl oder eine Prüfung, die sich auf die Karte statt auf die Bibliothek
bezog:

- Die Stand-Zeile trug `12 Dateien`, die Zahl der Kartenzeilen, statt der 19
  Dateien der Bibliothek. Dieselbe falsche Zahl wanderte in die Einleitung der
  Negativliste, wo sie zur Behauptung wird, alle zwölf Dateien seien geprüft.
- Abschnitt 5 wurde still übersprungen. Das in zwei früheren Läufen erkannte,
  nicht mehr vorhandene `Informationsblatt_Datenschutz_Vitero_HZD` blieb in der
  Vitero-Zeile stehen.
- Prüfung 3 und 4 meldeten beide grün, obwohl genau diese beiden Fehler in ihren
  Zuständigkeitsbereich fielen. Sie fragten zu unbestimmt.

In v8 nennt Abschnitt 8 die Herkunft der Zahl ausdrücklich (`die Zahl aus
Schritt 1`, nicht die Zeilenzahl), läuft Abschnitt 5 in jedem Lauf mit
Pflichtausgabe `verschwunden keine`, und die Prüfungen 3 und 4 verlangen einen
Abgleich Zeile für Zeile gegen die Liste aus Schritt 1. Dazu die Regel, die
bestehende Reihenfolge der Themenkarte nicht umzusortieren — der Lauf hatte sie
alphabetisch neu geordnet.

Der dritte Lauf kam bis zur Selbstprüfung: Auswahl rechtzeitig auf drei begrenzt,
nur diese drei gelesen, alle drei korrekt eingeordnet, das fehlende
`Informationsblatt_Datenschutz_Vitero_HZD` erkannt und das `beide lesen` in der
Vitero-Zeile entfernt, Stand-Zeile und Restzähler richtig gerechnet. Gescheitert
ist er an einem Widerspruch in diesem Skill: der Block **Nicht für Arbeitsfragen**
musste angelegt werden, durfte laut Grenze 1 aber nicht aus den gesperrten
Dateien gefüllt werden, und leer sein war nirgends erlaubt. In v7 steht daher
ausdrücklich, dass ein leerer Block vollständig ist — die Überschrift genügt,
darunter kommt `bisher keine`, und der Behälter füllt sich über die folgenden
Läufe.

Der zweite Lauf blieb im Rahmen: keine Wiederholungen, keine Doppellesungen,
und er fand einen echten Fehler — `Informationsblatt_Datenschutz_Vitero_HZD`
wird in der Themenkarte referenziert, liegt aber nicht mehr in der Bibliothek.
Abgebrochen ist er trotzdem, weil die Aufwandsgrenze zu spät griff: erst wurden
alle zwölf neuen Dateien eingeordnet, dann die Auswahl auf drei beschränkt. In
v6 fällt die Auswahl deshalb direkt nach dem Namensvergleich und vor dem ersten
Blick in eine Datei; die übrigen sind für den Lauf nicht mehr vorhanden. Die
Prüfung der Liste **Nicht in der Bibliothek** läuft nur noch gegen die Dateien
dieses Laufs statt gegen die ganze Bibliothek, und der Namensvergleich ignoriert
`.pdf`, ein angehängtes `(1)` und Groß- oder Kleinschreibung.

Der erste Lauf mit echtem Zuwachs (9 auf 19 Dateien) scheiterte: der Skill
öffnete Dokumente über vierzig Mal, wiederholte dieselben Bewertungen und brach
nach knapp sieben Minuten mitten im Satz ab, ohne etwas einzutragen. Ursache war
eine fehlende Aufwandsgrenze — §3 verlangte, jede neue Datei zu öffnen, und bei
zehn neuen Dateien, darunter mehrere sehr große, trägt das nicht. Deshalb steht
in v5 ein Abschnitt 0 über allem: höchstens drei neue Dateien pro Lauf, jede
Datei höchstens einmal öffnen, abgeschnittene Ausgabe akzeptieren statt
nachzuladen, und bei Wiederholung sofort entscheiden. Ein teilweise gepflegter,
aber eingetragener Abschnitt 2 schlägt einen Lauf, der nichts erreicht.

Dazu kam ein zweiter Befund: der Lauf sortierte von sich aus Dateien als
"nicht relevant" aus (ein Programmheft, zwei Strategiepapiere), ohne dass es
dafür einen Platz gab. Solche Dateien würden bei jedem weiteren Lauf erneut
gelesen und von `hausinfo-arbeit` als unbekannt gemeldet. Abschnitt 2 bekommt
deshalb einen vierten Block, **Nicht für Arbeitsfragen**, mit Dateiname und
einer Zeile Begründung.

Weil der Skill jetzt in eine Datei schreibt, die täglich benutzt wird, sitzen
zwischen Bauen und Schreiben zwei Sperren: eine mechanische Selbstprüfung mit
sechs Fragen (§8) und eine Rückfrage beim Nutzer (§9). Nach dem Schreiben wird
die Datei erneut gelesen und geprüft, ob Abschnitt 1, die Überschrift von
Abschnitt 3, die neue Stand-Zeile und die Schlusszeile stehen. Scheitert etwas
davon, gibt der Skill den Text zur Handarbeit aus statt einen zweiten
Schreibversuch zu starten.

Der Anschluss an `hausinfo-arbeit` braucht keine Änderung an dessen Datei:
§10 verweist den Nutzer bereits auf das Stichwort **Dokumentenkarte aktualisieren**,
und die Beschreibung dieses Skills löst genau darauf aus.
