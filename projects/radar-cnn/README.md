# CNN-Based Target Classification Using FMCW Radar Range-Doppler Maps

A project page for the Radar Signal Processing final project: a lightweight CNN classifies
pedestrians, cyclists, and cars from CARRADA Range-Doppler radar patches, beating a hand-crafted
SVM baseline by 15.9 points (89.6% vs. 73.7% test accuracy, macro F1 0.89 vs. 0.75).

Same setup as the U-Net project page: plain HTML/CSS, no build step, no framework — and it goes
into the **same personal-website repo** you already have, because your homepage already links to
it:

```html
<a class="project-title" href="projects/radar-cnn/">CNN-Based Target Classification Using FMCW Radar Range-Doppler Maps</a>
```

That relative link expects a folder named `radar-cnn` inside `projects/`, next to your homepage's
`index.html`.

```
projects/radar-cnn/
├── index.html      ← the project page itself
├── style.css       ← styling for this page (a copy of the U-Net page's template)
├── assets/         ← figures + paper PDF used by the page
│   ├── fig1_fmcw_overview.png
│   ├── fig2_classdistribution.png
│   ├── fig3_groundtruthannotations.png
│   ├── fig4_Patchesperclass.png
│   ├── fig5_radarCNN.png
│   ├── fig6_lossandAccuracy.png
│   ├── fig7_CNNconfusionMatrics.png
│   ├── fig8_SVMmatrics.png
│   ├── fig9_testsetaccuracy.png
│   └── Radar_Final_Project.pdf
└── code/
    └── radar_cnn_project_executed.ipynb
```

## How to add it

Same steps as the U-Net project page:

1. Open your personal-website repo on GitHub.
2. **Add file → Upload files**.
3. Drag in the whole `radar-cnn` folder — GitHub's uploader preserves the folder structure, so it
   lands at `projects/radar-cnn/...` automatically. **Both `index.html` and `style.css` need to go
   up together** — the page has no styling without its CSS file.
4. Commit.

Once merged, if your site is served via GitHub Pages, this page is live at:
`https://YOUR-USERNAME.github.io/YOUR-REPO/projects/radar-cnn/`
— matching the link already on your homepage.

## Preview before uploading

Open `index.html` directly in a browser from this folder; everything uses relative paths, so
nothing else is required to check it looks right.

## Customizing

- Colors/spacing/fonts: `:root` custom properties at the top of `style.css` (light mode), and the
  `@media (prefers-color-scheme: dark)` block for dark mode.
- Content: lives directly in `index.html`, in `<section>` blocks (`#overview`, `#background`,
  `#method`, `#results`, `#findings`, `#stack`).
- The back-links at the top and bottom point to `../../index.html#projects` — two folders up. If
  you move this folder elsewhere in the repo, update those two hrefs to match.
