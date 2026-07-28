# Kitchen Recipe Bank

Public static recipe packs for **KitchenAI** — no API server.

Apps download modules via jsDelivr; devices keep them in SQLite offline.

## CDN

```
https://cdn.jsdelivr.net/gh/mahboobmonnamd/kitchen-receipe-bank@master/index.json
https://cdn.jsdelivr.net/gh/mahboobmonnamd/kitchen-receipe-bank@master/packs/<pack-id>.json
```

## Layout

- `index.json` — catalog + facets (diets, cuisines, courses, dish_types, techniques, regions)
- `packs/*.json` — recipe modules with multi-axis `taxonomy`
- `ATTRIBUTION.md` — source licenses

## How developers update this repo

**Preferred (KitchenAI monorepo):**

1. Clone/edit [`kitchenAI`](https://github.com/mahboobmonnamd/kitchenAI) → `recipe-packs/`
2. Follow **[RECIPE_BANK.md](https://github.com/mahboobmonnamd/kitchenAI/blob/main/docs/RECIPE_BANK.md)** (checklist + sync)
3. Run `pnpm run publish:recipe-bank` (needs write access here)

**Direct on this repo:**

1. Get collaborator access (or fork + PR)
2. Edit `packs/*.json` + `index.json` (bump `version`, keep stable recipe `id`s)
3. Every recipe needs taxonomy / dish_types (cake → dessert + snack + baking)
4. Update `ATTRIBUTION.md`
5. Push to `master` (or open PR)

## Rules

- Commercial-safe sources only in default packs (see `ATTRIBUTION.md`)
- No RecipeNLG (CC BY-NC-SA) in commercial packs
- Taxonomy is multi-axis — never one category only ([ADR-012](https://github.com/mahboobmonnamd/kitchenAI/blob/main/docs/adr/012-recipe-taxonomy-github-packs.md))

## Repo

`git@github.com:mahboobmonnamd/kitchen-receipe-bank.git`
