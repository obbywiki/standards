# SERVER

For information regarding server maintenance.

## Staging

Updating MediaWiki versions typically requires testing first, usually at `staging.obby.wiki` and `staging-auth.obby.wiki`. The same database is never used and the staging surface is only required briefly to test functionality. As a quick reference, here is a checklist, ranked by importance:

* Pages render without an error or any delay.
* Auth (i.e., login/signup via password, oauth, etc.).
** It may be useful to test reauthentication points as well.
* Editing and page creation
* Images display correctly (and are optimized correctly via Thumbro)
* Uploading files works
* Data storing works (Cargo)
* Other extensions (OWAF, DynamicJsonLD, etc.)
* Other actions such as pagevalues, raw formats and ctypes
* Everything looks expected
