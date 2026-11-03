# antijante.github.io

Public project pages, served at <https://antijante.github.io>.

Each customer folder (for example `aluexbeams/`) is **written by a workflow** in that
customer's private `antijante/<customer>-hub` repo, which copies its `public/` folder here
on every push. Do not edit customer folders by hand; changes will be overwritten.

Everything in this repo is public, including its history. `robots.txt` asks search
engines not to crawl it, but anyone with the URL can read it.

## Add a customer

1. Create the private `antijante/<customer>-hub` repo from `antijante/aluexbeams-hub`'s structure.
2. Give it a deploy key secret (`SITE_DEPLOY_KEY`) with write access to this repo.
3. Push; the page appears at `https://antijante.github.io/<customer>/`.
