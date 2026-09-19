# Alpsanto Blog-Inhalte

Dieses öffentliche Repository enthält ausschließlich freigegebene, veröffentlichte Markdown-Artikel für [blog.alpsanto.com](https://blog.alpsanto.com). Es enthält keine Entwürfe, Zugangsdaten oder automatisch erzeugten Beispielbeiträge. Der Blog kann bis zum ersten freigegebenen Artikel leer sein.

## Aufbau

- `articles/<slug>.md`: ein veröffentlichter Artikel pro Datei. Der Dateiname entspricht dem stabilen `slug` im Frontmatter.
- `images/<slug>/...`: lokal gespeicherte Bilder eines Artikels. Bildnamen sind klein geschrieben und enthalten keine Leerzeichen. Der Website-Build kopiert sie nach `/images/blog/<slug>/...`; im Markdown werden sie als `/images/blog/<slug>/<datei>` referenziert.
- Veröffentlichte Bilder liegen ausschließlich lokal unter `images/<slug>/`. Bildrechte und Alt-Texte sind vor Veröffentlichung zu prüfen. Externe Bild-URLs aus Importen sind nur Hinweise für eine spätere, geprüfte Übernahme und dürfen nicht direkt als Artikelbild veröffentlicht werden.

Die öffentliche Website rendert nur Dateien aus `articles/` mit `draft: false`. Eine Änderung hier wird erst durch den gesonderten, auf einen konkreten Commit gepinnten Website-Build veröffentlicht.

## Artikelschema

Jede Datei beginnt mit YAML-Frontmatter zwischen zwei `---`-Zeilen. Erforderlich sind `id`, `slug`, `title`, `description`, `publishedAt`, `author`, `tags` und `draft`. Optional sind `updatedAt` und `image`. Danach folgt der Markdown-Inhalt.

| Feld | Format |
| --- | --- |
| `id` | Stabile, eindeutige Zeichenfolge; bei Quellenimporten bleibt die Quellen-ID erhalten. |
| `slug` | Eindeutige URL-Kennung, nur `a-z`, `0-9` und Bindestriche; nach Erstveröffentlichung stabil. |
| `title` | Sichtbare Überschrift. |
| `description` | Kurze Beschreibung für Übersicht und Suchergebnis. |
| `publishedAt` | ISO-8601-Zeitpunkt mit Zeitzone, z. B. `2026-09-19T10:00:00Z`. |
| `updatedAt` | Optionaler ISO-8601-Zeitpunkt der letzten inhaltlichen Änderung. |
| `author` | Freigegebener sichtbarer Autorenname; nicht aus einer Quelle erraten. |
| `tags` | Liste von Zeichenfolgen; leere Liste ist erlaubt. |
| `image` | Optionaler absoluter Website-Pfad unter `/images/blog/<slug>/` zu einer lokalen Rasterdatei (`.png`, `.jpg`, `.jpeg`, `.webp` oder `.avif`). |
| `draft` | Boolean; in diesem öffentlichen Repository immer `false`. |

Vor einem Commit: Angaben und Rechte prüfen, Roh-HTML und ausführbare Links aus Markdown entfernen, Bilddateien mit einchecken und `id` sowie `slug` auf Kollisionen prüfen. Ein späterer privater Import nach der [Outrank-Dokumentation](https://www.outrank.so/docs/webhook) erzeugt zunächst nur Kandidaten für eine getrennte redaktionelle Prüfung.

## Artikelverzeichnis

Noch keine Artikel veröffentlicht. Neue Artikel werden hier mit Titel, Markdown-Datei und Blog-URL verlinkt.
