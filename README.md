# Rhinnan's Portfolio Site

The live site: **https://cedricpayne.github.io/sisterweb/**

The whole site is one file — [`index.html`](index.html). Every time a change
is saved (committed) to this repository, GitHub automatically republishes the
site within a minute or two. No build steps, no tools to install.

## How to edit

1. Open [`index.html`](index.html) on github.com and click the **pencil icon** (✏️) at the top right of the file view.
2. Make your changes (see the cheat sheet below).
3. Click **Commit changes**, write a short note about what you changed, and commit.
4. Wait ~1–2 minutes, then refresh the live site (hard refresh: `Ctrl+Shift+R` / `Cmd+Shift+R`).

Everything you'd want to change is marked in the file with a `✏️ EDIT:` comment —
search the file for `EDIT:` to jump between them.

## Cheat sheet

**Change text** — headlines, descriptions, stats: just find the text and retype it.

**Change the password** — search for `var PASSWORD` near the bottom of the file.
⚠️ The password is visible to anyone who reads the page source, so it keeps out
casual visitors only — don't reuse a real password, and don't put anything truly
private on the site.

**Add an Instagram post** — copy an entire `<div class="card"> ... </div>` block,
paste it next to the others inside the same `<div class="grid">`, then replace the
URL in `data-instgrm-permalink="..."` with the new post's link
(e.g. `https://www.instagram.com/p/XXXXXXXX/`).

**Fix the TikTok embeds** — the two TikTok cards currently use short links
(`vt.tiktok.com/...`) with no video ID, so they may show up blank. To fix:
open the video in a browser, copy the full URL
(`https://www.tiktok.com/@rhinnanpayne/video/1234567890123456789`), paste it
into the `cite="..."` attribute, and put the long number at the end of that URL
into `data-video-id="..."`.

**Remove a card or section** — delete its whole block, from the opening
`<div class="card"` (or `<section`) down to its matching closing tag.

**Reorder sections/cards** — on the live site, click **Edit Layout** (bottom-right),
drag things around, click **Copy Order**, and send that list to whoever is editing
the HTML so they can match it. (Drag-and-drop changes are only visual — they reset
on refresh until the HTML itself is reordered.)

## Notes

- Instagram/TikTok embeds only render on the live site (or a local web server) —
  they won't load if you just double-click the HTML file on your computer.
- The deploy status is under the **Actions** tab. A green check = published.
