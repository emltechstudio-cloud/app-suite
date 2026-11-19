# EML App Suite

This repository combines the EML Tech Studio App Suite homepage with six apps in **separate folders at the repository root**. The root `index.html` is the homepage, so the intended addresses are `https://apps.emltechstudio.space/` for the suite and, for example, `https://apps.emltechstudio.space/audiolite/` for an app. There is no extra `/apps/` path segment.

## Repository layout

```text
index.html
CNAME
assets/
searchwithsem/
audiolite/
calcpro/
codeqr/
quotes/
youniversity/
```

| App | Root folder | Source repository / path |
| --- | --- | --- |
| Search with SEM | `searchwithsem/` | [searchwithsem](https://github.com/emltechstudio-cloud/searchwithsem) |
| Audiolite | `audiolite/` | [Audiolite](https://github.com/emltechstudio-cloud/Audiolite) |
| CalcPro | `calcpro/` | [Caculator](https://github.com/emltechstudio-cloud/Caculator) |
| CodeQR | `codeqr/` | [codeqr](https://github.com/emltechstudio-cloud/codeqr) |
| Quotes | `quotes/` | [quotes](https://github.com/emltechstudio-cloud/quotes) |
| EML Youniversity | `youniversity/` | [`officialwebsite.com/youniversity`](https://github.com/emltechstudio-cloud/officialwebsite.com/tree/main/youniversity) |

The root homepage uses static app cards, so the list does not disappear if the older dynamic catalogue feed is unavailable. The Open and Install buttons use paths inside this repository.

## Explicit exclusions

- **MyShub** (`myshub`) is excluded.
- **My Shop** (`myshop`) is excluded and remains a separate project.

## Domain and deployment

The root `CNAME` contains the requested domain `apps.emltechstudio.space`. This only records the intended domain in the repository. GitHub Pages has not been enabled, no deployment has been published, and no DNS settings have been changed. The existing main website and all original app repositories remain untouched.

The app directories are source snapshots from the existing repositories at the time this repository was assembled. They are now arranged at the requested root-level paths. Before making this the production host, test each app and its PWA install/service-worker behavior on the new paths; the source files were copied without broad code rewrites. MyShub is excluded, including its root-relative routing issue.

## Local preview

From the repository root, run:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.
