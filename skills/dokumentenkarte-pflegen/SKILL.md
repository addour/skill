---
name: dokumentenkarte-pflegen
description: 'Verwende diesen Skill, wenn der Nutzer Dokumentenkarte aktualisieren, Themenkarte aktualisieren, Dokumentenkarte prüfen oder Abschnitt 2 neu bauen sagt. Ebenso, wenn sich die Bibliothek "Arbeit docs" geändert hat, also eine Datei dazugekommen, entfernt oder umbenannt wurde, oder wenn der Skill hausinfo-arbeit gemeldet hat, dass die Themenkarte veraltet scheint. Liefert einen fertigen Abschnitt 2 zum Einsetzen in hausinfo-arbeit.'
---

# dokumentenkarte-pflegen

Hält Abschnitt 2 des Skills hausinfo-arbeit aktuell. Der Nutzer bearbeitet Skills in einem Webformular, deshalb ist das Ergebnis immer ein vollständiger, fertig formatierter Abschnitt 2 zum Kopieren. Gib nie einen anderen Abschnitt aus und schlage keine Änderung an einem anderen Abschnitt vor.

## 1. Ist-Stand und Soll-Stand holen

Bibliothek "Arbeit docs", ID 01a05c67-7950-744a-adab-232bcb7d9b24. listLibraryDocuments und searchLibraryDocuments nehmen libraries_ids als Array, readLibraryDocument nimmt document_id aus einem Suchtreffer.

1. Ist-Stand: listLibraryDocuments aufrufen und jeden Dateinamen notieren. Das ist die Wahrheit über die Bibliothek.
2. Soll-Stand: den Skill hausinfo-arbeit laden und daraus Abschnitt 2 mit allen drei Blöcken lesen, also Themenkarte, Fallen und Nicht in der Bibliothek.
3. Scheitert Schritt 1, brich ab und bitte den Nutzer, die Bibliothek anzuhängen. Scheitert Schritt 2, bitte ihn, den aktuellen Abschnitt 2 in den Chat zu kopieren. Arbeite nie mit einem geratenen Soll-Stand und nie mit einem Abschnitt 2 aus deinem Gedächtnis.

## 2. Vergleichen

Ordne jede Datei genau einer Gruppe zu.

- Unverändert: steht in der Bibliothek und in Abschnitt 2.
- Neu: steht in der Bibliothek, aber in keiner Zeile von Abschnitt 2.
- Verschwunden: steht in Abschnitt 2, aber nicht mehr in der Bibliothek.
- Umbenannt: ein neuer und ein verschwundener Name, und die neue Datei behandelt dasselbe Thema. Prüfe das durch Lesen, nicht durch Namensähnlichkeit.

Ist alles unverändert, gib nur einen Satz aus: die Dokumentenkarte ist aktuell, N Dateien, keine Änderung. Dann höre auf. Gib in diesem Fall keinen Abschnitt 2 aus.

## 3. Neue Datei einordnen

Öffne jede neue Datei mit readLibraryDocument. Rate ein Thema nie aus dem Dateinamen, auch wenn der Name eindeutig aussieht.

Lies den Anfang und notiere vier Dinge.

- Titel und Zielsetzung, also was die Datei regelt.
- Inhaltsverzeichnis oder Abschnittsüberschriften, daraus werden die Suchwörter.
- Geltungsbereich, also für wen die Datei gilt. Steht dort HZD, gilt sie nicht für Finanzämter, und umgekehrt. Das ist die wichtigste Angabe, weil eine Regel im falschen Geltungsbereich eine Frage nicht beantwortet.
- Stand oder Datum, wenn erkennbar.

Bau daraus eine Zeile im Stil der bestehenden Zeilen: Suchwörter mit Komma, Doppelpunkt, dann der Dateiname. Nimm als Suchwörter die Wörter, die in der Datei selbst vorkommen, nicht die, die du erwarten würdest. Deckt die neue Datei ein Thema ab, das eine bestehende Datei nur teilweise regelt, schreib bei beiden Zeilen "beide lesen" dazu und sag, welche Datei welchen Teil beantwortet.

Ist der Geltungsbereich einer Datei nach dem Lesen unklar, nimm sie mit auf und schreib die offene Frage in den Änderungsbericht. Erfinde keinen Geltungsbereich.

## 4. Verschwundene Datei

Entferne ihre Zeile. Entferne außerdem jede Falle und jeden "beide lesen"-Hinweis, der sich nur auf diese Datei bezieht. Nennt eine andere Zeile diese Datei als zweite Quelle, streiche dort den Zusatz und sag es im Änderungsbericht, weil das Thema danach nur noch halb belegt ist.

## 5. Liste "Nicht in der Bibliothek" prüfen

Diese Liste ist eine Behauptung über die Bibliothek und veraltet mit jeder neuen Datei.

Suche zu jedem Eintrag der Liste einmal in der Bibliothek. Findest du einen echten Treffer, also den Begriff selbst und nicht ein Nachbarthema, dann nimm den Eintrag aus der Liste und schreib stattdessen eine Zeile in die Themenkarte. Ein Nachbarthema ist kein Treffer und der Eintrag bleibt.

Gibt es keine neuen Dateien, überspringe diesen Abschnitt. Dann kann sich an der Liste nichts geändert haben.

## 6. Fallen

Übernimm jede bestehende Falle wörtlich, außer die Datei, um die es geht, ist verschwunden.

Nimm eine neue Falle nur mit Beleg aus dem gelesenen Text auf. Drei Anlässe rechtfertigen eine:

- Die Datei schränkt eine Regel im eigenen Wortlaut ein, etwa auf mobil erbrachte Arbeitszeit oder auf eine Behörde. Dann nenne den einschränkenden Wortlaut in der Falle.
- Die Datei beschreibt eine Anwendung und enthält selbst keine Daten, wie das MORADA-Handbuch.
- Zwei Dateien benutzen dasselbe Wort für verschiedene Dinge.

Ohne einen dieser Anlässe keine neue Falle.

## 7. Ausgabe

Genau zwei Teile, in dieser Reihenfolge.

Erstens ein Änderungsbericht, höchstens fünf Zeilen: was neu ist, was weg ist, was in der Liste "Nicht in der Bibliothek" gestrichen wurde, welche offenen Fragen bleiben. Bei jeder neuen Datei nenne ihren Geltungsbereich in drei Wörtern.

Zweitens der vollständige Abschnitt 2 in einem Codeblock zum Kopieren. Er beginnt mit der Überschrift und endet vor Abschnitt 3, und er enthält immer alle drei Blöcke: die Themenkarte, dann Fallen, dann Nicht in der Bibliothek. Auch die unveränderten Zeilen und Fallen stehen mit drin, denn der Nutzer ersetzt den ganzen Abschnitt und ergänzt nichts von Hand. Ein Abschnitt 2 mit einem fehlenden Block wäre schlimmer als keiner.

Die erste Zeile nach der Überschrift trägt das heutige Datum und die wirkliche Anzahl der Dateien: Stand JJJJ-MM-TT, N Dateien.

Danach eine Zeile: Ersetze in hausinfo-arbeit den ganzen Abschnitt 2 durch diesen Text und lass alle anderen Abschnitte unverändert.

## 8. Grenzen

Du änderst nur Abschnitt 2. Die Antwortregeln, die Modi, das Format und die Zuständigkeit gehören nicht dir. Fällt dir an einem anderen Abschnitt etwas auf, schreib einen Satz darüber unter den Änderungsbericht, aber gib keinen neuen Text dafür aus.

Die Themenkarte bleibt eine Suchhilfe und wird keine Faktenquelle. Schreib in eine Zeile nie eine Regel, eine Zahl oder eine Frist aus einer Datei, sondern nur, wo gesucht werden soll.

=== ENDE dokumentenkarte-pflegen v1 ===
