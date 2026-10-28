# Oil & Gas Direction Scorecard

This scorecard shows the direction of travel from 2021 to 2025 for 23 US oil and gas companies, each measured against its own record. It covers operations and safety, emissions, decarbonization strategy and context. Company disclosures sit side by side with independent federal records (PHMSA, EPA, BSEE, OSHA, lobbying filings).

> **Status: draft prototype for internal review.** The figures have not yet been through company review, and the direction and position labels are provisional. The data is as of 5 Oct 2026. It is not for circulation until CGEP clearance and company review are complete.

## What's here

| Path | What it is |
|---|---|
| `index.html` | The whole site in one self-contained file, with the data embedded. It needs no build step and no server code. |
| `data/scorecard-data.json` | The same data as a standalone file: every cell's direction, values by year, notes, and the document, page and link for each year. |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are. |

The site loads two Google Fonts. Everything else is inline.

## Before you push: public or private

**A GitHub Pages site is public.** On a free account, both the repository and the Pages site are public, so anyone with the link can read the pre-review data. Until release, choose one of these:

- **A private repository with Pages turned off.** Use it for version control and sharing with collaborators you add. Viewers download the repo and open `index.html` locally.
- **A private repository with Pages turned on.** This needs a paid GitHub plan (Pro, Team or Enterprise). The published site is still public unless the organization uses GitHub Enterprise Cloud, which can limit Pages to org members.
- **A public repository and Pages,** only after clearance and company review.

`index.html` includes `<meta name="robots" content="noindex">`, which keeps search engines from listing the draft. Remove it at launch.

## Publish on GitHub Pages

1. Create a repository, for example `oil-gas-direction-scorecard`, and upload these files to its root. Either drag them in on github.com ("Add file" → "Upload files"), or run:

   ```bash
   git init
   git add .
   git commit -m "Oil & Gas Direction Scorecard: draft prototype"
   git branch -M main
   git remote add origin https://github.com/<your-account>/oil-gas-direction-scorecard.git
   git push -u origin main
   ```
2. On GitHub, open **Settings → Pages**. Under "Build and deployment", choose **Deploy from a branch**, then **main** and **/ (root)**, and save.
3. After a minute or two, the site is live at `https://<your-account>.github.io/oil-gas-direction-scorecard/`.

## Updating the data

The site is rebuilt from the master workbook (`us_top24_scorecard.xlsx`): the build script writes the site's data and embeds it in `index.html`. To update, replace `index.html` and `data/scorecard-data.json` with the new build, then commit. Each push redeploys the site.

## Method in brief

- Every figure comes from the company's own documents or a government record. Each cell links to its source document, page and date.
- Each company is compared with its own past, not with the others. Directions compare the first and last two years, and a change within ±10% counts as flat.
- A series that spans an acquisition or a change in method is shown as a series break. No direction is read across it.
- Stated commitments compare what the company's own documents said each year.

The full method notes are on the site, below the matrix.

## Credit

Center on Global Energy Policy, Columbia University. Licensing to be decided before public release.
