# Publishing checklist

This folder is a local draft. It has **not** been pushed to GitHub yet.

Planned destination after review:

- Repository: `VetTV-Studios/simpsons-hit-and-run-recomp`
- Visibility: public
- GitHub Pages: deploy from branch `main`, folder `/docs`
- Planned URL: `https://vettv-studios.github.io/simpsons-hit-and-run-recomp/`

## Before the first push

1. Read `README.md` and preview `docs/index.html` locally.
2. Confirm both screenshots are approved for public use:
   - `docs/assets/title-screen.png`
   - `docs/assets/attract-demo.png`
3. Confirm the status claims still match the latest local build log.
4. Search the staged tree for game data or build output. It must not contain
   ISOs, XBEs, extracted game files, crash dumps, logs, generated game code,
   local SDK clones, virtual environments, or compiled executables.
5. Decide whether this repository will later hold the actual port code or
   remain a project/status site. Do not copy the existing development tree in
   blindly.

## First publication (maintainer-run)

Create an **empty** public repository named `simpsons-hit-and-run-recomp`
under the VetTV-Studios organization. Do not initialize it with a README,
license, or `.gitignore` on GitHub; this draft already contains those files.

Then, from this folder after review:

```powershell
git branch -M main
git remote add origin https://github.com/VetTV-Studios/simpsons-hit-and-run-recomp.git
git add README.md PUBLISHING.md .gitignore docs/index.html docs/styles.css docs/.nojekyll docs/assets/title-screen.png docs/assets/attract-demo.png
git status --short
git commit -m "Create project landing page and status site"
git push -u origin main
```

In the GitHub repository settings, open **Pages**, choose **Deploy from a
branch**, select `main` and `/docs`, then save. Wait for the Pages deployment
to finish and verify every image and internal anchor on the live URL.

## Description and topics to consider

Repository description:

> Fan-made static recompilation bring-up of the original Xbox version of
> The Simpsons: Hit & Run for native PC. Bring your own game; no assets included.

Candidate topics:

- `xbox`
- `static-recompilation`
- `reverse-engineering`
- `game-port`
- `directx-12`
- `simpsons-hit-and-run`

Do not add a release or download badge until a build has been deliberately
packaged, tested, and reviewed.
