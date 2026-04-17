# Lemongrass Holdings Static Site

Small static site package for local hosting or Docker deployment.

## Contents

- `index.html`: single-page site entrypoint
- `assets/`: local images and self-hosted font files
- `Dockerfile`: minimal `nginx:alpine` container
- `nginx.conf`: static file server config on port `8080`

## Run locally with Docker

```bash
docker build -t lemongrass-site .
docker run --rm -p 8080:8080 lemongrass-site
```

Then open `http://localhost:8080`.

## Notes

- Fonts are vendored locally under `assets/fonts`, so the page no longer depends on Google Fonts at runtime.
- The contact form remains static and opens the visitor's mail app with a drafted email to `hello@lemongrassinvestments.com`.
- Metadata and share-preview tags are set locally, but the final canonical URL should be added once the production domain is known.
