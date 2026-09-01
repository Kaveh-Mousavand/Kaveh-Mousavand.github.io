# kavehmousavand.github.io

Personal academic website for Kaveh Mousavand — plain HTML/CSS, no build step required.

## Updating an already-deployed site

If you already published an earlier version of this site, overwrite the files in your existing
repo with the ones in this folder. This version adds `assets/images/profile.jpg` and eight PDFs
under `assets/docs/` — your CV, research statement, extended abstracts, and posters — so **every
file that used to live on Wix now lives in this repo**, and the site no longer points to
`wixsite.com` or `filesusr.com` anywhere except two external conference websites you don't own.
See "Replace the files" below.

## Deploy on GitHub Pages (free)

1. **Create the repository.**
   On GitHub, click **New repository**. If you want the site at `https://<your-username>.github.io/`,
   name the repo exactly `<your-username>.github.io` (e.g. `kaveh-mousavand.github.io`, matching
   your existing `Kaveh-Mousavand` GitHub account). Otherwise any name works and the site will be
   published at `https://<your-username>.github.io/<repo-name>/`.

2. **Upload these files.**
   Either:
   - Drag-and-drop all files in this folder (`index.html`, `research.html`, `misc.html`,
     `fdb-applet.html`, `css/style.css`, this `README.md`) into the GitHub web UI ("Add file →
     Upload files"), or
   - Push from the command line:
     ```
     git init
     git add .
     git commit -m "Initial site"
     git branch -M main
     git remote add origin https://github.com/<your-username>/<repo-name>.git
     git push -u origin main
     ```

### Replace the files (updating an existing repo)

This update adds two new folders (`assets/images/`, `assets/docs/`) alongside the existing pages,
so the easiest and most reliable approach is uploading everything at once:

- **Drag-and-drop (recommended for this update):** open your repo on GitHub, click **Add file →
  Upload files**, then drag in the *entire contents* of this folder — `index.html`,
  `research.html`, `misc.html`, `fdb-applet.html`, `css/style.css`, `README.md`, and the two new
  folders `assets/images/` and `assets/docs/` with everything inside them. GitHub will detect the
  files with matching names and overwrite them, and add the new ones. Scroll down and click
  **Commit changes**.
- **Command line**, from inside your existing local clone of the repo:
  ```
  # copy all files from this folder into your local repo folder (overwriting), then:
  git add .
  git commit -m "Move all assets off Wix; new profile photo; redesigned sidebar"
  git push
  ```

### What's new in this update
- `assets/images/profile.jpg` — your new photo, cropped square and sized to fit the sidebar.
- `assets/docs/` — eight PDFs that used to be hosted on Wix (CV, research statement, two extended
  abstracts, a research note, and three posters). All links across the site now point here instead
  of `wixsite.com`/`filesusr.com`.
- The FDB Applet page's "README" link now points to the `FDB-Applet` GitHub repository instead of
  a Wix-hosted text file.

3. **Enable Pages.**
   In the repo, go to **Settings → Pages**. Under "Build and deployment", set
   **Source: Deploy from a branch**, branch **main**, folder **/(root)**. Save.

4. **Visit your site.**
   GitHub will publish it within a minute or two at the URL shown on that same Settings page.

## Structure

```
index.html        Home — bio, research interests, contact
research.html      Research & Events — publications, posters, conference organizing
misc.html          Miscellaneous — broader interests, expository reading
fdb-applet.html    FDB Applet — about, install instructions, license
css/style.css      Shared stylesheet
```

## Notes

- The profile photo and PDF links currently point to your existing Wix-hosted files
  (`static.wixstatic.com` / `...filesusr.com`) so nothing breaks on day one. Once you're ready to
  fully retire the Wix site, download those files and swap in local paths (e.g. `assets/cv.pdf`,
  `assets/profile.jpg`) so the new site doesn't depend on Wix staying online.
- To add a new publication, event, or link, just copy an existing `<li>` block in the relevant
  page and edit the text — no templating system to learn.
- Update the "© 2026" line in each page's footer as years pass, or replace it with JavaScript that
  fills in the current year automatically if you prefer.
