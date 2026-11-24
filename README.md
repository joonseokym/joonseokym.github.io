# joonseokym.com

Personal resume and project portfolio of Joonseo Kym (KAIST, Mechanical & Electrical Engineering), live at [joonseokym.com](https://joonseokym.com).

Built with Jekyll and GitHub Pages, originally based on [jglovier/resume-template](https://github.com/jglovier/resume-template).

## Structure

```
.
├── _config.yml          Site settings, header intro, section toggles, social links
├── _data/               Resume content, one file per section
│   ├── education.yml
│   ├── experience.yml
│   ├── projects.yml     Project cards (title, summary, thumbnail, post link)
│   ├── publications.yml
│   ├── patents.yml
│   ├── recognitions.yml
│   ├── militaryservice.yml
│   ├── associations.yml
│   ├── skills.yml
│   └── interests.yml    (section currently hidden)
├── _posts/              Project detail pages
├── _layouts/
│   ├── resume.html      Home page
│   └── post.html        Project pages, project list, 404
├── _includes/           <head>, social icons
├── _sass/               Styles (variables, base, resume)
├── css/main.scss        Stylesheet entry point
├── assets/
│   ├── cv/              Joonseo_Kym_CV.pdf (kept in sync with the Overleaf source)
│   ├── docs/            Project reports and papers
│   ├── images/
│   │   ├── avatar.jpg
│   │   ├── og-image-2026.png   Link preview image
│   │   ├── logos/       School, lab, and activity logos
│   │   ├── thumbs/      Project card thumbnails (800×450)
│   │   └── projects/    Figures used in each project post
│   └── videos/
├── blog.html            All projects page (/blog.html)
├── 404.html
├── index.html
├── favicon.png
└── apple-touch-icon.png
```

## Editing

- **Resume text**: edit the matching file in `_data/`. The intro lives in `_config.yml` (`resume_header_intro`).
- **New project**: add a post to `_posts/`, put its figures in `assets/images/projects/<slug>/`, add an 800×450 thumbnail to `assets/images/thumbs/`, and add an entry to `_data/projects.yml`.
- **CV**: replace `assets/cv/Joonseo_Kym_CV.pdf` with the latest export from Overleaf.

## Running locally

```sh
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`. With Docker:

```sh
docker build -t joonseokym-site .
docker run --rm -p 4000:4000 joonseokym-site
```

## License

Code and styles are MIT licensed (see [LICENSE](LICENSE)). Resume content and media are not covered by the license.
