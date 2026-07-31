# ObbyWiki Design File

By wlft (2026-07-31 UTC).

## Skin

The Obby Wiki uses the Citizen skin along with [Citizen 4 design tokens](https://mwcitizen.skin/guide/migrating-to-citizen-4#migrate-your-token-overrides). Most of the Citizen 4 design tokens use Codex tokens (MW 1.46), but some may be different.

* https://mwcitizen.skin/

Make a note of how [existing extensions](https://github.com/orgs/obbywiki/repositories?q=mediawiki-extensions-) already implement these design practices.

## Design

The majority of design choices are inherited from Citizen, however, some aspects are different.

### Proportions

#### Chips & Pills

Chips should not be in the form of pills. `border-radius` should never be 999px or anything close to that, use variables and consistent corner radii. Chips should be rectangular, as should most elements that are typically pills. Chips (or badges) should always be a solid color and may utilize icons.

### Themes

Citizen's default themes include both dark and light variants. The main accent color, `--color--progressive`, depends, but is usually blue. Every aspect and style should work with all light and dark themes.

### Flow and Clarity

Every interface or element should be visually consistent and make sense where it is. For example, if two types of social connections are different on the backend (i.e., one type offers connections managed under Special:Preferences, and one is just a URI/@username fill), then both should be acknowledged in the same spot. If the user must go to another place to edit it, then communicate that clearly, but subtly. Don't scream it, just leave it there for the user to learn it themself.

* Do: Include immediately configurable items with a "Manage additional connections here" link
* Don't: Put the fields and the link in a seperate place, or expect users to know where to find the other connections.

#### Separation & Grouping

Sometimes two elements make sense together. For example, a profile picture and banner option. These could go under an 'Appearance' header. This is an example of good grouping.

### Actions

Primary actions should always be obvious.

## Language

All user-facing interface text **must** be in US English for consistency purposes. Use simple English, capable of being understood by non-native speakers. This means that technical details should not be shared, as many users do not understand what these terms mean.

### Unicode & Characters

Standard unicode may be used if necessary. Please ensure it can render on all modern software.
