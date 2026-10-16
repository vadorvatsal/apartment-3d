# Our new home — 3D apartment tour

Static site prepared for GitHub Pages. No build step is needed.

## Publish using the GitHub website

1. Open your new GitHub repository.
2. Choose **Add file > Upload files**.
3. Upload the CONTENTS of this folder into the repository root. Do not upload the ZIP or put the files inside another folder.
4. Commit the upload to your chosen publishing branch.
5. Open **Settings > Pages**.
6. Under **Build and deployment**, choose **Deploy from a branch**.
7. Select the branch containing these files, choose **/(root)**, and save.
8. Wait for GitHub's deployment to finish, then use the website link shown in Pages settings.

Official instructions: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Files

- `index.html`: opens the main interactive tour and preserves query parameters and layout links.
- `Home 3D Tour.dc.html`: the current tour, including Layout 1 and Layout 2 buttons.
- `Home 3D Tour - Layout 1 backup.dc.html`: the original Layout 1 tour.
- `support.js`: the required rendering runtime; keep beside both tour files.
- `.nojekyll`: serves the files as a plain static site.

The tour loads React and Babel from unpkg.com, Three.js from esm.sh, and fonts from Google Fonts, so visitors need an internet connection.

To share a specific layout, append `#layout=1` or `#layout=2` to the website URL.

## Preview locally

From this folder, run `python -m http.server 8000`, then open http://localhost:8000/ in your browser.
