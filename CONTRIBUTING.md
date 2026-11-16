# Contributing

- One change per pull request. It's squash-merged; its title becomes the commit.
- The title is a [Conventional Commit](https://www.conventionalcommits.org) and decides the release: `fix:` patch, `feat:` minor, `!` or a `BREAKING CHANGE:` footer breaking (a minor below 1.0, a major after); `chore:`, `docs:`, `test:`, `refactor:`, `ci:` release nothing.
- Releases happen on merge. Never bump a version by hand; for a specific one, push a tag: `git tag v1.0.0 && git push origin v1.0.0`.
- Each repo runs on its own: `pnpm dev` on port 3000, Postgres on `localhost:5432` with the repo's own database.
- Before pushing: `pnpm lint && pnpm typecheck && pnpm format:check && pnpm test:unit`.
