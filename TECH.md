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

A look at what a generic extension repository should look like (note the `src/` directory).

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

#### Additions For Public Repositories

Optionally, if the extension is public, add a `.github/FUNDING.yml` file with the following content:

```yaml
custom: ["https://obby.wiki/OW:Funding"]
```

It may also be appropriate to add a `CONTRIBUTING.md` file pointing athttps://github.com/obbywiki/standards.

## Modules & Templates

Modules, templates, and other resources (such as scripts or files managed under the MediaWiki: namespace) are placed in the [OWSMT public repository](https://github.com/obbywiki/modules) (or obbywiki/modules on GitHub). The majority of modules are written in Luau.

### Contributing

Please see the README in the OWMST for more information on how to contribute source code.

### Requesting a Module or a Template

You can request a new module on the OWSMT issues tab on GitHub provided you have a valid reason.

### Creating a new Module/Template/File

You can fork the OWSMT repository and create a Pull Request. Please follow WikiWire's format (e.g., modules/<group/host>/ModuleName/ModuleName.module.lua/luau).

### Licensing

Please view the OWSMT repository licensing information regarding the content stored there.
