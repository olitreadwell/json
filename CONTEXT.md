# nlohmann/json context
> refreshed 2026-09-04 | upstream default: develop @ 19386dd14af178fecd4a4a65549b07e240e092a9

## Identity & policies
- upstream: nlohmann/json, default branch `develop`, primary language C++, English-first (yes)
- CLA/DCO: DCO required (CONTRIBUTING.md: "All contributions (including pull requests) must agree to the Developer Certificate of Origin (DCO) version 1.1"). No CLA bot.
- AI-assisted PR policy: unstated (no ban found in CONTRIBUTING)
- signed commits required: no
- PR template: `.github/PULL_REQUEST_TEMPLATE.md` (checklist: describe changes, reference issue, 100% coverage, docs updated, amalgamated via `make amalgamate`)
- external tracker: github

## Conventions (verified from merged PRs)
- branch naming: `fix/<kebab-description>` dominant for human fixes; `claude/...` also seen; dependabot uses `dependabot/...`
- commit style: plain imperative / descriptive; PRs merged against `develop`
- test command: `cmake -S. -B build && cmake --build build -j 10 && ctest --test-dir build -j 10`
- docs build: `make install_venv -C docs/mkdocs && make serve -C docs/mkdocs`
- amalgamate: `make amalgamate` (regenerates single_include from include/nlohmann)
- CONTRIBUTING explicitly exempts typo fixes from the issue-first discussion requirement: "Only a few cases (e.g., fixing typos) do not require prior discussions."

## Maintainer picture
- primary maintainer: Niels Lohmann (nlohmann). Active, responsive.
- external contributors merge regularly (darkdi, Angadi56, petrbel seen in vetted research).

## Issue-area health
- typo/doc/link fixes are welcome and exempt from issue-first.

## Gap ledger (dedupe — READ FIRST, never re-pick)
- `2026-09-04` self-found gap (dead links in docs) — outcome: pr-opened — lesson: FAQ `dump()` link (old nlohmann.github.io Doxygen page) and CocoaPods "file issues here" link (Bitbucket issues page) both 404; replaced with relative `../api/basic_json/dump.md` (repo convention) and `https://cocoapods.org/pods/nlohmann_json` (200). Fork PR #2, base=develop, head=fix/broken-links-in-docs. Docs-only, no amalgamate needed.

## Mined gaps (discovered, not yet attempted)
- `2026-09-04` docs dead links (FAQ dump() + CocoaPods issues) — status: attempted (pr-opened, fork PR #2)
- `2026-09-04` trivial-fix pass (typos: `supress`->`suppress` in macro_scope.hpp, `advices`->`advice` in Makefile; dead links in customers.md) — status: proposed (not attempted; macro_scope.hpp needs amalgamate, customers.md links are third-party/transient)
