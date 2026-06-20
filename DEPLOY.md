# Publishing the Research Toolkit on GitHub Pages (free)

The site is plain static HTML, so hosting is free and there is no build step.
Everything lives in this `toolkit/` folder:

```
toolkit/
  index.html                  site home (blog landing)
  downloads.html              use-online / download page
  about.html                  mission, citation, host-your-own
  assets/blog.css             shared styles for the blog pages
  posts/                      one page per tool + how-to articles
  prisma-flow.html  dedupe.html  cite.html  screen.html
  molbio.html  qpcr.html  solutions.html  tissue-culture.html   the tools
  research-toolkit-tools.zip  all tools in one download
```

## Option A — publish alongside QueryBee (fewest steps)

If this folder is already inside your QueryBee GitHub repository and Pages is on:

1. Commit and push the new `toolkit/` folder.
2. The site goes live at `https://<your-username>.github.io/<repo>/toolkit/`
   (for example `https://mafatlalmkher-cpu.github.io/querybee/toolkit/`).

Add a link from QueryBee's own page to `toolkit/` so visitors can find it.

## Option B — give it its own address

For a cleaner URL like `…github.io/research-toolkit/`:

1. Create a free GitHub account if you do not have one.
2. Create a new public repository, e.g. `research-toolkit`.
3. Upload the **contents** of this `toolkit/` folder to the repository root
   (so `index.html` is at the top level, with the `assets/` and `posts/` folders beside it).
4. In the repository, open **Settings → Pages**.
5. Under **Build and deployment**, set **Source = Deploy from a branch**,
   **Branch = main**, **folder = / (root)**, then **Save**.
6. Wait one to two minutes. Your site is live at
   `https://<your-username>.github.io/research-toolkit/`.

## Not using GitHub?

- **Netlify** or **Cloudflare Pages**: create a free account and drag this `toolkit`
  folder onto the dashboard. You get a live URL immediately.
- **No website at all**: every tool also works as a downloaded file. Send the file,
  or open it from a USB stick. The bench calculators need no internet.

## Notes

- Do not rename `assets/` or `posts/`; the pages link to them by those names.
- The reference formatter (`cite.html`) and QueryBee need the internet only to look up
  reference details. Every other tool works fully offline.
- To add a new article later, copy any file in `posts/`, change the text, and add a
  card for it on `index.html` under the Articles section.
