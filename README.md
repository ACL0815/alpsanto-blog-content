# Alpsanto Blog — öffentliches Source-Repository

Dieses Repository enthält die öffentlichen Markdown-Quellen und Bilder des Alpsanto-Blogs. Die einzige primäre Publishing- und SEO-Version erscheint auf [blog.alpsanto.com](https://blog.alpsanto.com). Artikelquellen und Content-PRs dürfen hier bereits vor dem Website-Release sichtbar sein. Rohimporte, interne Notizen und Zugangsdaten gehören nicht hierher. Die Website veröffentlicht nur separat freigegebene Artikelversionen.

## Aufbau

- `articles/<slug>.md`: eine öffentliche Artikelquelle pro Datei. Der Dateiname entspricht dem stabilen `slug` im Frontmatter.
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
| `draft` | Boolean; `true` ist eine öffentlich sichtbare Vorab-Fassung, die nicht auf der Website erscheint. |

Vor einem Commit: Angaben und Rechte prüfen, Roh-HTML und ausführbare Links aus Markdown entfernen, Bilddateien mit einchecken und `id` sowie `slug` auf Kollisionen prüfen. Ein späterer privater Import nach der [Outrank-Dokumentation](https://www.outrank.so/docs/webhook) erzeugt zunächst nur Kandidaten für eine getrennte redaktionelle Prüfung.

## Artikelverzeichnis

Noch keine Artikelquellen eingestellt. Markdown bleibt eine schlanke Inhaltsquelle ohne zusätzliche SEO-Texte oder Keyword-Blöcke; die Website erzeugt Metadaten und Self-Canonicals.
