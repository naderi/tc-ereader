# eReader

[English](README.md) | **Deutsch**

Ein Betrachter für PDF, E-Books und Comics (Lister-Plugin) für den [Total Commander](https://www.ghisler.com), 32 und 64 Bit.
F3 auf einer PDF-, EPUB-, FB2/FB3-, MOBI/AZW3- oder Comic-Datei (CBZ, CBR, CB7, CBT), und sie lässt sich direkt lesen – schnell und sparsam, mit Inhaltsverzeichnis, Textsuche, Links und dunklem Design.
PDF-Seiten zeichnet Windows selbst, E-Books werden als fließender Text in einer angenehmen Lesespalte gesetzt. Nativ, keine Laufzeitumgebung, nichts zu installieren außer dem Plugin.

![eReader zeigt ein PDF mit seinen Lesezeichen und den Symbolleisten-Buttons für Zoom, Anpassen, Drehen und Abdunkeln](docs/screenshot.de.png)

## Unterstützte Dateien

- **PDF:** `.pdf` – auch kennwortgeschützte und beschädigte Dateien
- **EPUB:** `.epub`, `.kepub`
- **FictionBook:** `.fb2`, `.fbz`, `.fb3`
- **Mobipocket und Kindle:** `.mobi`, `.azw`, `.azw3`, `.prc`, `.pdb` – MOBI 6, KF8, PalmDOC, eReader (ungeschützt, als reiner Text); Bücher mit Kopierschutz (DRM) können nicht angezeigt werden
- **Comics:** `.cbz`, `.cbr`, `.cb7`, `.cbt` – CBR und CB7 nutzen die UnRAR- und 7-Zip-Bibliotheken des Total Commanders (`UNRAR64.DLL`, `TC7Z64.DLL`; `UNRAR.DLL`, `TC7Z.DLL` für 32 Bit)

## Funktionen

- Inhaltsverzeichnis in einer Seitenleiste: PDF-Lesezeichen, Kapitel und Überschriften von E-Books
- Klickbare Links: Sprünge im Dokument, zurück mit Alt+Links, Webadressen öffnen sich im Browser
- Gehe zu Seite oder Kapitel, Seitenzähler in der Werkzeugleiste, Position im Lister-Titel
- PDF: Seitenbreite, ganze Seite, Originalgröße und freier Zoom; unterschiedlich große Seiten werden einzeln eingepasst
- PDF und Comics: aktuelle Seite oder alle Seiten drehen (Strg+R), für gescannte Dokumente, die quer oder auf dem Kopf stehen
- E-Books: größere und kleinere Schrift, wählbare Schriftart, schmale Textspalte, Bilder, Tabellen und Fußnoten
- Text markieren und kopieren, auch in PDFs mit Textebene
- Miniaturansichten für die Thumbnail-Ansicht des Total Commander (Cover oder erste Seite)
- Helles und dunkles Design (automatisch wie Windows, wie Total Commander oder fest) im Windows-11-Look; im dunklen Design lassen sich auch PDF-Seiten abdunkeln
- Seiten werden im Hintergrund gezeichnet: Der Lister bleibt bedienbar, auch bei großen Büchern
- Buchinfo (Titel, Autor, Reihe, Verlag, Datum, Sprache, ISBN, Beschreibung, Datei) im Info-Dialog (F1) und im Kontextmenü
- Tooltips an allen Symbolleisten-Buttons und an Links; der Info-Button sitzt in der Symbolleiste, das ganze Fenster dient dem Lesen; die Knöpfe lassen sich auch in eine Statusleiste unten verschieben oder ausblenden (*Knöpfe* im Kontextmenü)
- Oberfläche auf Deutsch und Englisch (richtet sich nach der Windows-Sprache)

![Der Info-Dialog mit Titel, Autor, Reihe, Verlag, ISBN und Beschreibung des Buchs](docs/about.de.png)

![eReader zeigt ein EPUB-Buch mit Inhaltsverzeichnis](docs/epub.de.png)

## Download und Installation

1. **`eReader.zip`** aus der [neuesten Version](https://github.com/naderi/tc-ereader/releases/latest) herunterladen.
2. Die ZIP-Datei im Total Commander öffnen (Enter auf der Datei) und die Frage nach der Installation des Plugins bestätigen.

Die Einstellungen liegen in `eReader.ini` neben dem Plugin (alle Schlüssel stehen im Abschnitt [Einstellungen](#einstellungen) und in der `readme.txt` im ZIP). Voraussetzung ist Windows 10 oder 11 (PDF-Seiten zeichnet die in Windows eingebaute PDF-Engine).

## Tasten

| Taste | Aktion |
|---|---|
| F12 oder Strg+T | *Inhaltsverzeichnis* (Seitenleiste) |
| Strg+G | *Gehe zu Seite…* / *Gehe zu Kapitel…* |
| Alt+Links | *Zurück* |
| Strg+1 / Strg+2 / Strg+0 | PDF: *Seitenbreite* / *Ganze Seite* / *Originalgröße* |
| Strg+Plus / Strg+Minus | PDF: *Vergrößern* / *Verkleinern* (auch Strg+Mausrad); E-Books: *Größere Schrift* / *Kleinere Schrift* |
| Strg+R / Strg+Umschalt+R | PDF und Comics: aktuelle Seite / alle Seiten nach rechts *drehen* (mehr im Menü des *Drehen*-Buttons) |
| Strg+3 | PDF und Comics: *Fortlaufendes Scrollen* ein/aus (auch als Button in der Werkzeugleiste, nur bei *Ganze Seite*); ausgeschaltet wird eine Seite nach der anderen gezeigt und Mausrad und Pfeiltasten blättern am Seitenrand weiter |
| Strg+D | *Seiten abdunkeln* (PDF im dunklen Design) |
| Strg+A, Strg+C | *Alles markieren*, *Kopieren* |
| Strg+K | *Textcursor* ein/aus (wie Caret-Navigation im Browser): Pfeiltasten, Pos1/Ende, Bild auf/ab und Strg+Pfeile bewegen ihn durch den Text, Umschalt erweitert die Markierung (PDF und E-Books); die Wahl wird gemerkt, Dateien öffnen dann mit Textcursor |
| F7 | Suchen (Suche des Total Commander) |
| F1 | Info |

Weitere Optionen – *Design*, *Knöpfe*, *Schriftart…*, *Schmale Textspalte* – stehen im Kontextmenü (Rechtsklick).

## Einstellungen

`eReader.ini` (Abschnitt `[eReader]`) wird beim ersten Start neben dem Plugin angelegt. Die meisten Werte lassen sich auch im Lister ändern und werden dann in die Datei zurückgeschrieben.

| Schlüssel | Werte | Bedeutung |
|---|---|---|
| `Theme` | `0` automatisch (Standard), `1` hell, `2` dunkel, `3` nur wie Total Commander | `0` ist dunkel, wenn Total Commander oder Windows dunkel ist |
| `ZoomMode` | `0` Breite anpassen, `1` Seite anpassen, `2` fester Zoom | PDF-Zoom |
| `Zoom` | `10`–`800` (Standard `100`) | PDF-Zoom in Prozent, gilt bei `ZoomMode=2` |
| `Buttons` | `1` oben (Standard), `2` Statusleiste, `0` ausgeblendet | Wo die Knöpfe der Leiste sitzen |
| `Sidebar` | `1` / `0` | Inhaltsverzeichnis anzeigen |
| `DarkPages` | `1` / `0` | PDF-Seiten im dunklen Design abdunkeln |
| `BookFont` | Schriftname, leer = Standard | Schrift für E-Books |
| `BookFontSize` | `6`–`40` (Standard `12`) | Textgröße für E-Books in Punkt |
| `BookNarrow` | `1` / `0` | Schmale Textspalte für E-Books |

## Lizenz

Freeware – kostenlos nutzbar, aber **nicht verkäuflich**. Siehe [LICENSE](LICENSE).

## Unterstützung

Wenn eReader dir Zeit spart, kannst du die Entwicklung auf Ko‑fi unterstützen. ☕

<a href='https://ko-fi.com/N7N123QIX0' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi2.png?v=6' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

---

© 2026 [Ali Naderi](https://github.com/naderi) · [digitalent.dev](https://digitalent.dev/de/)
