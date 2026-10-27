# Featured project

## ReproMin

[ReproMin](https://github.com/fly1d/repomin) is a repository-scale test-case reducer.
It shrinks failing Maven, Gradle, and Python projects while preserving the configured failure.
The result includes a smaller payload and evidence that can be validated or replayed.

Try the self-contained demo from the [published dev14 pre-release](https://github.com/fly1d/repomin/releases/tag/v0.1.0.dev14):

```sh
uvx --from https://github.com/fly1d/repomin/releases/download/v0.1.0.dev14/repomin-0.1.0.dev14-py3-none-any.whl \
  repomin demo ./repomin-demo
```

With `uv` installed, this runs the demo without installing ReproMin into your project environment.

Maintainer-run examples:

- [Gradle composite-build failure](https://github.com/fly1d/repomin/blob/main/docs/CASE_STUDY_GRADLE_38843.md): 854 → 11 files; the configured failure reproduced in 5/5 fresh copies.
- [tsdown CSS module duplication](https://github.com/fly1d/repomin/blob/main/docs/CASE_STUDY_TSDOWN_979.md): 14 → 8 files; the configured failure reproduced in 3/3 fresh copies.

These are feasibility results from maintainer-run pilots, not independent adoption.
Development and these maintainer-run validations materially used OpenAI Codex.

[Quick start](https://github.com/fly1d/repomin/blob/main/docs/QUICKSTART.md) · [中文入门](https://github.com/fly1d/repomin/blob/main/docs/QUICKSTART.zh-CN.md)

ReproMin is pre-alpha. Use trusted repositories and commands; the default host backend runs your command directly and is not a sandbox.
