# ObbyWiki Design File

By wlft (2026-07-31 UTC).

## Skin

The Obby Wiki uses the Citizen skin along with [Citizen 4 design tokens](https://mwcitizen.skin/guide/migrating-to-citizen-4#migrate-your-token-overrides). Most of the Citizen 4 design tokens use Codex tokens (MW 1.46), but some may be different.

* https://mwcitizen.skin/

## Design

The majority of design choices are inherited from Citizen, however, some aspects are different.

### Proportions

#### Chips & Pills

Chips should not be in the form of pills. `border-radius` should never be 999px or anything close to that, use variables and consistent corner radii. Chips should be rectangular, as should most elements that are typically pills.

### Themes

Citizen's default themes include both dark and light variants. The main accent color, `--color--progressive`, depends, but is usually blue. Every aspect and style should work with all light and dark themes.
