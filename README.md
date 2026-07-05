# AI Ticket Triage — UI

A minimal console-style interface for the [AI Ticket Triage API](https://github.com/dhanibaksh777-byte/ai-ticket-triage-api). Paste a support message, get it classified instantly.

**Live demo:** https://ai-ticket-triage-ui.vercel.app

## What it does

Type a support ticket into the intake box and it comes back tagged with:
- **Category** — billing, technical, account, or general
- **Priority** — low, medium, high, or urgent
- **Sentiment** — positive, neutral, or negative
- **Summary** — a one-line breakdown of the issue

The result renders as a stamped ticket card, color-coded by priority and sentiment.

## Tech stack

Plain HTML, CSS, and JavaScript — no framework, no build step. Talks directly to the FastAPI backend via `fetch()`.

## Backend

This UI is a thin client for a separate API that handles the actual classification:
👉 [ai-ticket-triage-api](https://github.com/dhanibaksh777-byte/ai-ticket-triage-api)

## Run locally

Open `index.html` directly in a browser. It's already pointed at the live backend, so no local server is needed.

If you want to point it at your own backend instead, update this line in `index.html`:

```javascript
const API_URL = "https://ai-ticket-triage-api.onrender.com/classify";
```
