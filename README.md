# os-data

Small demo repository that shows how to read basic OS information using Node.js and a tiny static UI under `os-info`.

## Structure

- `index.js` - top-level Node example (uses `node:os`).
- `cjs/` - CommonJS demo files.
- `mjs/` - ESM demo files.
- `os-info/` - small static demo (HTML + CSS + client JS) that shows OS info in the browser.

Inside `os-info/src/` you'll find:
- `index.js` - app entry that wires DOM helpers and utils to the Node `os` module when available.
- `dom.js` - DOM element selectors.
- `utils.js` - small helper functions.

## Run the static demo (os-info)

You can open the static demo in a browser. From the repository root:

```bash
# open the file directly in your browser
xdg-open os-info/index.html
```

Or serve the folder using a simple static server (recommended for some browser features):

```bash
# with Python 3
python3 -m http.server --directory os-info 8000
# then open http://localhost:8000 in your browser
```

## Run the Node demos

Run the top-level Node example:

```bash
node index.js
```

Run the CommonJS demo (if present):

```bash
node cjs/index.js
```

Run the ESM demo (requires Node >= 12 with ESM support):

```bash
node mjs/index.mjs
```

## License

This project is licensed under the MIT License — see the `LICENSE` file.

---

If you want, I can:
- Add a one-line script to `package.json` for serving `os-info`.
- Convert `src` modules to ESM or add more UI interactions (e.g., button listeners).
