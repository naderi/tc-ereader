# eReader

**English** | [Deutsch](README.de.md)

A PDF, e-book and comic book viewer (Lister plugin) for [Total Commander](https://www.ghisler.com), 32 and 64 bit.
Press F3 on a PDF, EPUB, FB2, MOBI/AZW3 or CBZ file and read it right there – fast and with little memory, with table of contents, text search, links and a dark design.
PDF pages are rendered by Windows itself, e-books are laid out as flowing text in a comfortable reading column. Native, no runtime, nothing to install besides the plugin.

![eReader showing an EPUB book with its table of contents](docs/screenshot.png)

## Supported files

- **PDF:** `.pdf` – also password-protected and damaged files
- **EPUB:** `.epub`, `.kepub`
- **FictionBook:** `.fb2`, `.fbz`
- **Mobipocket and Kindle:** `.mobi`, `.azw`, `.azw3`, `.prc`, `.pdb` – MOBI 6, KF8, PalmDOC; books with DRM cannot be shown
- **Comic books:** `.cbz`

## Features

- Table of contents in a sidebar: PDF bookmarks, e-book chapters and headings
- Clickable links: jumps within the document, back with Alt+Left, web addresses open in the browser
- Go to page or chapter, page counter in the toolbar, position in the Lister title
- PDF: fit width, fit page, actual size and free zoom; pages of different sizes are each fitted on their own
- E-books: larger and smaller text, selectable font, narrow text column, pictures, tables and footnotes
- Text selection and copying, also in PDFs with a text layer
- Thumbnails for Total Commander's thumbnail view (cover or first page)
- Light and dark design (automatic like Windows, or fixed) in the Windows 11 look; in dark mode PDF pages can be darkened too
- Pages are rendered in the background: the Lister stays responsive, even with large books
- Status bar with title, author, format and page or chapter count
- English and German user interface (follows the Windows language)

## Download and installation

1. Download **`eReader.zip`** from the [latest release](https://github.com/naderi/ereader/releases/latest).
2. Open the ZIP in Total Commander (Enter on the file) and confirm the question whether to install the plugin.

Settings are stored in `eReader.ini` next to the plugin. Requires Windows 10 or 11 (PDF pages are rendered by the PDF engine built into Windows).

## Keys

| Key | Action |
|---|---|
| F12 or Ctrl+T | *Contents* (sidebar) |
| Ctrl+G | *Go to page…* / *Go to chapter…* |
| Alt+Left | *Back* |
| Ctrl+1 / Ctrl+2 / Ctrl+0 | PDF: *Fit width* / *Fit page* / *Actual size* |
| Ctrl+plus / Ctrl+minus | PDF: *Zoom in* / *Zoom out* (also Ctrl+mouse wheel); e-books: *Larger text* / *Smaller text* |
| Ctrl+D | *Darken pages* (PDF in dark mode) |
| Ctrl+A, Ctrl+C | Select all, copy |
| F7 | Find (Total Commander's search) |
| F1 | About |

More options – *Theme*, *Font…*, *Narrow text column* – are in the context menu (right click).

## License

Freeware – free to use, but **not for sale**. See [LICENSE](LICENSE).

## Support

If eReader saves you time, you can support its development on Ko‑fi. ☕

<a href='https://ko-fi.com/N7N123QIX0' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi2.png?v=6' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

---

© 2026 [Ali Naderi](https://github.com/naderi) · [digitalent.dev](https://digitalent.dev/en/)
