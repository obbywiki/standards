# TECH

By wlft (2026-08-16 UTC).

This file contains useful information about how tech should be implemented in regards to the Obby Wiki.

## Extensions

MediaWiki extensions are very powerful and can sometimes be the only way to implement a feature. However, they are also the hardest of any solution to both create and maintain. For instance, MediaWiki extensions are very dependent on MediaWiki itself, which means every extension must be updated manually in order to support a new MediaWiki version and its changeset. In order to achieve easier portability and maintainability, a few standards are applied to extensions:

### Language

MediaWiki extensions are predominantly PHP (obviously), but some other languages can help.

#### UI

When rendered from the server (server-side), the recommended method or producing non-interactive HTML is by using the MediaWiki HTML constructor class (see https://www.mediawiki.org/wiki/Manual:Html.php) along with Mustache templating.

When rendering interactive UIs, Vue is used alongside TypeScript. Vite can be used to bundle these into production-ready JavaScript (usually under `resources/dist/*.js`).

##### Styling

Either Less/vanilla CSS can be used to style HTML depending on preference. For larger extensions, Less may be better.

### ResourceLoader

Resource loader.

### Recommended Repository Layout (extensions)

_Not related to the WikiWire recommended repository layout._

```
.
├─ i18n/
├─ resources/
├─ src/
│  └─ Hooks.php
│  └─ ...
└─ ...
└─ extension.json
└─ README.md
└─ ...
```
