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
dazukommen, verschwinden oder umbenannt werden. Liefert einen fertigen
Abschnitt 2 zum Kopieren, ändert nichts anderes.

| Datei | Inhalt |
|-------|--------|
| `skills/dokumentenkarte-pflegen/SKILL.md` | aktuelle Fassung (v3), eine Datei zum Hochladen |

Die Datei wird als Ganzes hochgeladen. Das YAML-Frontmatter mit `name` und
`description` muss deshalb drin bleiben, sonst weist Vibe die Datei zurück.
Der Text darunter kommt dagegen ohne Markdown-Syntax aus: keine Überschriften
mit Raute, keine Aufzählungsstriche. Abschnitte stehen als
Großbuchstabenzeilen, Listen als eingerückte Wortmarken. Grund ist die
Darstellung: beim Zurücklesen aus Vibe verschwanden Überschriften und ganze
Absätze, während Aufzählungen stehen blieben, sodass sich der gespeicherte
Inhalt nicht mehr prüfen ließ. Ohne Markdown-Zeichen ist das Angezeigte gleich
dem Gespeicherten. Prüfzeile am Ende: `ENDE dokumentenkarte-pflegen v3`.

Der Anschluss an `hausinfo-arbeit` braucht keine Änderung an dessen Datei:
§10 verweist den Nutzer bereits auf das Stichwort **Dokumentenkarte aktualisieren**,
und die Beschreibung dieses Skills löst genau darauf aus.
