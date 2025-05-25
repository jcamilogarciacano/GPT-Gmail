# GPT-Gmail
# Gmail Calendar Event Creator (GPT Action)

This repository contains an OpenAPI schema and plugin manifest to enable a **custom GPT Action** that can schedule events in your **Google Calendar** using OAuth2 authentication.

## 🚀 What It Does

This GPT allows you to say things like:

> "Schedule a meeting called 'Team Sync' tomorrow at 10 AM with alice@example.com and bob@example.com."

...and the GPT will use the Google Calendar API to insert the event into your calendar.

---

## 📂 Files in This Repo

| File | Purpose |
|------|---------|
| `openapi.yaml` | Defines the Google Calendar API endpoint used by GPT |
| `.well-known/ai-plugin.json` | Tells ChatGPT how to use the plugin (name, auth, schema URL) |

---

## 🌐 Hosting on GitHub Pages

To use this GPT Action, you need to host the files via **GitHub Pages**:

### 1. Enable GitHub Pages

- Go to your repository: **Settings → Pages**
- Under **“Source”**, choose:
  - Branch: `main`
  - Folder: `/root` (or `/docs` if your files are there)
- GitHub will give you a live URL like:  
  `https://<your-username>.github.io/GPT-Gmail/`

---

### 2. File URLs You Will Need

Update your `ai-plugin.json` to point to the GitHub Pages URLs:

```json
"api": {
  "type": "openapi",
  "url": "https://<yo
