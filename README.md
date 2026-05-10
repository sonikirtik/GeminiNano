# NANO_LOCAL — Chat with Chrome's Built-in AI, Offline

> A single HTML file that lets you talk to Google's Gemini Nano model running **locally inside your Chrome browser** — no internet, no API key, no server.
---
## What Is This?

Google Chrome silently ships with a local AI model called **Gemini Nano**. It lives on your machine and can run completely offline. This tool gives it a clean chat interface you can use right now — no installation required.

---

## Before You Start — Enable the Required Flags

> ⚠️ **This step is mandatory.** The model will not work until you enable these flags in Chrome.

You need to enable **3 flags** in Chrome. The app's Settings panel (top right corner) will show you exactly which ones and whether they are detected.

### Step-by-step:

**1.** Open the HTML file in Chrome. Click **"Setup & Flags"** in the top right corner.

**2.** For each flag listed, click **Copy** next to the flag URL.

**3.** Open a **new Chrome tab**, paste the URL into the address bar, and press Enter.

**4.** Set the dropdown to **Enabled** (or **Enabled BypassPerfRequirement** if available).

**5.** Click **Relaunch** at the bottom of the flags page.

**6.** Repeat for all 3 flags..

Once all flags are detected, you'll see **"API Ready ✓"** in green at the top left. You're good to go.

---

## How to Use

```
1. Download nano_local.html
2. Double-click the file — it opens in Chrome
3. Enable the flags (see above) if API status shows not ready
4. Type your message and hit Send
```

That's it. No Python, no Node, no server. Just a file.

---

## What the Interface Looks Like

| Main Chat | Settings Panel |
|-----------|---------------|
| Clean dark chat UI | Lists required flags with copy buttons |
| API status shown top left | Step-by-step flag setup guide |
| Send messages to the local model | Memory & cleanup info |

---

## Memory & Cleanup

**Does it free memory when you close the tab?**

**Yes — mostly.** Inference memory and GPU buffers are released when the tab is closed. However, the model weights stay loaded in Chrome's cache until Chrome is fully quit.

**TL;DR:** Close the tab → inference stops. Quit Chrome → model unloads.

To remove the model entirely, clear Chrome's cache or look in your Chrome profile folder under `GeminiNano/`.

---

## Requirements

- Google Chrome (latest version recommended)
- Windows, Mac, or Linux
---

## License

MIT © 2026 Kirtik Soni

---

*Built because Google put a free local AI on your machine. Might as well use it.*
