# Love Mariama Juices

Static site for [mariamajuices.com](https://www.mariamajuices.com/) — rebuilt from the original Squarespace design so it can be hosted for free on GitHub Pages.

Plain HTML/CSS/JS, no build step. Fonts are Google Fonts (Calistoga + Nunito Sans).

## Editing

- All content is in `index.html`.
- Colors and layout are in `css/style.css` (brand palette is at the top in `:root`).
- Images live in `assets/`.

To preview locally: `python3 -m http.server 4173` in this folder, then open http://localhost:4173.

## Contact form

The form posts to [FormSubmit](https://formsubmit.co/) and delivers to mariamaseret@hotmail.ca.

**One-time activation:** the first time someone submits the form, FormSubmit emails an activation link to mariamaseret@hotmail.ca. Mariama needs to click it once; after that, submissions arrive as regular emails. After activation, FormSubmit provides a random alias endpoint — you can optionally swap it into the form's `action` in `index.html` so the raw address isn't in the HTML.

After submitting, the visitor is redirected back to the site with a "Thank you! I will be in touch!" message.

## Deploying

Hosted on GitHub Pages from the `main` branch. Any push to `main` republishes the site in about a minute. The custom domain is configured via the `CNAME` file plus DNS at the domain registrar:

- `www` CNAME record → `<github-username>.github.io`
- Apex/root `A` records → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153

In the repo's **Settings → Pages**, set the custom domain to `www.mariamajuices.com` and enable **Enforce HTTPS** once the certificate is issued.
