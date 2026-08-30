# Facebook media catalog

Public catalog of Facebook media clips (series, films, anime, comedians) with France watch availability (Prime, Netflix, Crunchyroll first).

## Filters

Pills at the top: Tout, Séries, Films, Anime, Humoristes. Cards show genre, runtime, filler % (anime), IMDb / Rotten Tomatoes / MyAnimeList scores, and where to watch in France. Subscribed platforms (Netflix, Prime, Crunchyroll) are highlighted.

The page loads `site/catalog.json` in the browser.

## Deploy

The Hostinger VPS serves this site with docker-compose (nginx:alpine, host port 8081):

```bash
docker compose up -d --build
```

`Dockerfile` copies `site/` into nginx html. `restart: unless-stopped` keeps the container up.
