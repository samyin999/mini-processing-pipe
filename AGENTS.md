# Instructions for AI agents (minipipe)

This repo is Sam's **learning project**: a small, synthetic version of an eDiscovery processing pipeline
(audit a Reveal export, restore what it lost, build a Nuix-style `.mdb`), built to learn Python and system design.

## Rules

- **Agents never write code here.** No Python, tests, `pyproject.toml` or other code in this repo, not even a small
  fix. Sam writes all of it. Agents explain concepts, set exercises, review Sam's commits, run Sam's code and tests,
  and point at problems (what and why), not the fixed code.
- **Agents may add:** mock data under `mock-data/` (made by throwaway scripts kept outside the repo), and docs Sam asks for.
- **Fake data only.** No real client, matter, firm, staff, server or machine names, no real document IDs, stamps or
  paths. Generic examples only (`ABC.001.0001.0001`, `\\fileserver\import`).
- **Bytes matter.** Files in `mock-data/` are compared by MD5 and must stay byte for byte as made: `.gitattributes`
  turns off line-ending conversion. Never open and re-save them with an editor.
- **Teaching style:** one concept at a time, in depth; if Sam is stuck, stay on it. Ask Sam a question at the end of a
  lesson to check understanding.
