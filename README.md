# Until Next Time

A farewell page — a short thank-you note, plus a personal message for each
teammate. Published with GitHub Pages at
<https://manishseagull.github.io/untilnexttime/>.

## Layout

| Path | What it is |
| --- | --- |
| `index.html` | **The live site.** Edit this one. |
| `og-image.png` | Link-preview image used by WhatsApp / LinkedIn / Twitter. |
| `versions/original/index.html` | Frozen earlier version, kept so previously shared `/versions/original/` links still resolve. Not maintained. |

GitHub Pages must be set to serve from the repository root (Settings → Pages →
Branch: `main`, folder: `/ (root)`), otherwise `index.html` will not be found.

## Editing the notes

All the messages live in one clearly-marked block near the top of the `<script>`
tag in `index.html`:

```js
const SHOW_LEADERS = false;

const teamMembers = [
  { name: "Ankita Balyan",
    message: "Ankita, it was lovely having you as part of the team..." },
  ...
];
```

- Names are sorted alphabetically automatically — add new people anywhere in the array.
- **Managers & Leaders** notes live in the `leaders` array, same shape.
  Setting `SHOW_LEADERS = false` hides that section from the page entirely.

## Sharing an individual note

Every person has their own URL, built from their name:

```
https://manishseagull.github.io/untilnexttime/#note/mayur-vaidakar
```

Opening a note puts that URL in the address bar, so it can be copied and sent
to that person directly. The browser's Back button steps back note → list → page.

## Regenerating the link-preview image

`og-image.png` is a 1200×630 screenshot of `og-source.html`. To change it, edit
that file and re-shoot it with any headless Chrome:

```sh
chrome --headless --window-size=1200,630 --screenshot=og-image.png og-source.html
```
