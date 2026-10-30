# Updating this website

All edits push to `main` and auto-deploy via GitHub Actions in ~2 minutes.

## Add a paper
Edit `data/papers.yaml` and add an entry:
```yaml
- title: "Paper Title"
  authors: ["Štěpán Jabůrek", "Coauthor Name"]
  year: 2026
  field: "IPE"               # IPE | Political Ideology | Methods | Science of Science | Data
  status: "WP"               # published | accepted | minor revisions | R&R | WP | preprint
  venue: ""                  # journal or preprint repository name (optional)
  link: ""                   # DOI or external URL (optional)
  pdf: "files/your-paper.pdf"  # if you upload the PDF below (optional)
  code: ""                   # replication code URL (optional)
  abstract: ""               # expandable abstract text (optional)
```
If you have a PDF, drop it into `static/files/` (e.g. `static/files/io-scapegoating-2026.pdf`) and reference it via `pdf: "files/io-scapegoating-2026.pdf"`.

### Contribution fields (`field:`)
- `"IPE"` — `01 · IPE`
- `"Political Ideology"` — `02 · Political Ideology`
- `"Methods"` — `03 · Methods`
- `"Science of Science"` — `04 · Science of Science`
- `"Data"` — `05 · Data`

### Status values (`status:`)
- `"published"` (or `"published in journal"`) — shows `Venue, Year` in bold italics (or `Published, Year`)
- `"accepted"` — shows `Accepted, Venue` (or `Accepted, Year`)
- `"minor revisions"` — shows `Minor Revisions at Venue` (or `Minor Revisions, Year`)
- `"R&R"` (or `"revise and resubmit"`) — shows `R&R at Venue` (or `R&R, Year`)
- `"WP"` (or `"working paper"`) — shows `Working Paper, Year`
- `"preprint"` — shows `Preprint, Venue, Year` (or `Preprint, Year`)

## Add a dataset
Edit `data/datasets.yaml` (automatically included in `05 · Data`):
```yaml
- title: "Dataset name"
  authors: ["Štěpán Jabůrek"]
  year: 2026
  field: "Data"
  status: "published"
  venue: "Harvard Dataverse"
  link: "https://doi.org/..."
  description: "One-sentence description."
```

## Add an "Other stuff" entry (R Packages or Web Apps)
Edit `data/other.yaml`:
```yaml
# Under r_packages to add an R Package:
r_packages:
  - name: "packageName"
    description: "Brief description of the R package."
    link: "https://github.com/..."

# Under web_apps to add a Web Application:
web_apps:
  - name: "App Name"
    description: "Brief description of the dashboard."
    link: "https://..."
    image: "images/app.png" # Optional: screenshot under static/images/
```

## Update bio / homepage prose
Edit `content/_index.md` (the body below the front matter).

## Update CV
Replace `static/files/cv.pdf` with the new PDF (same filename).

## Change photo
Replace `static/images/photo.jpg` with a new square image (~400×400).

## Add a project
Edit `data/projects.yaml`.

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
