# danielpallies.com — Quarto site

A starter for your new site. Your **Home / About** page is already filled in with
your real text. The other pages have placeholders waiting for content.

---

## One-time setup (Windows)

1. Install **Quarto**: https://quarto.org/docs/get-started (the `.msi` installer)
2. Install **Git for Windows**: https://git-scm.com (accept the defaults)
3. Create a **GitHub account**: https://github.com/signup
4. (Recommended) Install **VS Code** + its Quarto extension for a live-preview button.

---

## See it on your own computer

Unzip this folder somewhere, then open a terminal in it and run:

```
quarto preview
```

Your browser opens the site. Edit any `.qmd` file, save, and it refreshes live.

---

## Fill in your content

- **Home** — `index.qmd` (already done; add your photo at `assets/profile.jpg`)
- **CV** — put your real CV at `files/pallies-cv.pdf`; it embeds automatically.
  This is the embedded-PDF feature Wix dropped — it just works here.
- **Teaching** — `teaching.qmd`
- **Monsters** — `monsters.qmd`
- **Blog** — copy the `blog/welcome/` folder, rename it, edit `index.qmd` inside.

Math works like LaTeX: `$...$` inline, `$$...$$` displayed.

---

## Change the colors

Open `styles.scss` and edit the five values at the top. That's the whole palette.

---

## Publish to the web (do this after setup)

From the project folder, one command builds the site and pushes it live to
GitHub Pages:

```
quarto publish gh-pages
```

The first time, it walks you through connecting your GitHub account and creates
the repository for you.

## Point danielpallies.com at it (last step)

1. In your new GitHub repo: **Settings -> Pages -> Custom domain**, enter
   `danielpallies.com`, save.
2. At whoever controls your DNS (check lookup.icann.org, or your Wix Domains
   panel), add these records:
   - Four `A` records for the apex domain pointing to:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One `CNAME` record for `www` pointing to `YOUR-USERNAME.github.io`
3. Back in Settings -> Pages, tick **Enforce HTTPS** once it's available.

DNS changes can take a few hours to take effect. The `CNAME` file in this project
keeps the custom domain attached each time you re-publish.
