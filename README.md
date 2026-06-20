# Wiki Reader

A dual-pane reading application for EPUB books with LLM Wiki companion pages. Read your book on one side, browse related wiki notes on the other.

## Features

- **Dual-pane layout**: EPUB reader on one side, wiki file browser on the other
- **Swap panes**: Toggle which side shows the book vs wiki
- **Resizable divider**: Drag to adjust panel widths
- **File tree navigation**: Browse wiki markdown files like a file system
- **Markdown rendering**: Wiki pages rendered with proper formatting
- **WikiLinks support**: Click `[[page-name]]` links to navigate between wiki pages
- **Chapter navigation**: Previous/Next buttons for EPUB chapters
- **Dark theme**: Easy on the eyes for long reading sessions

## Usage

1. Open `index.html` in a browser
2. Click **Import** to load:
   - An EPUB file (your book)
   - A wiki directory (markdown files from your LLM Wiki)
3. Read the book on one panel, click wiki files on the sidebar to view notes on the other panel
4. Click **Swap** to switch which panel shows the book vs wiki

## Tech Stack

- Pure HTML/CSS/JS (no build step required)
- JSZip for EPUB parsing (loaded from CDN)
- Client-side only — no server needed

## Development

```bash
npm install  # only if you want to serve locally
npx serve .
```

Or just open `index.html` directly in a browser.

## License

MIT
