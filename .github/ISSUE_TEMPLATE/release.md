---
name: Release
about: Prepare a release
title: "[RELEASE] v"
labels: release
---

<!-- Never write the Registrator mention in this description: the mention alone, anywhere in the issue, starts a registration. -->

## Checklist

- [ ] Version bumped in `Project.toml`
- [ ] `CHANGELOG.md` / `BREAKING.md` up to date
- [ ] CI, documentation and breakage checks are green
- [ ] Release branch merged
- [ ] GitHub release and tag created

## Registration

**Stable release** (General registry): once every box above is ticked, post **one** comment that starts with the JuliaRegistrator trigger (`register`, preceded by the mention of the bot), followed by `Release notes:` and the "What's Changed" of the GitHub release. Post it once: the mention starts a registration wherever it appears, in this description or in any comment.

**Beta release** (`ct-registry`): no comment here; register with `LocalRegistry`, see [RELEASING.md](https://github.com/control-toolbox/ct-registry/blob/HEAD/RELEASING.md).
