# Inventory Pipeline

A Mario-themed mobile web app to track your freezer inventory — add, sort, complete, and delete items, all stored locally in your phone's browser at zero cost.

---

## Features

- **Splash page** — Mario-style home screen to navigate sections
- **Freezer Inventory** — table view with 4 columns: Category, Date, Item, Notes
- **Sortable columns** — tap any column header to sort A→Z or Z→A
- **Add items** — bottom-sheet form with category dropdown, date picker, and notes
- **Custom categories** — add your own categories or delete existing ones
- **Task completion** — check off an item to gray it out and move it to the bottom
- **Delete** — trash icon appears on completed rows for permanent removal
- **Offline-ready** — all data stored in your browser via `localStorage`, no internet needed after first load

---

## Tech Stack

| Layer | Choice |
|---|---|
| Frontend | Vanilla HTML5 + CSS3 + JavaScript (ES6) |
| Storage | Browser `localStorage` — no backend, no database |
| Font | [Press Start 2P](https://fonts.google.com/specimen/Press+Start+2P) (Google Fonts) |
| Hosting | GitHub Pages (GHE) |

**No frameworks. No build step. No monthly cost.**

---

## File Structure

```
project/kitchen/
├── index.html      ← Splash page (KITCHEN + TBD buttons)
├── freezer.html    ← Freezer inventory table + add-item form + category manager
└── style.css       ← Shared Mario theme (sky, ground, pipes, clouds, pixel font)
```

---

## localStorage Keys

| Key | Contents |
|---|---|
| `freezer_items` | Array of `{ id, category, date, item, note, completed }` |
| `freezer_categories` | Array of category name strings (sorted A–Z) |

---

## Getting Started (new machine)

```bash
# 1. Clone the repo
git clone https://ghe.megaleo.com/nina-sarmiento/miap_project.git

# 2. Open the app
open miap_project/project/kitchen/index.html
```

Or install the **Live Server** extension in VS Code, right-click `index.html` → *Open with Live Server* for auto-reload while editing.

---

## Pushing Changes

```bash
cd miap_project
git add project/kitchen/
git commit -m "Your message here"
git push origin master
```

---

## Roadmap

- [x] Freezer inventory table with sorting
- [x] Add / delete custom categories
- [x] Task-completion workflow (check off, move to bottom, delete)
- [ ] GitHub Pages live URL
- [ ] Ingredient Checker — paste a recipe, highlight what's missing from inventory
- [ ] Pantry inventory section (TBD button)
