# Project Website Template (Jekyll)

This is the **project introduction page** generated for the "Plastic Mold Factory: Capacity-Load Forecasting & Economic Analysis System". It is built with Jekyll and can be deployed to GitHub Pages.

## Directory Structure

```
project_website/
├── _config.yml              # Jekyll configuration
├── index.md                 # Page content (edit this file!)
├── _layouts/
│   └── project_page.html    # Page layout template
└── static/
    └── image/
        ├── dashboard.svg    # Dashboard placeholder (replace with a real screenshot)
        └── pipeline.svg     # Architecture diagram
```

## Usage

### 1. Edit the content
Open `index.md` and update the fields in the front matter:

| Placeholder | Replace with |
|-------------|--------------|
| `zhanghe` | Your name |
| `https://github.com/wyl-ctrl-c-v/moju-website` | Your GitHub repository URL |

### 2. Replace the images
Save a real screenshot of the running system as a PNG, put it into `static/image/`, and update the corresponding reference in `index.md`, e.g.:

```markdown
![System dashboard](static/image/dashboard.png)
```

### 3. Preview locally (optional)
After installing Jekyll, run:

```bash
cd project_website
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000 in your browser.

### 4. Deploy to GitHub Pages
1. Create a new repository on GitHub, e.g. `project_website`;
2. Upload / push this folder to the repository;
3. Repository → `Settings` → `Pages` → `Build and deployment` → `Deploy from a branch` → branch `main`, folder `/(root)` → Save;
4. After about 1 minute, visit: `https://your-username.github.io/project_website/`.

> Note: if images do not show after deployment, open `_config.yml` and change `baseurl: ""` to `baseurl: "/project_website"` (i.e. `/repo-name`).

## Notes
- This page is a **static introduction page**, used to present what the project is, its features, screenshots, and links;
- The Flask system itself requires a Python runtime and should be deployed separately to platforms such as Render / Railway.
