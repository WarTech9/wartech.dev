# wartech homepage

Personal portfolio site for [John Warmann](https://linkedin.com/in/jwarmann) — full-stack engineer, digital nomad.

## Stack

Zero dependencies. Plain HTML, CSS, and vanilla JS. Deployed via Vercel.

## Local development

Open any page directly in a browser, or serve locally:

```sh
npx serve .
# or
python3 -m http.server 8080
```

## Pages

| File | Purpose |
|---|---|
| `index.html` | Landing — hero, featured projects, let's talk |
| `projects.html` | Filterable project showcase (Mobile / Blockchain / AI) |
| `experience.html` | Career history, organized by era (Foundation → Mobile → Web3 → AI) |
| `life.html` | Photo gallery — hiking, mountains, cities |

## Photos

Gallery images live in `photos/`. Filenames follow the convention `site-[date]-[location].webp`. To add photos:

1. Convert to WebP (target < 300KB per image)
2. Drop into `photos/`
3. Add a `<figure>` entry to the gallery in `life.html` — caption format: `// location`

## Deployment

Pushes to `main` deploy automatically via Vercel.
