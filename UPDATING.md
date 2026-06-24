# Updating this website

All edits push to `main` and auto-deploy via GitHub Actions in ~2 minutes.

## Add a paper
Edit `data/papers.yaml` and add an entry:
```yaml
- title: "Paper Title"
  authors: ["Štěpán Jabůrek", "Coauthor Name"]
  year: 2026
  kind: working_paper        # or "published"
  status: "working paper"    # working paper | under review | revise and resubmit | accepted | published
  venue: ""                  # journal name if published
  link: ""                   # DOI or external URL
  pdf: "files/your-paper.pdf"  # if you upload the PDF below
```
If you have a PDF, drop it into `static/files/` (e.g. `static/files/io-scapegoating-2026.pdf`) and reference it via `pdf: "files/io-scapegoating-2026.pdf"`.

## Add a dataset
Edit `data/datasets.yaml`:
```yaml
- title: "Dataset name"
  authors: ["Štěpán Jabůrek"]
  year: 2026
  venue: "Harvard Dataverse"
  link: "https://doi.org/..."
  description: "One-sentence description."
```

## Add a teaching entry
Edit `data/teaching.yaml`:
```yaml
- course: "Course Name"
  role: "Co-Lecturer (40%)"
  institution: "Charles University"
  term: "Spring 2026"
```

## Update bio / homepage prose
Edit `content/_index.md` (the body below the front matter).

## Update CV
Replace `static/files/cv.pdf` with the new PDF (same filename).

## Change photo
Replace `static/images/photo.jpg` with a new square image (~400×400).

## Add a project
Edit `data/projects.yaml`.

## Mark a paper as published
In `data/papers.yaml`, change `kind: working_paper` to `kind: published`, set `status: "published"`, and add the `venue:` and `link:` fields.

## Local preview
```
hugo server
```
Open http://localhost:1313.

## Build locally
```
hugo --gc --minify
```
Output goes to `public/`.
