# LOGICA Development V2

## Project status
New independent **public** development repository. The legacy project is preserved unchanged at [LOGICA-Recovery](https://github.com/hmasprod-a11y/LOGICA-Recovery).

**IMPORTANT:** This repository has **not yet imported the application source or a distributable binary**. Do not treat it as a tested release.

## Verified historical reference
- Candidate baseline branch (old repository): `development/recovered-pos`
- Recorded head: `8218f5c825bfef4428f7530202fff9bc4c1a660a`
- Earlier Windows development/login build: [Actions #40270222140](https://github.com/hmasprod-a11y/LOGICA-Recovery/actions/runs/40270222140) (success at `00ce82779a87f34407f1db7adbb0881eb711b860`).
- A green CI run does not replace interactive acceptance tests.

## Migration gates
1. Review original branch contents **before any public import**. Exclude database dumps, customer records, keys, credentials, runtime/license files, binary archives and unlicensed third-party assets.
2. Import only audited code/config templates with a clear provenance manifest.
3. Build in isolated Windows CI; test startup, database, PIN login, catalogue, cash sale, stock, permissions and print paths.
4. Freeze a working baseline before making refactor changes. Do not port large stacked PRs wholesale.
5. Make small reviewed changes with regression tests; do not overwrite existing customer installations.

## Known prior regression symptoms
- Activation prompt reappeared in Release packages.
- Missing `bd` / local DB startup.
- `TABLE_PASS.Catégorie` login projection error.
- NullReferenceException on catalogue load (`Form_2_ARTICLES.Form_Me_Load`) and other UI paths.

These failures are **not yet fixed in this new repository**. Track each against the verified baseline.
