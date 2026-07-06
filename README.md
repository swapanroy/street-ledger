# 🥬 Stall Ledger

**Snap a shelf, log the price.**

Stall Ledger turns a photo of a produce shelf into a clean, sortable price ledger. Take a picture of the price tags at a grocery store or farmers market, and AI reads the store name, produce names, and prices straight off the tags — no manual typing.

**[Live demo →](https://swapanroy.github.io/stall-ledger/)**

---

## What it does

- 📸 **Snap or upload a photo** of a shelf with price tags
- 🤖 **AI extracts the data** — store name, produce name, price per item, price per weight
- 📅 **Auto-logs the date** each item was entered
- 🖼️ **Keeps a thumbnail** of the source photo next to each row (click to zoom)
- ✏️ **Edit anything inline** — click any store name to fix or add it, one row or many at once
- ☑️ **Select and manage rows** — select one, select all, remove selected, remove all
- 🔀 **Sort** by date, produce name, or price
- 📤 **Export** the ledger to CSV or Excel
- 🔑 **Bring your own AI** — connect a free Google Gemini key (or your own OpenAI/Claude key), right in the browser

## How to use it

1. Open the [live page](https://swapanroy.github.io/stall-ledger/)
2. Follow the on-screen steps to connect a free AI key (Google Gemini is the easiest — no credit card needed)
3. Take or upload a photo of a shelf with visible price tags
4. Click **Extract prices** and watch the ledger fill in
5. Fix up any store names, sort the list, and export to CSV/Excel whenever you're ready

No installation, no account with us, nothing to sign up for on this site — it's a single static page.

## Privacy & cost

- Your AI key is typed into your own browser and sent **directly** to your chosen provider (Google, OpenAI, or Anthropic) — it never passes through any server of ours, and isn't saved once you close the tab.
- Because everyone uses their own key, running this page costs the site owner **nothing**. Each person's AI usage is billed to their own account, on whatever free tier or plan they already have.

## Tech stack

- Plain HTML, CSS, and JavaScript — no build step, no framework, no dependencies to install
- [SheetJS](https://sheetjs.com/) (loaded from CDN) for Excel export
- Vision-capable LLM APIs (Google Gemini, OpenAI GPT-4o, or Anthropic Claude) called directly from the browser
- Hosted for free on [GitHub Pages](https://pages.github.com/)

## Running it yourself

This is a single self-contained `index.html` file. To run it locally, just open the file in a browser — or clone the repo and serve it however you like:

```bash
git clone https://github.com/swapanroy/stall-ledger.git
cd stall-ledger
# open index.html in your browser, or serve it:
python3 -m http.server 8000
```

To deploy your own copy, fork this repo and enable **GitHub Pages** in the repo settings (Settings → Pages → Deploy from branch → main → root).

## Limitations (it's a proof of concept)

- Data lives only in memory for the current browser tab — refreshing the page clears the ledger. Export to CSV/Excel before closing if you want to keep it.
- Extraction accuracy depends on photo clarity — a straight-on, well-lit shot of the price tags works best.
- Not every AI provider is guaranteed to allow direct browser calls (CORS); if one doesn't work, try another from the settings panel.

## Credits

Built by **Swapan Roy** — [GitHub](https://github.com/swapanroy)

## License
@SwapanRoy 
