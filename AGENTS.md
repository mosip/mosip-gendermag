# AGENTS.md

## Repository Overview

This repository is currently a placeholder. On the `develop` branch (and on
`master`), the only tracked file is `README.md`, which reads:

```text
# mosip-gendermag
Contains AI tool required for Gendermag
```

The GitHub repository description says the same thing: "Contains AI tool
required for Gendermag". GenderMag is a usability-inspection method used to
find gender-inclusiveness issues in software (it stands for "Gender-Inclusive
Magnifier"). Based on the repo name and description, this repository is meant
to eventually hold an AI-assisted tool that supports GenderMag-style reviews
for MOSIP products. As of this writing, no such tool, script, or
documentation of the review process has been added yet — there is no source
code, no build configuration, and no application logic in this repository.

Do not assume a technology stack, folder layout, or build process beyond
what is described below. When real content is added to this repo, this file
should be updated to reflect it accurately.

## Technology Stack

None yet. There is no `pom.xml`, `package.json`, `requirements.txt`,
`build.gradle`, Dockerfile, or any other build/dependency manifest in this
repository. Whether the eventual tool will be Java, Python, Node.js, or
something else is not yet determined by anything in this repo — check again
once real source files land before making claims about the stack.

## Build & Test Commands

There is no build process, test suite, or CI workflow currently present on
the `develop` branch. There are no `.github/workflows` files on `develop` or
`master`. Do not invent build or test commands; if you add real source code,
add real build/test tooling and document the actual commands here.

## Configuration

No configuration files, environment variables, or secrets exist in this
repository yet. If configuration is introduced later, document each
local-override or secrets file explicitly here (for example, note whether it
should ever be committed).

## Project Structure Notes

```text
mosip-gendermag/
├── README.md   # one-line repo description
└── AGENTS.md   # this file
```

That is the entire tracked contents of the `develop` branch at the time this
file was written. There are no subfolders, so a single root `AGENTS.md` is
sufficient — do not create subfolder guides until real subdirectories with
distinct tooling actually exist.

## Development Workflow

1. Fork the repository and clone your fork.
2. Add the upstream remote: `git remote add upstream https://github.com/mosip/mosip-gendermag.git`.
3. Branch from `upstream/develop` (the active integration branch) for any change:

   ```shell
   git fetch upstream develop
   git checkout -b my-feature-branch upstream/develop
   ```

4. Make focused commits and sign off each one (`git commit -s`), matching
   MOSIP's standard DCO practice used across its other repositories.
5. Push to your fork (never push directly to `upstream`) and open a pull
   request against `develop`.

## Pull Request Guidelines

- Target the `develop` branch, not `master`.
- Reference the tracking issue in the PR description (e.g. `Addresses
  https://github.com/mosip/mosip-config/issues/10670`).
- Keep the first commit/PR title line short and prefixed with the issue
  number, e.g. `#10670: <summary>`.
- Since this repo currently has no CI checks on `develop`, do not claim in a
  PR description that "CI validates this" — verify what actually runs (if
  anything) before writing that.
- Sign off every commit (`git commit -s`) so it carries a `Signed-off-by`
  trailer matching your real git identity.

## Repository-Specific Considerations

- This is an early-stage/placeholder repository. Treat any assumption about
  its purpose beyond "AI tool for GenderMag reviews" as unverified until
  real code or documentation is added.
- Because there is no existing code style, dependency file, or CI
  configuration to follow, do not copy conventions from other MOSIP repos
  into this one without calling out that you did so — future contributors
  need to know which parts were established here versus carried over as a
  guess.
- Re-check `git ls-tree develop --name-only` before relying on this file's
  "Project Structure Notes" section, since it will go stale the moment real
  content is added.

## Agent rules

### Do

1. Verify the current tracked contents of the target branch
   (`git ls-tree <branch> --name-only`) before describing the repo's
   structure, stack, or build process.
2. Update this file's Technology Stack, Build & Test Commands, and Project
   Structure Notes sections as soon as real source code or tooling is added.
3. Target the `develop` branch for both branching and pull requests.
4. Sign off every commit (`git commit -s`).
5. State clearly when something is a placeholder or not yet implemented,
   rather than filling gaps with guesses.

### Do not

1. Do not invent build commands, dependency versions, or a technology stack
   that isn't backed by an actual file in the repository.
2. Do not claim CI checks, tests, or workflows exist unless you have found
   the actual `.github/workflows` file on the branch you are working from.
3. Do not push directly to `upstream` — always push to your fork (`origin`)
   and open a pull request.
4. Do not target `master` for new branches or PRs; use `develop`.
5. Do not create subfolder `AGENTS.md` files until real subdirectories with
   distinct tooling actually exist in this repo.
