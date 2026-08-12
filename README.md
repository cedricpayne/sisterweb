# Rhinnan's Portfolio Site

The live site: **https://cedricpayne.github.io/sisterweb/**

The whole site is one file — [`index.html`](index.html). Every time a change
is saved (committed) to this repository, GitHub automatically republishes the
site within a minute or two. No build steps, no tools to install.

## The easiest way to edit (no code!)

The site has a built-in visual editor:

1. Open the live site and click **Edit Layout** (bottom-right).
2. **Click any text to retype it** — headlines, stats, descriptions, all editable in place.
3. **Drag sections and cards** to reorder them.
4. Click **Export Updated HTML** — it downloads a file called `portfolio-updated.html` with all your changes baked in.
5. On GitHub, open `index.html`, click the pencil icon (✏️), select everything, and paste the contents of the downloaded file over it. Commit.
6. Wait ~1–2 minutes, then refresh the live site (hard refresh: `Ctrl+Shift+R` / `Cmd+Shift+R`).

(Steps 1–4 also work on a copy of the file opened locally — but embeds only
render on the live site.)

## Editing the HTML directly

Open [`index.html`](index.html) on github.com, click the pencil icon, edit,
commit. Everything worth changing is marked with a `✏️ EDIT:` comment —
search the file for `EDIT:` to jump between them.

**Change the password** — search for `var PASSWORD`.
⚠️ The password is visible to anyone who reads the page source, so it keeps out
casual visitors only — don't reuse a real password, and don't put anything truly
private on the site.

**Add an Instagram post** — copy an entire `<div class="card"> ... </div>` block,
paste it next to the others inside the same `<div class="grid">`, then replace the
URL in `data-instgrm-permalink="..."` with the new post's link.

**Swap a YouTube video** — in the iframe's `src`, replace the ID after
`/embed/` with the new video's ID (the part after `watch?v=` in its URL).

**Fix the two remaining TikTok embeds** — the "Sample 2" and "Spotify Partnership"
cards still use short links (`vt.tiktok.com/...`) with no video ID, so they may
show up blank. Fix: open the video in a browser, copy the full URL
(`https://www.tiktok.com/@rhinnanpayne/video/1234567890123456789`), paste it
into `cite="..."`, and put the long number at the end into `data-video-id="..."`.

**Remove a card or section** — delete its whole block, from the opening
`<div class="card"` (or `<section`) down to its matching closing tag.

## Notes

- Instagram/TikTok embeds only render on the live site (or a local web server) —
  they won't load if you just double-click the HTML file on your computer.
- The deploy status is under the **Actions** tab. A green check = published.
