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

`fdoku.me` is registered at Namecheap and uses Namecheap BasicDNS
(`dns1`/`dns2.registrar-servers.com`). The zone holds:

| Type  | Host | Value                              |
|-------|------|------------------------------------|
| A     | `@`  | `185.199.108.153`                  |
| A     | `@`  | `185.199.109.153`                  |
| A     | `@`  | `185.199.110.153`                  |
| A     | `@`  | `185.199.111.153`                  |
| CNAME | `www`| `friedy10.github.io.`              |

The `CNAME` file at the repo root is what tells GitHub Pages to answer for
`fdoku.me` — deleting it reverts the site to <https://friedy10.github.io>.
