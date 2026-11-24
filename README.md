# joonseokym.com

Personal resume and project portfolio of Joonseo Kym (KAIST, Mechanical & Electrical Engineering), live at [joonseokym.com](https://joonseokym.com).

Built with Jekyll and GitHub Pages, based on [jglovier/resume-template](https://github.com/jglovier/resume-template).

## Structure

- `_config.yml`: name, title, intro, social links, section toggles
- `_data/*.yml`: resume content (education, experience, projects, awards, etc.)
- `_posts/`: project detail pages linked from the resume
- `_assets/pdf/Joonseo_Kym_CV.pdf`: downloadable CV (kept in sync with the Overleaf source)

## Running locally

```sh
bundle install
bundle exec jekyll serve
```

Then open `localhost:4000`. A `Dockerfile` is also included.

## License

Code and styles are MIT licensed (see [LICENSE](LICENSE)). Resume content and media are not covered by the license.
