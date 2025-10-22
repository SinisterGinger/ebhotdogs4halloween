# EB Halloween Hotdogs — Netlify Forms (Git-ready)

Bilingual static site with Netlify Forms (no backend). Pricing: **$10 meal**, **$3 extras**.

## Files
- `index.html` — form (`data-netlify="true"`) + hidden `subject` + live total
- `thanks.html` — confirmation page
- `thanks/index.html` — allows `/thanks`
- `_redirects` — maps `/thanks` → `/thanks.html`
- `netlify.toml` — publish root and redundant redirect
- `README.md` — you’re reading it

## Deploy via Git (recommended)
1. Create a new GitHub repo: `ebhotdogs4halloween`
2. Add these files to the repo root and commit:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: EB Hotdogs FR/EN form"
   git branch -M main
   git remote add origin https://github.com/<your-username>/ebhotdogs4halloween.git
   git push -u origin main
   ```
3. Netlify → **Add new site → Import from Git** → connect your repo
   - **Build command:** _none_
   - **Publish directory:** `/` (root)
4. Visit the site and submit one test to register the `hotdogs` form.

## Email notifications
Netlify → Site → **Project configuration → Notifications → Form submission notifications**
- Event: New form submission
- Form: `hotdogs`
- Recipients: `r.kuzmin@hotmail.com, directioneb@csftno.com, pierre.cook@csftno.com`

## CSV export
Netlify → **Forms** → `hotdogs` → Export CSV.

## Tweaks
- Make parent email required by adding `required` to `<input name="email">`.
- Edit the subject line in the hidden `subject` field.
