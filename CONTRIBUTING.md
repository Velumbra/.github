# Contributing

- One change per pull request. It's squash-merged; its title becomes the commit.
- The title is a [Conventional Commit](https://www.conventionalcommits.org) and decides the release: `fix:` patch, `feat:` minor, `feat!:` major, anything else none.
- Releases happen on merge. Don't bump versions by hand.
- Run `pnpm lint && pnpm typecheck && pnpm format:check && pnpm test:unit` before pushing.
