# Breast Ultrasound Lesion Segmentation with U-Net

A project page for the Digital Image Processing final project: automated breast lesion
segmentation on the **BUSI** ultrasound dataset using **U-Net**, with a controlled comparison of
five loss functions (BCE, MSE, Dice, DiceBCE, Focal). Best result: **Focal Loss**, Dice 0.783 /
IoU 0.644.

This folder is a self-contained static website — plain HTML/CSS, no build step, no framework.

```
project-website/
├── index.html      ← the page itself
├── style.css       ← all styling
├── assets/         ← figures + paper PDF used by the page
│   ├── quantitative_summary.png
│   ├── loss_curves.png
│   ├── qualitative_comparison.png
│   └── UNET_BUSI_segmentation_DIP_project.pdf
└── code/           ← original implementation, linked from the page
    ├── Segmentation_using_UNET.ipynb
    └── segmentation_using_unet.py
```

## 1. Preview it locally

Just open `index.html` in a browser — everything is relative paths, so no server is required.
(Some browsers restrict local `file://` PDF embeds slightly, but the link still opens the PDF.)

## 2. Put it on GitHub

```bash
cd project-website
git init
git add .
git commit -m "Add breast ultrasound segmentation project page"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```

If you'd rather add this as a subfolder of an existing repo (e.g. a `projects/` directory in a
personal-site repo), just copy the whole `project-website/` folder in instead of running `git
init`.

## 3. Publish it with GitHub Pages (free hosting)

1. In the repo on GitHub: **Settings → Pages**.
2. Under "Build and deployment", set **Source** to `Deploy from a branch`.
3. Pick branch `main`, folder `/ (root)` — or `/project-website` if you added this as a subfolder
   of a bigger repo — then **Save**.
4. GitHub gives you a live URL, typically:
   `https://YOUR-USERNAME.github.io/YOUR-REPO/`

## 4. Link it from your personal website

In your personal site's projects section, point the project's link/thumbnail at the Pages URL
from step 3 (or at `index.html` directly if you're hosting everything from one repo).

## 5. A couple of placeholders to swap out

Two spots in `index.html` use placeholder links — search for `YOUR-USERNAME`/`YOUR-REPO` and
`your-personal-site.example.com` and replace them with:

- your real GitHub repo URL (appears twice: the "View code on GitHub" button and the footer), and
- the URL of your personal site's projects page (the "← Back to projects" footer link).

## Customizing

- Colors, spacing, fonts: edit the CSS custom properties at the top of `style.css` (`:root` for
  light mode, the `@media (prefers-color-scheme: dark)` block for dark mode).
- Content: all copy lives directly in `index.html`, organized into `<section>` blocks
  (`#overview`, `#pipeline`, `#losses`, `#results`, `#findings`, `#stack`).
- Figures: swap files in `assets/` and keep the same filenames, or update the `src` attributes in
  `index.html` if you rename them.
