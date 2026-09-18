# Personal website

Single page, no JavaScript, no build step. One HTML file plus two assets.

```
index.html                 the whole site
photo.jpg                  your photo, square, at least 400x400
Nishant_Resume_2026.pdf    linked from the Curriculum Vitae button
```

## Before you publish

Open `index.html` and search for `FILL`. Four things need you.

1. `photo.jpg` does not exist yet. Save a square photo into this folder with exactly that name. It gets cropped to a circle, so keep your face roughly centred.
2. The Google Scholar URL. If you do not have a profile yet, make one, it takes ten minutes and professors do check it. If you would rather not, delete that whole `<li>` rather than leaving a dead link.
3. The CoDIT paper title.
4. The CoDIT year, which also appears in the News section.

Two more to check rather than fill.

Your LinkedIn URL is written as `linkedin.com/in/nishant-bhave`, taken from your CV. Your older CV had a longer handle ending in `b1a943253`. Confirm which one actually resolves.

The phone number is live and formatted as a `tel:` link. See the note at the bottom of this file before you decide to keep it.

## Publishing on GitHub Pages

Create a new public repository on GitHub named exactly:

```
nishantjb1.github.io
```

The name has to match your username, otherwise the site lands on a `/repo-name/` subpath instead of the clean root URL.

Then, from inside this `website` folder:

```bash
git init
git add index.html photo.jpg Nishant_Resume_2026.pdf README.md
git commit -m "Personal website"
git branch -M main
git remote add origin https://github.com/nishantjb1/nishantjb1.github.io.git
git push -u origin main
```

On GitHub, go to the repository, then Settings, then Pages. Set Source to `Deploy from a branch`, branch `main`, folder `/ (root)`. Save.

The site appears at `https://nishantjb1.github.io` within a few minutes. The first build sometimes takes longer than later ones, so do not panic if it 404s for the first five minutes.

## Updating later

Edit `index.html`, then:

```bash
git add -A && git commit -m "Update" && git push
```

The live site refreshes on its own within a minute or so.

## A note on the phone number

You asked for it, so it is in. Worth knowing the tradeoff before you commit.

A phone number on a public page gets scraped by bots, and the practical result is spam calls rather than professors ringing you. Nobody in an admissions process will phone you out of the blue, they will email. If you want to keep a phone route open without publishing the number, the usual move is to leave it off the site and put it on the CV PDF instead, which is the document a serious reader downloads anyway.

Your call. Deleting it is one line in the contact list.

## Why one page and not several

You asked about navigating to separate pages. I built this as a single page with a sticky navigation bar that scrolls, and that is deliberate.

The visitor you care about is a professor giving you sixty seconds before deciding whether to reply. Every click is a place where that person leaves. On one page they scroll past your publications whether they meant to or not, which is the outcome you want. Separate pages also mean separate files to keep in sync, and more ways for a link to break.

If the page ever grows past roughly twice its current length, splitting Research and Projects onto their own pages becomes worth it. It is not worth it yet.
