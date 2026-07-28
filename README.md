# Kitchen Recipe Bank

Public, static recipe knowledge packs for **KitchenAI** (ADR-012).

No API server — the mobile/desktop apps download only the modules a user needs
(onboarding prefs: diet, cuisine, region), then keep them offline in SQLite.

## Layout

- `index.json` — catalog + facets (`diets`, `cuisines`, `courses`, `dish_types`, `techniques`, `regions`)
- `packs/*.json` — recipe modules with multi-axis `taxonomy`
- `ATTRIBUTION.md` — source licenses

## CDN (jsDelivr)

```
https://cdn.jsdelivr.net/gh/mahboobmonnamd/kitchen-receipe-bank@main/index.json
https://cdn.jsdelivr.net/gh/mahboobmonnamd/kitchen-receipe-bank@main/packs/<pack-id>.json
```

## Taxonomy

Every recipe must pass KitchenAI `normalizeTaxonomy()` before publish.

Example: **cake** → `courses: [dessert, snack]`, `dish_types: [cake]`, `techniques: [baking]`.

Do **not** add CC BY-NC-SA corpora (e.g. RecipeNLG) to commercial packs.

## Repo

`git@github.com:mahboobmonnamd/kitchen-receipe-bank.git`
