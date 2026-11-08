# Deploy Chapel Home

## Download
On Our project, choose **Download deployable site**. Extract chapel-home-source.zip. The extracted folder contains index.html, app.js, data.js, style.css, images/, and these guides. No npm installation, build command, API key, or backend is required.

## Option 1: Netlify manual deployment
1. Sign in to Netlify and open its manual deploy / drag-and-drop flow.
2. Drag the extracted folder containing index.html directly into the deploy dropzone. Do not upload a parent folder that hides index.html another level down.
3. Open the deployment URL and test Explore, property photos, three-property comparison, and a clearly labeled test review.
4. To update, edit the local files and upload the updated folder on the same site's Deploys page.

If connecting a Git repository containing the original project layout instead, leave the build command empty and set the publish directory to dist. For the flattened download ZIP, use the repository root as publish directory.
Official guide: https://docs.netlify.com/start/quickstarts/netlify-drop-quickstart/

## Option 2: GitHub Pages
1. Create a GitHub repository and upload the **contents** of the extracted ZIP at its root. index.html must be at the root. Include the images directory and .nojekyll file.
2. Go to Settings → Pages → Build and deployment → Source → Deploy from a branch.
3. Select main and /(root), then Save.
4. Wait for the Pages deployment to finish and open the URL shown in Settings → Pages.
5. Commit edits to main to redeploy.

Hash routes (such as #property/union) and relative assets work on repository subpaths without server rewrite rules.
Official guide: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Local preview
From inside the extracted folder:

    python3 -m http.server 8000

On Windows, use `py -m http.server 8000` if python3 is not available. Open http://localhost:8000. For the original source tree, run `python3 -m http.server 8000 --directory dist` from the project root.

## Content edits
- data.js: name, property information, photo paths and credits, dated public research, and the two team-provided accounts.
- app.js: pages, forms, filters, comparison, local saving.
- style.css: design and responsive layout.
- images/: downloaded property photos; update data.js when replacing them.
- TEAM_GUIDE.md: usability tasks, survey questions, and research guidance.

The current ChatGPT-hosted copy remains private. Deploying to a public host can make the bundled content publicly accessible; it does not turn local submissions into a shared database. Each origin/device has its own local data. Export before moving hosts. Public-review summaries are historical, not verified current conditions. Photo attribution is included; downloading a photo does not establish a redistribution license. Before broader public use, obtain permission or replace photos with your own/appropriately licensed images, and confirm permission to identify student contributors.

## What hosting does not add
Reviews, feedback, and flags stay in the browser. No team inbox, shared review feed, residency verification, moderation, or server exists. Before collecting real public submissions, add a database/API, moderation workflow, server validation, privacy/retention rules, and abuse prevention.
