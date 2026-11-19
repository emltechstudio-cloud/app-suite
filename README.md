# EML App Suite

This repository contains the App Suite homepage and six app source folders at the repository root. The homepage lists the six bundled apps plus a MyShub card linking to its existing live app and install page. There is no extra `/apps/` directory.

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

| Bundled app | Folder | Source |
| --- | --- | --- |
| Search with SEM | `searchwithsem/` | [searchwithsem](https://github.com/emltechstudio-cloud/searchwithsem) |
| Audiolite | `audiolite/` | [Audiolite](https://github.com/emltechstudio-cloud/Audiolite) |
| CalcPro | `calcpro/` | [Caculator](https://github.com/emltechstudio-cloud/Caculator) |
| CodeQR | `codeqr/` | [codeqr](https://github.com/emltechstudio-cloud/codeqr) |
| Quotes | `quotes/` | [quotes](https://github.com/emltechstudio-cloud/quotes) |
| EML Youniversity | `youniversity/` | [`officialwebsite.com/youniversity`](https://github.com/emltechstudio-cloud/officialwebsite.com/tree/main/youniversity) |

## Copy and change policy

The six app folders were copied from their existing repositories without rewriting their app code. `youniversity/install.html` is the only new app-specific page; the copied Youniversity source did not have a dedicated install page. The suite's root homepage is a separate catalogue page; it retains the existing catalogue API lookup and analytics calls, with static app-card content if the API is unavailable.

**MyShub** remains listed in the App Suite but its source folder is not copied into this repository. The card opens the existing app at [myshub.site](https://myshub.site) and links to its existing install page at [myshub.site/install.html](https://myshub.site/install.html). Its original repository and live app are untouched.

**My Shop** (`myshop`) is not included here and remains untouched as a separate project.

## Youniversity and the main site

The existing Youniversity app files are copied into `youniversity/`, with the new install page at `youniversity/install.html`. The original Youniversity folder on `officialwebsite.com` remains in place because the main site was not changed. This is a copy, not a move, so it does not reduce the original repository's size.

## Domain and deployment

The root `CNAME` contains `apps.emltechstudio.space`. GitHub Pages has not been enabled, no deployment has been published, and DNS has not been changed. The CNAME file alone does not publish the site; Pages settings and the DNS record still need to be configured. Pages access for a private repository depends on the GitHub plan.

All original app repositories and the existing main website remain untouched. The copied apps still need production testing on the new hostname before the domain is switched over.

## Local preview

From the repository root, run:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.
