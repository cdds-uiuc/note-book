# Climate Dynamics and Data Science Notes

Source for the book published at https://cdds-uiuc.github.io/note-book/.

## Local development

```bash
conda env create -f environment.yml
conda activate note-book
jupyter book start       # live preview at http://localhost:3000
jupyter book build --html  # static build under _build/html/
```

Pushes to `main` are built and deployed to GitHub Pages via `.github/workflows/deploy.yml`.
