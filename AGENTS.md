# Instructions for knowledge-maintenance agents

## Objective
Organize and maintain this repository as a clear, accurate, practical developer knowledge base. Prefer small, useful, well-verified entries over speculative or duplicated content.

## Directory taxonomy
- `concepts/<domain>/<slug>/` for broad principles independent of a particular technology.
- `languages/<language>/<slug>/` for language syntax, features, and idioms.
- `frameworks/<framework>/<slug>/` for framework-specific patterns and behavior.
- `libraries/<language>/<library>/` for third-party library usage.
- `projects/<slug>/` for hands-on implementations combining multiple topics.
- `knowledge/` for the central index and learning journal.

Use lowercase kebab-case slugs. Reuse existing categories and paths. Create a folder only when adding a real file, not to reserve future topics. Never use placeholder `.gitkeep` files.

## Workflow for adding a topic
1. Inspect existing paths and `knowledge/concepts.yaml`; avoid duplicates and update existing entries where appropriate.
2. Confirm the facts against reliable sources or runnable experiments. Mark version-dependent behavior and uncertainty. Do not claim code was run unless it was.
3. Choose the single most appropriate path. Create a `README.md` with:
   - Title and short overview
   - Problem/use case and mental model
   - Explanation with a concrete, realistic example
   - Practical exercise or experiment
   - Pitfalls, limitations, and related concepts
   - References, when relevant
4. Add a small `example.py`, `example.sql`, or other appropriate example only if it adds value. Keep it runnable where feasible and explain how to execute it. Never commit credentials or secrets.
5. Insert or update exactly one index item in `knowledge/concepts.yaml` with a unique ID, valid path, category, title, tags, and status.
6. Append to the learning log only when meaningful learning, testing, or review took place. Do not fabricate dates, results, or personal progress.
7. Check that all indexed paths exist; internal links work; YAML is valid; examples run if the environment supports them. State what was not verified.

## Knowledge index format
`knowledge/concepts.yaml` is a YAML document with `version: 1` and `entries: []`. Each entry:
```yaml
- id: concepts-algorithms-binary-search
  title: Binary search
  category: concepts
  path: concepts/algorithms/binary-search/README.md
  tags: [algorithms, search]
  status: verified
```
Allowed statuses: `draft`, `reviewed`, `verified`. Verified means explanations were cross-checked and examples tested when applicable. Never advance status without evidence.

## Editing rules
Keep changes focused, preserve user-authored material, and favor extending over overwriting. No automated mass reorganizations without clear need. Do not add empty category directories, project boilerplate, package managers, or CI until justified by actual content. Prefer concise technical English.
