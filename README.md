# kavehmousavand.github.io

Personal academic website for Kaveh Mousavand — plain HTML/CSS, no build step required.

## Updating an already-deployed site

If you already published an earlier version of this site, just overwrite the files in your
existing repo with the ones in this folder (same filenames, same structure — `index.html`,
`research.html`, `misc.html`, `fdb-applet.html`, `css/style.css`). No need to delete or recreate
the repo. See "Replace the files" below.

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

- **Web UI:** open your repo, click into each file (`index.html`, `research.html`, `misc.html`,
  `fdb-applet.html`, `css/style.css`), click the pencil ("Edit this file") icon, select all
  existing content and delete it, then paste in the new content from this folder. Commit each
  change. GitHub Pages will redeploy automatically within a minute or two.
- **Or, drag-and-drop:** on the repo's main page, drag the updated files from this folder onto the
  file list — GitHub will detect the matching filenames and offer to replace them. Commit.
- **Or, command line**, from inside your existing local clone of the repo:
  ```
  # copy the new files from this folder over your local repo, then:
  git add .
  git commit -m "Redesign: smaller top-left photo, Enomoto-style sidebar"
  git push
  ```

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
