# CatKinKitKat Zola Blog

Static blog powered by Zola with the anemone theme and deployed via GitHub Pages.

## Getting started
- Prereqs: Zola v0.20+ and Git.
- After cloning, pull the theme submodule: `git submodule update --init --recursive`.
- Local preview: `zola serve` (serves at http://127.0.0.1:1111 by default).
- Build locally: `zola build` (outputs to `public/`).

## Content
- Site config lives in [config.toml](config.toml); `base_url` is set for the project Pages URL.
- Home page copy: [content/_index.md](content/_index.md).
- Example post: [content/blog/hello-world.md](content/blog/hello-world.md). Add more posts in the same folder using CommonMark front matter + body.

## Deployment (GitHub Pages)
- Workflow: [.github/workflows/deploy.yml](.github/workflows/deploy.yml) builds with Zola and uploads the `public/` artifact, then deploys with `actions/deploy-pages`.
- Triggers: push to `master` or manual `workflow_dispatch`.
- In GitHub: Settings → Pages → Source → GitHub Actions.

## Theme
- Theme: anemone (via git submodule under [themes/anemone](themes/anemone)).
- Update to latest theme: `git submodule update --remote themes/anemone`.