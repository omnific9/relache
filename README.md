# Relâche — company site + investor deck

Static site for **Relâche**, the manufacturer of virtual relationships.

- `index.html` — company website
- `deck/index.html` — VC pitch deck (arrow keys / space to navigate)
- `assets/img/` — AI-generated brand imagery (gpt-image-1)

## Deploy to GitHub Pages

```bash
git init && git add -A && git commit -m "Relâche site + deck"
gh repo create relache --public --source=. --push
gh api repos/{owner}/relache/pages -X POST -f build_type=workflow \
  || echo "or: repo Settings → Pages → Deploy from branch → main /(root)"
```

Then visit `https://<user>.github.io/relache/` (deck at `/relache/deck/`).

## Preview locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```
