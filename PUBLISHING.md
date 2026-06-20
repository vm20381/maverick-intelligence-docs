# Publishing these docs

This `docs/` folder is the single source of truth for the Maverick Intelligence
API documentation. It powers the live site at https://docs.maverickintelligence.co
(Mintlify) and is mirrored to a **public** GitHub repo so it can be indexed by
[Context7](https://context7.com) and consumed by AI coding agents.

- **Edit here** (in the monorepo). Never edit the public repo directly.
- **Public mirror:** https://github.com/vm20381/maverick-intelligence-docs
- Keep this folder publishable only — **no internal/engineering notes, secrets,
  account IDs, or infrastructure URLs.** Anything committed here can become public.

## Sync to the public repo

After doc changes land on `main`, push the `docs/` subtree to the public repo:

```bash
# from the monorepo root
git subtree push --prefix docs https://github.com/vm20381/maverick-intelligence-docs.git main
```

That's the whole workflow. Context7 re-indexes from the public repo.
