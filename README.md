# brand-assets

Hosted brand logo assets for EIA Investments venue + email reporting, served over the
**jsDelivr CDN** so they load in HTML emails (and anywhere else) with no authentication.

**Public repo - logos only, no data.**

## What's in `/logos/` right now

These are **white (reversed) wordmarks** - the versions for use on **dark backgrounds**.
They're the set currently loaded by the daily venue sales email, whose masthead sits on a
dark brand band. Each is a transparent-background PNG, ~120px tall, one per entity.

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
| `logos/abh.png` | ABH Pub Group | Group | |
| `logos/eia.png` | EIA Investments | Parent | |
| `logos/bluerock.png` | BlueRock | Entity | |
| `logos/prime.png` | Prime | Entity | |
| `logos/ai-dojo.png` | AI Dojo | Entity | |
| `logos/workflowmax.png` | WorkflowMax | Entity | ⚠ Needs a proper **mono-white master** - the coloured roundel flattened when reversed |

> WTT (Welcome to Thornbury) has no packaged logo yet, so the email uses a text wordmark for it.

## Using a logo

```
https://cdn.jsdelivr.net/gh/eia-investments/brand-assets@main/logos/penny-black.png
```

`@main` serves the latest commit. Pin a tag (e.g. `@v1`) if you want cache-bust control.

## Adding more logos later

The files above are the **white** set and use the bare entity name. **The email references
these exact filenames by URL - don't rename or move them.** For other variants, add *new*
files with a suffix so the white set stays put and its URLs keep working:

| Convention | Use |
|---|---|
| `<entity>.png` | **White / reversed** (current default, for dark backgrounds) |
| `<entity>-colour.png` | Full-colour version |
| `<entity>-black.png` | Mono dark, for light backgrounds |
| `<entity>-icon.png` | Mark / icon only (no wordmark) |

(If the set grows large, group future variants in subfolders like `logos/colour/` -
just leave the current white files where they are.)
