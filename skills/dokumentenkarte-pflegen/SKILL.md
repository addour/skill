dokumentenkarte-pflegen

Haelt Abschnitt 2 des Skills hausinfo-arbeit aktuell. Der Nutzer bearbeitet
Skills in einem Webformular, deshalb ist das Ergebnis immer ein vollstaendiger,
fertig formatierter Abschnitt 2 zum Kopieren. Gib nie einen anderen Abschnitt
aus und schlage keine Aenderung an einem anderen Abschnitt vor.


ABSCHNITT 1   IST-STAND UND SOLL-STAND HOLEN

Bibliothek "Arbeit docs", ID 01a05c67-7950-744a-adab-232bcb7d9b24.
listLibraryDocuments und searchLibraryDocuments nehmen libraries_ids als Array,
readLibraryDocument nimmt document_id aus einem Suchtreffer.

Schritt 1   Ist-Stand. Rufe listLibraryDocuments auf und notiere jeden
Dateinamen. Das ist die Wahrheit ueber die Bibliothek.

Schritt 2   Soll-Stand. Lade den Skill hausinfo-arbeit und lies daraus
Abschnitt 2 mit allen drei Bloecken, also Themenkarte, Fallen und Nicht in
der Bibliothek.

Schritt 3   Scheitert Schritt 1, brich ab und bitte den Nutzer, die Bibliothek
anzuhaengen. Scheitert Schritt 2, bitte ihn, den aktuellen Abschnitt 2 in den
Chat zu kopieren. Arbeite nie mit einem geratenen Soll-Stand und nie mit einem
Abschnitt 2 aus deinem Gedaechtnis.


ABSCHNITT 2   VERGLEICHEN

Ordne jede Datei genau einer Gruppe zu.

Gruppe unveraendert   steht in der Bibliothek und in Abschnitt 2.
Gruppe neu            steht in der Bibliothek, aber in keiner Zeile von
                      Abschnitt 2.
Gruppe verschwunden   steht in Abschnitt 2, aber nicht mehr in der Bibliothek.
Gruppe umbenannt      ein neuer und ein verschwundener Name, und die neue Datei
                      behandelt dasselbe Thema. Pruefe das durch Lesen, nicht
                      durch Namensaehnlichkeit.

Ist alles unveraendert, gib nur einen Satz aus: die Dokumentenkarte ist aktuell,
N Dateien, keine Aenderung. Dann hoere auf. Gib in diesem Fall keinen
Abschnitt 2 aus.


ABSCHNITT 3   NEUE DATEI EINORDNEN

Oeffne jede neue Datei mit readLibraryDocument. Rate ein Thema nie aus dem
Dateinamen, auch wenn der Name eindeutig aussieht.

Lies den Anfang und notiere vier Dinge.

Erstens    Titel und Zielsetzung, also was die Datei regelt.
Zweitens   Inhaltsverzeichnis oder Abschnittsueberschriften, daraus werden die
           Suchwoerter.
Drittens   Geltungsbereich, also fuer wen die Datei gilt. Steht dort HZD, gilt
           sie nicht fuer Finanzaemter, und umgekehrt. Das ist die wichtigste
           Angabe, weil eine Regel im falschen Geltungsbereich eine Frage nicht
           beantwortet.
Viertens   Stand oder Datum, wenn erkennbar.

Bau daraus eine Zeile im Stil der bestehenden Zeilen: Suchwoerter mit Komma,
Doppelpunkt, dann der Dateiname. Nimm als Suchwoerter die Woerter, die in der
Datei selbst vorkommen, nicht die, die du erwarten wuerdest. Deckt die neue
Datei ein Thema ab, das eine bestehende Datei nur teilweise regelt, schreib bei
beiden Zeilen "beide lesen" dazu und sag, welche Datei welchen Teil beantwortet.

Ist der Geltungsbereich einer Datei nach dem Lesen unklar, nimm sie mit auf und
schreib die offene Frage in den Aenderungsbericht. Erfinde keinen
Geltungsbereich.


ABSCHNITT 4   VERSCHWUNDENE DATEI

Entferne ihre Zeile. Entferne ausserdem jede Falle und jeden "beide lesen"
Hinweis, der sich nur auf diese Datei bezieht. Nennt eine andere Zeile diese
Datei als zweite Quelle, streiche dort den Zusatz und sag es im
Aenderungsbericht, weil das Thema danach nur noch halb belegt ist.


ABSCHNITT 5   LISTE NICHT IN DER BIBLIOTHEK PRUEFEN

Diese Liste ist eine Behauptung ueber die Bibliothek und veraltet mit jeder
neuen Datei.

Suche zu jedem Eintrag der Liste einmal in der Bibliothek. Findest du einen
echten Treffer, also den Begriff selbst und nicht ein Nachbarthema, dann nimm
den Eintrag aus der Liste und schreib stattdessen eine Zeile in die Themenkarte.
Ein Nachbarthema ist kein Treffer und der Eintrag bleibt.

Gibt es keine neuen Dateien, ueberspringe diesen Abschnitt. Dann kann sich an
der Liste nichts geaendert haben.


ABSCHNITT 6   FALLEN

Uebernimm jede bestehende Falle woertlich, ausser die Datei, um die es geht,
ist verschwunden.

Nimm eine neue Falle nur mit Beleg aus dem gelesenen Text auf. Drei Anlaesse
rechtfertigen eine.

Anlass 1   Die Datei schraenkt eine Regel im eigenen Wortlaut ein, etwa auf
           mobil erbrachte Arbeitszeit oder auf eine Behoerde. Dann nenne den
           einschraenkenden Wortlaut in der Falle.
Anlass 2   Die Datei beschreibt eine Anwendung und enthaelt selbst keine Daten,
           wie das MORADA Handbuch.
Anlass 3   Zwei Dateien benutzen dasselbe Wort fuer verschiedene Dinge.

Ohne einen dieser Anlaesse keine neue Falle.


ABSCHNITT 7   AUSGABE

Genau zwei Teile, in dieser Reihenfolge.

Teil 1   Ein Aenderungsbericht, hoechstens fuenf Zeilen: was neu ist, was weg
         ist, was in der Liste Nicht in der Bibliothek gestrichen wurde, welche
         offenen Fragen bleiben. Bei jeder neuen Datei nenne ihren
         Geltungsbereich in drei Woertern.

Teil 2   Der vollstaendige Abschnitt 2 in einem Codeblock zum Kopieren. Er
         beginnt mit der Ueberschrift und endet vor Abschnitt 3, und er
         enthaelt immer alle drei Bloecke: die Themenkarte, dann Fallen, dann
         Nicht in der Bibliothek. Auch die unveraenderten Zeilen und Fallen
         stehen mit drin, denn der Nutzer ersetzt den ganzen Abschnitt und
         ergaenzt nichts von Hand. Ein Abschnitt 2 mit einem fehlenden Block
         waere schlimmer als keiner.

Die erste Zeile nach der Ueberschrift traegt das heutige Datum und die
wirkliche Anzahl der Dateien: Stand JJJJ MM TT, N Dateien.

Danach eine Zeile: Ersetze in hausinfo-arbeit den ganzen Abschnitt 2 durch
diesen Text und lass alle anderen Abschnitte unveraendert.


ABSCHNITT 8   GRENZEN

Du aenderst nur Abschnitt 2. Die Antwortregeln, die Modi, das Format und die
Zustaendigkeit gehoeren nicht dir. Faellt dir an einem anderen Abschnitt etwas
auf, schreib einen Satz darueber unter den Aenderungsbericht, aber gib keinen
neuen Text dafuer aus.

Die Themenkarte bleibt eine Suchhilfe und wird keine Faktenquelle. Schreib in
eine Zeile nie eine Regel, eine Zahl oder eine Frist aus einer Datei, sondern
nur, wo gesucht werden soll.


ENDE dokumentenkarte-pflegen v2 plain
