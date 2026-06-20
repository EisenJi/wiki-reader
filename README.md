# Wiki Reader

A dual-pane reading application for EPUB books with LLM Wiki companion pages. Read your book on one side, browse related wiki notes on the other.

## Features

- **Dual-pane layout**: EPUB + Wiki side by side, with draggable divider
- **Persistent state**: Imported books and wiki files survive page refresh via IndexedDB
- **Integrated wiki sidebar**: File tree lives inside the wiki panel, not globally
- **Three themes**: Dark (default), Light, Sepia
- **Research-backed typography**: Georgia serif for EPUB, 18px base, 1.7 line-height
- **Font size controls**: A- / A+ buttons with localStorage persistence
- **Minimal toolbar**: Chapter navigation, progress bar, book title, font/theme controls
- **Back button**: Wiki navigation history (50 entries max) so you can return to guide pages after clicking wikilinks
- **Swap panels**: Physically swaps DOM order for intuitive layout change
- **Responsive**: Mobile-friendly with media queries
- **Keyboard shortcuts**: Escape to close modal

## Usage

1. Open `index.html` in a browser
2. Click **Import** button
3. Select an EPUB file and a wiki directory (containing `.md` files)
4. Read the book on the left, browse wiki notes on the right
5. Click wikilinks in wiki pages to navigate between related pages
6. Use **← Back** to return to previous wiki pages
7. Click **⇄ Swap** to swap the panels
8. Use **A- / A+** to adjust font size
9. Use **🌙 / ☀️ / 📜** to switch themes

## File Structure

```
wiki-reader/
├── index.html          # Single-file application (all CSS, JS, HTML inline)
├── README.md           # This file
├── package.json        # Dependencies (JSZip, etc. for future server use)
└── .gitignore
```

## Technical Details

- **IndexedDB**: Stores EPUB chapters and wiki file contents for persistence across sessions
- **JSZip**: Parses EPUB files (ZIP archives containing HTML chapters)
- **Markdown parser**: Custom lightweight parser supporting headers, lists, links, code, blockquotes, wikilinks, YAML frontmatter
- **No build step**: Pure HTML/CSS/JS, works directly in browser

## Development

```bash
# Install dependencies (for future server features)
npm install

# Serve locally
npx serve .
```

## License

MIT