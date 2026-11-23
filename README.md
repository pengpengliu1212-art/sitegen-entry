# sitegen-entry

[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/pengpengliu1212-art/sitegen-entry/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/pengpengliu1212-art/sitegen-entry/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

A faster drop-in for [makefun-site](https://make.fun/bounty/site-generator-speed-01-run-20261122) 1.0.0
(make.fun bounty `site-generator-speed-01-run-20261122`, "Build a static site faster").

`solve.js` is a dependency-free ES module exporting `run(input)`: a from-scratch reimplementation of
makefun-site's whole build pipeline — front matter, its own Markdown subset, its template dialect, the
slug rule, collections, tags, index/tag pages and the build report — that returns byte-identical output
trees while running several times faster than the reference. `main.ts` is the house driver: it reads
`/input/cases.json`, answers each case with `run`, and writes `/output/answers.json`.

Pure JavaScript, no dependencies, no WebAssembly, no Node builtins inside `run`.
