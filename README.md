# brand-assets

Hosted brand logo assets for EIA Investments venue + email reporting, served over the
**jsDelivr CDN** so they load in HTML emails (and anywhere else) with no authentication.

**Public repo - logos only, no data.**

## Using a logo

```
https://cdn.jsdelivr.net/gh/eia-investments/brand-assets@main/logos/<file>.png
```

`@main` serves the latest commit. Pin a tag (e.g. `@v1`) if you want cache-bust control.
Raw GitHub URLs also work: `https://raw.githubusercontent.com/eia-investments/brand-assets/main/logos/<file>.png`

## Naming convention

| Pattern | Use |
|---|---|
| `<entity>.png` | **White / reversed** wordmark, for dark backgrounds (the daily-email masthead set) |
| `<entity>-colour.png` | Brand-colour version, for light backgrounds |
| `<entity>-black.png` | Mono dark, for light backgrounds |
| `<entity>-icon.png` | Mark / icon only (no wordmark) |

**The daily venue sales email references the bare `<entity>.png` filenames by URL - never rename or move them.** Add new variants as new files with a suffix.

## Inventory

### White set (dark backgrounds) - `<entity>.png`

Transparent-background PNGs, ~120px tall, one per entity. Loaded by the daily venue sales email masthead.

| File | Entity | Type | Notes |
|------|--------|------|-------|
| `logos/penny-black.png` | Penny Black | Venue | Phase 1 of the daily email |
| `logos/belles.png` | Belles Hot Chicken | Brand | Co-brands with Penny Black (`Penny Black x Belles`) |
| `logos/hightail.png` | Hightail | Venue | |
| `logos/natural-history.png` | Natural History | Venue | |
| `logos/the-mint.png` | The Mint | Venue | |
| `logos/myrtle.png` | Myrtle Wine Bar | Venue | |
| `logos/murmur.png` | Murmur | Venue | |
| `logos/wtb.png` | Welcome to Brunswick | Venue | "4 Pines" co-mark removed, wordmark only |
| `logos/wtt.png` | Welcome to Thornbury | Venue | |
| `logos/abh.png` | ABH Pub Group | Group | |
| `logos/eia.png` | EIA Investments | Parent | |
| `logos/bluerock.png` | BlueRock | Entity | |
| `logos/prime.png` | Prime | Entity | |
| `logos/ai-dojo.png` | AI Dojo | Entity | |
| `logos/workflowmax.png` | WorkflowMax | Entity | ⚠ Needs a proper mono-white master - the coloured roundel flattened when reversed |

No white WTG (Welcome to Group) mark exists yet - use a text wordmark on dark surfaces.

### Light-background set (12/06/2026)

Verified against the Brand Guide workspace (thumbnail-rendered on white before upload). Recoloured files keep the original alpha channel and use the entity's documented brand primary.

| File | Entity | Source | Notes |
|------|--------|--------|-------|
| `logos/abh-colour.png` | ABH Pub Group | Site bundle (webp converted to PNG) | Burgundy wordmark |
| `logos/abh-black.png` | ABH Pub Group | Skill bundle | Mono black wordmark |
| `logos/ai-dojo-icon.png` | AI Dojo | Site bundle | Purple roundhouse "R" mark; works on light or dark |
| `logos/belles-colour.png` | Belles Hot Chicken | Designer bundle | Red diamond lockup |
| `logos/bluerock-colour.png` | BlueRock | Designer bundle | Primary blue + fluro green |
| `logos/bluerock-black.png` | BlueRock | Designer bundle | Secondary mono black |
| `logos/bluerock-icon.png` | BlueRock | Designer bundle | Primary icon, blue + fluro green |
| `logos/eia-black.png` | EIA Investments | Brand bundle | Radial "Everything Is Awesome" wordmark, near-black |
| `logos/hightail-colour.png` | Hightail | EIA portfolio set | Blue outline wordmark |
| `logos/murmur-black.png` | Murmur | Recoloured from white set | Brand black `#100806` |
| `logos/myrtle-colour.png` | Myrtle Wine Bar | Recoloured from white set | Olive `#5C614B`, includes "Wine Bar" descriptor |
| `logos/natural-history-colour.png` | Natural History | Recoloured from white set | Dark green `#115742` |
| `logos/penny-black-black.png` | Penny Black | Recoloured from white set | Mono dark `#1A1A1A` |
| `logos/prime-colour.png` | Prime | Site bundle | Full-colour roundel + navy wordmark |
| `logos/the-mint-colour.png` | The Mint | Recoloured from white set | Forest green `#003928` |
| `logos/workflowmax-colour.png` | WorkflowMax | Site bundle | Full-colour primary (slate + green roundel) |
| `logos/wtb-colour.png` | Welcome to Brunswick | Recoloured from white set | Dark teal `#0F4837`, wordmark only |
| `logos/wtg-colour.png` | Welcome to Group | EIA portfolio set | ⚠ Low-res (190x110) arrow lockup - only WTG mark on file; replace when a master is sourced |
| `logos/wtt-colour.png` | Welcome to Thornbury | Recoloured from white set | Navy `#26467E`, stacked wordmark |

## Adding more logos later

1. Verify the file is a true PNG (`Image.open(p).format == 'PNG'`) - web bundles often ship WEBP with a `.png` extension.
2. Render a thumbnail on the target background colour and look at it before committing.
3. Recolour only to a documented brand colour (alpha-preserving RGB swap).
4. Follow the naming convention above; never touch the existing white set filenames.
5. Update the inventory table in this README.

Source-of-truth process lives in the Brand Guide workspace: `Brand Guide/_skill-updates/HOW-TO-BUILD-A-BRAND-GUIDE.md` (logo sourcing doctrine).

(If the set grows large, group future variants in subfolders like `logos/colour/` - just leave the current white files where they are.)
