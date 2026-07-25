# governed.software

The site for **[Doctrine-Driven Development (D³)](https://github.com/governed-software/doctrine-driven-development)** —
an engineering discipline in which architectural decisions earn authority through observable evidence.

> Install the engineering discipline, not just the prompt.

## What this repository is

One self-contained `index.html`. No build step, no framework, no dependency, nothing to install.

Two constraints shape it, and both are deliberate:

- **It must work without JavaScript.** The install picker, the Starter/Professional switch, and the
  EN/ES toggle are CSS only — hidden radio inputs plus `:checked` sibling selectors. JavaScript
  enhances exactly one thing, the copy button. Content delivery never depends on it.
- **One authority per fact.** The install commands shown here are the same ones documented in the
  doctrine repository, and `install.sh` is served from there — never copied into this repo. A second
  copy would be a second authority, which the doctrine forbids.

## Local preview

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

To check a state the CSS toggles control, move `checked` between the `tier` or `lang` radio inputs at
the top of `<body>` and reload.

## Deployment

GitHub Pages, published from `main` at the repository root.

- `CNAME` holds the custom domain.
- `.nojekyll` disables Jekyll processing; the page is served exactly as authored.

---

Apache-2.0 · © Rodrigo Vicente — TeamX Agency · [teamx.agency](https://teamx.agency)
