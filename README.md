# Tripsy Help Scout Docs CSS

Custom CSS and local previews for the Tripsy Help Scout Docs site at `tripsy.help`.

## Files

- `custom.css`: the stylesheet deployed to Help Scout Docs.
- `custom-head-code.html`: the non-CSS custom head code, including Beacon setup and the category badge script.
- `helpscout.css`: captured Help Scout base stylesheet used by local preview pages.
- `preview.html`: local preview of the Help Center home page.
- `preview-timezones.html`: local preview of the Timezones article.
- `logo-light.png` and `logo-dark.png`: brand assets referenced by `custom.css` through GitHub raw URLs.

## Setup

Install dependencies:

```sh
npm install
```

Format and check files:

```sh
npm run format
npm run lint
```

## Local Preview

Start a static server from the project root:

```sh
python3 -m http.server 8765 --bind 127.0.0.1
```

Open:

- Home preview: `http://127.0.0.1:8765/preview.html`
- Article preview: `http://127.0.0.1:8765/preview-timezones.html`

The preview pages load the local `custom.css`, so changes to the stylesheet can be tested by refreshing the browser.

## Deploying To Help Scout

1. Copy `custom.css` into the Help Scout Docs custom CSS field.
2. Copy `custom-head-code.html` into the Help Scout Docs custom head code field.
3. Verify `logo-light.png` and `logo-dark.png` are available through the raw GitHub URLs used in `custom.css`.

The local preview files are only for development and should not be pasted into Help Scout.
