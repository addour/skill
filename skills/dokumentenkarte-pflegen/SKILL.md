---
name: dokumentenkarte-pflegen
description: 'Verwende diesen Skill, wenn der Nutzer Dokumentenkarte aktualisieren, Themenkarte aktualisieren, Dokumentenkarte pruefen oder Abschnitt 2 neu bauen sagt. Ebenso, wenn sich die Bibliothek "Arbeit docs" geaendert hat, also eine Datei dazugekommen, entfernt oder umbenannt wurde, oder wenn der Skill hausinfo-arbeit gemeldet hat, dass die Themenkarte veraltet scheint. Traegt den neuen Abschnitt 2 nach Bestaetigung direkt in hausinfo-arbeit ein.'
---

dokumentenkarte-pflegen

Haelt Abschnitt 2 des Skills hausinfo-arbeit aktuell und traegt ihn nach
Bestaetigung selbst ein. Du aenderst eine Datei, die im taeglichen Gebrauch ist.
Ein falscher Schreibvorgang beschaedigt sie still. Deshalb gilt: erst pruefen,
dann fragen, dann schreiben, dann nachlesen.


ABSCHNITT 1   IST-STAND UND SOLL-STAND HOLEN

Bibliothek "Arbeit docs", ID 01a05c67-7950-744a-adab-232bcb7d9b24.
listLibraryDocuments und searchLibraryDocuments nehmen libraries_ids als Array,
readLibraryDocument nimmt document_id aus einem Suchtreffer.

Zieldatei ist /home/user/skills/hausinfo-arbeit/SKILL.md

Schritt 1   Ist-Stand. Rufe listLibraryDocuments auf und notiere jeden
Dateinamen. Das ist die Wahrheit ueber die Bibliothek.

Schritt 2   Soll-Stand. Lies die Zieldatei und merke dir Abschnitt 2 im
Wortlaut, mit allen drei Bloecken, also Themenkarte, Fallen und Nicht in der
Bibliothek. Merke dir dabei auch, wie die Ueberschriften dort geschrieben sind,
also ob mit Raute oder ohne. Diesen genauen Wortlaut brauchst du spaeter zum
Ersetzen.

Schritt 3   Scheitert Schritt 1, brich ab und bitte den Nutzer, die Bibliothek
anzuhaengen. Scheitert Schritt 2, brich ab und sag, dass du die Zieldatei nicht
lesen konntest. Arbeite nie mit einem geratenen Soll-Stand und nie mit einem
Abschnitt 2 aus deinem Gedaechtnis. Schreibe nie in eine Datei, die du in
diesem Lauf nicht selbst gelesen hast.


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
N Dateien, keine Aenderung. Dann hoere auf. Schreibe in diesem Fall nichts und
gib auch keinen Abschnitt 2 aus.


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


ABSCHNITT 7   DEN NEUEN ABSCHNITT 2 BAUEN

Bau den vollstaendigen Abschnitt 2, nicht nur den geaenderten Teil. Er enthaelt
immer alle drei Bloecke in dieser Reihenfolge: die Themenkarte, dann Fallen,
dann Nicht in der Bibliothek. Auch die unveraenderten Zeilen und Fallen stehen
mit drin. Ein Abschnitt 2 mit einem fehlenden Block waere schlimmer als keiner,
denn er loescht beim Ersetzen still Regeln, die vorher da waren.

Uebernimm die Ueberschriften genau in der Schreibweise, die du in Schritt 2
gelesen hast. Aendere die Formatierung der Datei nicht.

Die erste Zeile nach der Ueberschrift traegt das heutige Datum und die
wirkliche Anzahl der Dateien, im Muster der alten Zeile: Stand JJJJ-MM-TT,
N Dateien.

Die Themenkarte bleibt eine Suchhilfe und wird keine Faktenquelle. Schreib in
eine Zeile nie eine Regel, eine Zahl oder eine Frist aus einer Datei, sondern
nur, wo gesucht werden soll.


ABSCHNITT 8   SELBSTPRUEFUNG VOR DEM SCHREIBEN

Geh diese sechs Fragen durch. Ist eine Antwort nein, schreibe nicht. Sag
stattdessen, welche Pruefung gescheitert ist, und gib den neuen Abschnitt 2 als
Text aus, damit der Nutzer selbst entscheiden kann.

Pruefung 1   Enthaelt mein neuer Abschnitt 2 alle drei Bloecke, also
             Themenkarte, Fallen und Nicht in der Bibliothek?
Pruefung 2   Ist jede Falle aus dem alten Abschnitt 2 entweder woertlich
             uebernommen, oder gehoert sie zu einer verschwundenen Datei?
Pruefung 3   Kommt jeder Dateiname aus dem Ist-Stand genau einmal vor, und
             kein Name, den es in der Bibliothek nicht gibt?
Pruefung 4   Stimmt die Zahl in der Stand-Zeile mit der wirklichen Anzahl der
             Dateien ueberein?
Pruefung 5   Habe ich jede neue Datei selbst geoeffnet und ihren
             Geltungsbereich notiert?
Pruefung 6   Beginnt mein Ersetzungstext an der Ueberschrift von Abschnitt 2
             und endet er vor der Ueberschrift von Abschnitt 3, ohne eine
             Zeile aus Abschnitt 1 oder Abschnitt 3 mitzunehmen?


ABSCHNITT 9   EINTRAGEN

Zeig zuerst den Aenderungsbericht, hoechstens fuenf Zeilen: was neu ist, was weg
ist, was in der Liste Nicht in der Bibliothek gestrichen wurde, welche offenen
Fragen bleiben. Bei jeder neuen Datei nenne ihren Geltungsbereich in drei
Woertern. Nenne dazu die alte und die neue Stand-Zeile.

Frag danach in einem Satz: soll ich das jetzt direkt in hausinfo-arbeit
eintragen? Warte auf die Antwort. Schreibe nie ungefragt.

Sagt der Nutzer ja, lade den Skill skill-creator und ersetze mit search_replace
in /home/user/skills/hausinfo-arbeit/SKILL.md genau einen Block: als zu
suchenden Text den alten Abschnitt 2 im Wortlaut aus Schritt 2, als neuen Text
den gebauten Abschnitt 2. Ein einziger Ersetzungsvorgang, kein zweiter. Fasse
keinen anderen Abschnitt an, keine Ueberschrift von Abschnitt 1 oder 3, und
niemals die Frontmatter-Zeilen mit name und description.

Lies danach die Datei erneut und pruefe vier Dinge: steht Abschnitt 1
unveraendert da, steht die Ueberschrift von Abschnitt 3 unveraendert da, steht
die neue Stand-Zeile drin, und steht die Schlusszeile der Datei noch am Ende.
Berichte das Ergebnis in einer Zeile.

Findet search_replace den alten Text nicht, schlaegt der Schreibvorgang fehl,
oder faellt eine der vier Pruefungen negativ aus, sag das offen und gib den
neuen Abschnitt 2 als Text aus, damit der Nutzer ihn selbst einsetzen kann.
Versuche in diesem Fall keinen zweiten Schreibvorgang und repariere nichts auf
Verdacht.


ABSCHNITT 10   GRENZEN

Du aenderst nur Abschnitt 2 von hausinfo-arbeit. Die Antwortregeln, die Modi,
das Format und die Zustaendigkeit gehoeren nicht dir. Faellt dir an einem
anderen Abschnitt etwas auf, schreib einen Satz darueber unter den
Aenderungsbericht, aber aendere dort nichts.

Du legst keinen neuen Skill an, loeschst keinen und benennst keinen um. Du
aenderst keine andere Datei als die eine Zieldatei.


ENDE dokumentenkarte-pflegen v4
