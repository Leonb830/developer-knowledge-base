# Developer Knowledge Base

An agent-maintained, practical knowledge base for software engineering concepts, languages, frameworks, libraries, and projects.

## Purpose
Collect verified explanations, runnable examples, experiments, and lessons learned. Learn by building and testing, not by collecting definitions alone.

## Organization
The agent creates directories **only when adding actual content**:

- `concepts/<domain>/<topic>/` — fundamentals such as algorithms, networking, and databases
- `languages/<language>/<topic>/` — language-specific features
- `frameworks/<framework>/<topic>/` — framework-specific practices
- `libraries/<language>/<library>/` — reusable library notes
- `projects/<project>/` — applied projects and experiments
- `knowledge/concepts.yaml` — searchable content index
- `knowledge/learning-log.md` — dated learning history

Example future paths: `concepts/algorithms/binary-search/README.md`, `languages/python/decorators/README.md`, `frameworks/fastapi/dependency-injection/README.md`.

## Adding knowledge
1. Read [AGENTS.md](AGENTS.md) for contribution rules.
2. Check for an existing topic before adding a new one.
3. Create a concise topic README that explains **what**, **why**, **when**, and **how**, with a practical example and a verification step.
4. Add supporting code or SQL only when useful and tested.
5. Add or update its entry in [knowledge/concepts.yaml](knowledge/concepts.yaml).
6. Append a dated entry to [knowledge/learning-log.md](knowledge/learning-log.md) when learning or testing actually occurred.

Use simple Markdown and ordinary source files. No scaffolding, dependencies, or empty directories until needed.
