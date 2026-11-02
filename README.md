# Arnav Wadhwa — portfolio site

Ready for GitHub Pages: `index.html` plus one image in `assets/`.

Upload both, keeping the folder:

```
index.html
assets/
  arnav-booth.jpg
```

It has two views, with a **Frontend / Backend** switch at the top of each:

- **Frontend** (the default): a regular website with four pages: Home, About me, Projects and Contact.
- **Backend**: the same content as a code editor, with five files and a working terminal:
  - `index.tsx` (home)
  - `about.md`
  - `projects.json`
  - `contact.ts`, which has the message form built in
  - `README.md`, a short description of the site
  - `assets/arnav-booth.jpg`, the photo on the About page, shown in an image viewer. `about.md` points to it with `<img src="assets/arnav-booth.jpg">`.

Every frontend page also has a "view source" link that opens the matching file in the backend. Switching views keeps your place: the About page opens `about.md`, and so on.

## Contact form

Both views have a message form. Messages go through Web3Forms (free plan) to the email you used to create the access key. The key is already in `index.html`, near the top of the `<script>`:

```js
const WEB3FORMS_ACCESS_KEY = "…";
```

The key is safe in a public page: it can only send messages *to* you, never read anything.

## Publish on GitHub Pages

1. Create a repo (for example `portfolio`) and add `index.html` and the `assets` folder.
2. Repo → **Settings → Pages** → Source: **Deploy from a branch**, branch `main`, folder `/ (root)` → Save.
3. The site appears at `https://wadhwaa28.github.io/portfolio/` after a minute or two.
   (Name the repo `wadhwaa28.github.io` to put it at the root: `https://wadhwaa28.github.io/`.)

Send yourself a test message from the live site.

## Direct links

Frontend pages:

- `…/#home`
- `…/#about`
- `…/#projects`
- `…/#contact`

Backend files:

- `…/#code-home`
- `…/#code-about`
- `…/#code-projects`
- `…/#code-contact`
- `…/#readme`

## How the contact form works

- A visitor fills in their name, email, topic and message, then presses **Send message** (or Ctrl+Enter).
- You get an email titled `Portfolio message: <topic> from <name>`. Hitting **Reply** answers the visitor directly.
- Below the form, each visitor sees what they've sent from their browser, kept only on their device.
- **Spam protection:** a hidden bot-check field, plus one message every 30 seconds per visitor.
- **Free plan:** 250 messages a month, and no automatic "got your message" email to the sender.
