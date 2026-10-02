# fdoku.me

Personal research site for Friedrich Doku. Plain static HTML and CSS — no build step,
no generator, no dependencies. Edit the files and push.

```
index.html          front page: hero, research, publications, experience, writing, contact
404.html
css/site.css        the whole stylesheet
writing/*.html      ported technical notes
assets/             hero photo, open-graph card, CV pdf
images/             screenshots used by the writing pages
```

## Editing

**Publications and research** live directly in `index.html` as `.pub` and `.entry`
blocks — copy an existing one and change the text. Research entries carry a
`kind-finding` (amber) or `kind-system` (blue) marker depending on whether the work
found something or built something.

**The CV** is `assets/friedrich-doku-cv.pdf`. Replace the file, keep the name, and every
link on the site stays correct.

**Colours and type** are CSS custom properties at the top of `css/site.css`.

## Local preview

```sh
python3 -m http.server 8000
```

## Custom domain

`fdoku.me` currently points at Hostinger. To move it here:

1. Point the apex record at GitHub Pages (`185.199.108.153`, `.109.153`, `.110.153`,
   `.111.153`), or CNAME `www` to `friedy10.github.io`.
2. Add a `CNAME` file at the repo root containing `fdoku.me`.
3. Enable *Enforce HTTPS* in the repository's Pages settings.

Until step 2, the site serves from <https://friedy10.github.io>.
