---
name: dokumentenkarte-pflegen
description: 'Verwende diesen Skill, wenn der Nutzer Dokumentenkarte aktualisieren, Themenkarte aktualisieren, Dokumentenkarte pruefen oder Abschnitt 2 neu bauen sagt. Ebenso, wenn sich die Bibliothek "Arbeit docs" geaendert hat, also eine Datei dazugekommen, entfernt oder umbenannt wurde, oder wenn der Skill hausinfo-arbeit gemeldet hat, dass die Themenkarte veraltet scheint. Traegt den neuen Abschnitt 2 nach Bestaetigung direkt in hausinfo-arbeit ein.'
---

dokumentenkarte-pflegen

Haelt Abschnitt 2 des Skills hausinfo-arbeit aktuell und traegt ihn nach
Bestaetigung selbst ein. Du aenderst eine Datei, die im taeglichen Gebrauch ist.
Ein falscher Schreibvorgang beschaedigt sie still. Deshalb gilt: erst pruefen,
dann fragen, dann schreiben, dann nachlesen.


ABSCHNITT 0   AUFWANDSGRENZE

Diese Regeln gelten fuer den ganzen Lauf und stehen ueber allen anderen.

Grenze 1   Bearbeite in einem Lauf hoechstens drei neue Dateien. Gibt es mehr,
           nimm die ersten drei aus der Liste, schreibe den Abschnitt 2 mit
           diesen dreien, und sag am Ende: noch N Dateien offen, sag
           weitermachen fuer die naechsten drei. Ein unvollstaendiger, aber
           eingetragener Abschnitt 2 ist besser als ein Lauf, der nichts
           erreicht.

Grenze 2   Oeffne jede Datei hoechstens einmal pro Lauf. Wird die Ausgabe
           abgeschnitten, ist das in Ordnung. Der Anfang der Datei reicht.
           Oeffne sie nicht erneut und versuche nicht, den Rest zu bekommen.

Grenze 3   Wiederhole nie eine Ueberlegung, die du schon angestellt hast.
           Merkst du, dass du dieselbe Datei zum zweiten Mal bewertest,
           entscheide dich sofort und geh weiter.

Grenze 4   Kommst du trotzdem nicht durch, brich ab und sag, wie weit du
           gekommen bist. Ein ehrlicher Abbruch ist besser als eine
           abgeschnittene Antwort.


ABSCHNITT 1   IST-STAND UND SOLL-STAND HOLEN

Bibliothek "Arbeit docs", ID 01a05c67-7950-744a-adab-232bcb7d9b24.
listLibraryDocuments und searchLibraryDocuments nehmen libraries_ids als Array,
readLibraryDocument nimmt document_id aus einem Suchtreffer.

Zieldatei ist /home/user/skills/hausinfo-arbeit/SKILL.md

Schritt 1   Ist-Stand. Rufe listLibraryDocuments auf und notiere jeden
Dateinamen. Das ist die Wahrheit ueber die Bibliothek.

Schritt 2   Soll-Stand. Lies die Zieldatei und merke dir Abschnitt 2 im
Wortlaut, mit allen Bloecken, also Themenkarte, Fallen, Nicht fuer Arbeitsfragen
und Nicht in der Bibliothek. Merke dir auch, wie die Ueberschriften dort
geschrieben sind, also ob mit Raute oder ohne. Diesen genauen Wortlaut brauchst
du spaeter zum Ersetzen. Fehlt der Block Nicht fuer Arbeitsfragen, gibt es ihn
in dieser Fassung noch nicht, und du legst ihn neu an.

Schritt 3   Scheitert Schritt 1, brich ab und bitte den Nutzer, die Bibliothek
anzuhaengen. Scheitert Schritt 2, brich ab und sag, dass du die Zieldatei nicht
lesen konntest. Arbeite nie mit einem geratenen Soll-Stand und nie mit einem
Abschnitt 2 aus deinem Gedaechtnis. Schreibe nie in eine Datei, die du in
diesem Lauf nicht selbst gelesen hast.


ABSCHNITT 2   VERGLEICHEN

Ordne jede Datei genau einer Gruppe zu.

Gruppe unveraendert   steht in der Bibliothek und in Abschnitt 2, gleich in
                      welchem Block.
Gruppe neu            steht in der Bibliothek, aber in keinem Block von
                      Abschnitt 2.
Gruppe verschwunden   steht in Abschnitt 2, aber nicht mehr in der Bibliothek.
Gruppe umbenannt      ein neuer und ein verschwundener Name, und die neue Datei
                      behandelt dasselbe Thema. Pruefe das durch Lesen, nicht
                      durch Namensaehnlichkeit.

Ist alles unveraendert, gib nur einen Satz aus: die Dokumentenkarte ist aktuell,
N Dateien, keine Aenderung. Dann hoere auf. Schreibe in diesem Fall nichts und
gib auch keinen Abschnitt 2 aus.

Sind es mehr als drei neue Dateien, gilt Grenze 1 aus Abschnitt 0. Sag gleich
zu Beginn, wie viele neu sind und welche drei du in diesem Lauf nimmst.


ABSCHNITT 3   NEUE DATEI EINORDNEN

Rate ein Thema nie aus dem Dateinamen, auch wenn der Name eindeutig aussieht.
Aber lies auch nicht mehr, als du zum Einordnen brauchst.

Weg 1, zuerst   Rufe searchLibraryDocuments mit dem Thema oder dem Dateinamen
                als query auf und lies die Treffer aus dieser Datei. Meist
                stehen Titel, Zielsetzung und Geltungsbereich schon darin.

Weg 2, nur wenn Weg 1 nicht reicht   Oeffne die Datei einmal mit
                readLibraryDocument und lies den Anfang. Nicht mehr, kein
                zweiter Versuch.

Notiere vier Dinge.

Erstens    Titel und Zielsetzung, also was die Datei regelt.
Zweitens   Suchwoerter aus den Ueberschriften der Datei, nicht aus deiner
           Erwartung.
Drittens   Geltungsbereich, also fuer wen die Datei gilt. Steht dort HZD, gilt
           sie nicht fuer Finanzaemter, und umgekehrt. Das ist die wichtigste
           Angabe, weil eine Regel im falschen Geltungsbereich eine Frage nicht
           beantwortet.
Viertens   Stand oder Datum, wenn erkennbar.

Bau daraus eine Zeile im Stil der bestehenden Zeilen: Suchwoerter mit Komma,
Doppelpunkt, dann der Dateiname. Deckt die neue Datei ein Thema ab, das eine
bestehende Datei nur teilweise regelt, schreib bei beiden Zeilen "beide lesen"
dazu und sag, welche Datei welchen Teil beantwortet.

Ist der Geltungsbereich nach dem Lesen unklar, nimm die Datei trotzdem auf und
schreib die offene Frage in den Aenderungsbericht. Erfinde keinen
Geltungsbereich.


ABSCHNITT 4   DATEIEN OHNE REGELUNGSINHALT

Manche Dateien in der Bibliothek beantworten keine Frage zum Arbeitsalltag.
Sie gehoeren nicht in die Themenkarte, aber sie muessen trotzdem verzeichnet
werden, sonst liest der naechste Lauf sie wieder und hausinfo-arbeit meldet sie
als unbekannt.

Solche Dateien kommen in den Block Nicht fuer Arbeitsfragen, mit dem Dateinamen
und einer Zeile Begruendung. Drei Arten sind gemeint.

Art 1   Veranstaltungsprogramme und Termine, etwa ein Programmheft.
Art 2   Strategiepapiere, Agenden und Fortschrittsberichte ohne Regelungen.
Art 3   Doppelte oder aeltere Fassungen einer Datei, die schon in der
        Themenkarte steht.

Alles andere kommt in die Themenkarte. Im Zweifel Themenkarte, denn eine
ueberfluessige Zeile kostet nur eine Suche, eine fehlende Zeile kostet eine
Antwort.

Ein Programmheft ist zwar keine Regelung, es beweist aber, dass es das Thema
gibt. Steht das Thema in der Liste Nicht in der Bibliothek, streiche es dort
nach Abschnitt 6.


ABSCHNITT 5   VERSCHWUNDENE DATEI

Entferne ihre Zeile, gleich aus welchem Block. Entferne ausserdem jede Falle
und jeden "beide lesen" Hinweis, der sich nur auf diese Datei bezieht. Nennt
eine andere Zeile diese Datei als zweite Quelle, streiche dort den Zusatz und
sag es im Aenderungsbericht, weil das Thema danach nur noch halb belegt ist.


ABSCHNITT 6   LISTE NICHT IN DER BIBLIOTHEK PRUEFEN

Diese Liste ist eine Behauptung ueber die Bibliothek und veraltet mit jeder
neuen Datei. Eine falsche Behauptung dort erzeugt eine falsche Kreuz-Antwort.

Suche zu jedem Eintrag der Liste einmal in der Bibliothek. Findest du einen
echten Treffer, also den Begriff selbst und nicht ein Nachbarthema, dann nimm
den Eintrag aus der Liste. Gehoert der Treffer zu einer Datei in der
Themenkarte, schreib dort die Suchwoerter dazu. Gehoert er zu einer Datei aus
dem Block Nicht fuer Arbeitsfragen, sag im Aenderungsbericht, dass es das Thema
gibt, die Datei aber keine Regelung enthaelt.

Ein Nachbarthema ist kein Treffer und der Eintrag bleibt.

Gibt es keine neuen Dateien, ueberspringe diesen Abschnitt.


ABSCHNITT 7   FALLEN

Uebernimm jede bestehende Falle woertlich, ausser die Datei, um die es geht,
ist verschwunden.

Nimm eine neue Falle nur mit Beleg aus dem gelesenen Text auf. Drei Anlaesse
rechtfertigen eine.

Anlass 1   Die Datei schraenkt eine Regel im eigenen Wortlaut ein, etwa auf
           mobil erbrachte Arbeitszeit oder auf eine Behoerde. Dann nenne den
           einschraenkenden Wortlaut in der Falle.
Anlass 2   Die Datei beschreibt eine Anwendung und enthaelt selbst keine Daten,
           wie das MORADA Handbuch.
Anlass 3   Zwei Dateien benutzen dasselbe Wort fuer verschiedene Dinge, oder
           zwei Dateien regeln dasselbe Thema fuer verschiedene Personenkreise.

Ohne einen dieser Anlaesse keine neue Falle.


ABSCHNITT 8   DEN NEUEN ABSCHNITT 2 BAUEN

Bau den vollstaendigen Abschnitt 2, nicht nur den geaenderten Teil. Er enthaelt
immer alle vier Bloecke in dieser Reihenfolge: die Themenkarte, dann Fallen,
dann Nicht fuer Arbeitsfragen, dann Nicht in der Bibliothek. Auch die
unveraenderten Zeilen und Fallen stehen mit drin. Ein Abschnitt 2 mit einem
fehlenden Block waere schlimmer als keiner, denn er loescht beim Ersetzen still
Regeln, die vorher da waren.

Uebernimm die Ueberschriften genau in der Schreibweise, die du in Schritt 2
gelesen hast. Aendere die Formatierung der Datei nicht.

Die erste Zeile nach der Ueberschrift traegt das heutige Datum und die
wirkliche Anzahl der Dateien in der Bibliothek, im Muster der alten Zeile:
Stand JJJJ-MM-TT, N Dateien. Bist du nach Grenze 1 noch nicht durch, schreib
dahinter: davon M noch nicht eingeordnet.

Die Themenkarte bleibt eine Suchhilfe und wird keine Faktenquelle. Schreib in
eine Zeile nie eine Regel, eine Zahl oder eine Frist aus einer Datei, sondern
nur, wo gesucht werden soll.


ABSCHNITT 9   SELBSTPRUEFUNG VOR DEM SCHREIBEN

Geh diese sechs Fragen durch. Ist eine Antwort nein, schreibe nicht. Sag
stattdessen, welche Pruefung gescheitert ist, und gib den neuen Abschnitt 2 als
Text aus, damit der Nutzer selbst entscheiden kann.

Pruefung 1   Enthaelt mein neuer Abschnitt 2 alle vier Bloecke?
Pruefung 2   Ist jede Falle aus dem alten Abschnitt 2 entweder woertlich
             uebernommen, oder gehoert sie zu einer verschwundenen Datei?
Pruefung 3   Kommt jeder Dateiname aus dem Ist-Stand genau einmal vor, in der
             Themenkarte oder im Block Nicht fuer Arbeitsfragen, und kein Name,
             den es in der Bibliothek nicht gibt? Noch nicht eingeordnete
             Dateien nach Grenze 1 sind hier ausgenommen und stehen im
             Aenderungsbericht.
Pruefung 4   Stimmt die Zahl in der Stand-Zeile mit der wirklichen Anzahl der
             Dateien ueberein?
Pruefung 5   Habe ich zu jeder eingeordneten neuen Datei den Geltungsbereich
             notiert?
Pruefung 6   Beginnt mein Ersetzungstext an der Ueberschrift von Abschnitt 2
             und endet er vor der Ueberschrift von Abschnitt 3, ohne eine
             Zeile aus Abschnitt 1 oder Abschnitt 3 mitzunehmen?


ABSCHNITT 10   EINTRAGEN

Zeig zuerst den Aenderungsbericht, hoechstens acht Zeilen: wie viele Dateien die
Bibliothek hat, was neu eingeordnet wurde, was in den Block Nicht fuer
Arbeitsfragen kam, was aus der Liste Nicht in der Bibliothek gestrichen wurde,
wie viele Dateien noch offen sind, welche Fragen offen bleiben. Bei jeder neu
eingeordneten Datei nenne ihren Geltungsbereich in drei Woertern. Nenne die
alte und die neue Stand-Zeile.

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


ABSCHNITT 11   GRENZEN

Du aenderst nur Abschnitt 2 von hausinfo-arbeit. Die Antwortregeln, die Modi,
das Format und die Zustaendigkeit gehoeren nicht dir. Faellt dir an einem
anderen Abschnitt etwas auf, schreib einen Satz darueber unter den
Aenderungsbericht, aber aendere dort nichts.

Du legst keinen neuen Skill an, loeschst keinen und benennst keinen um. Du
aenderst keine andere Datei als die eine Zieldatei.


ENDE dokumentenkarte-pflegen v5
