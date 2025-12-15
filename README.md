MotoFix - GitHub Pages hosting for Android App Links

Goal: publish /.well-known/assetlinks.json on a stable free host (GitHub Pages).

Steps:
1) Create a new PUBLIC GitHub repo (example name: motofix-links).
2) Upload the contents of this folder to the root of the repo:
   - index.html
   - .well-known/assetlinks.json
3) Enable GitHub Pages:
   Repo → Settings → Pages → Build and deployment:
   - Source: Deploy from a branch
   - Branch: main
   - Folder: / (root)
4) Verify the file opens as JSON:
   https://<YOUR_GITHUB_USER>.github.io/<REPO_NAME>/.well-known/assetlinks.json

Then update your AndroidManifest intent-filter host + pathPrefix to match:
- host: <YOUR_GITHUB_USER>.github.io
- pathPrefix: /<REPO_NAME>

assetlinks.json already includes:
- package_name: app.netlify.steady_torte_dfaec6.twa
- SHA-256: E4:DA:08:41:E7:53:7D:93:68:21:51:3B:A4:27:CD:7A:A2:A4:A1:AB
