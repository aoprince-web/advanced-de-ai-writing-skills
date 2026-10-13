# Advanced De-AI Writing Skills

An integrated writing toolkit that combines the original **De-AI Writing** editing standard with the broader **Human Writing Skills** toolkit for multilingual prose, genre-aware drafting, rewrite fidelity, and long-document review.

The guiding rule is simple: **fix what the sentence is doing, not merely the words it uses.** Preserve the writer's meaning, evidence, voice, and constraints. Do not invent detail, force artificial imperfections, or treat a pattern match as proof that text was written by AI.

## Two complementary layers

### 1. The original De-AI Writing standard

The complete original project is preserved in [de-ai-writing/](de-ai-writing/), including its SKILL.md, references/signs.md, Python pattern scanner, and before/after example. Its field guide is the core reference when the task is specifically to de-AI or humanise existing writing.

Run the original scanner from the repository root:

    python3 de-ai-writing/scripts/check_ai_signs.py path/to/file.md
    python3 de-ai-writing/scripts/check_ai_signs.py path/to/file.md --summary
    cat draft.txt | python3 de-ai-writing/scripts/check_ai_signs.py -

The scanner catches only a subset of patterns. It is not an AI detector and cannot replace a careful reading of the full text.

### 2. The advanced Human Writing Skills toolkit

The root-level humanwriting/, skills/, docs/, tests/, integrations/, and plugins/ retain the advanced toolkit's Python CLI, specialist editorial modules, protected-content and rewrite-fidelity checks, long-form audit workflow, local MCP coordination, integrations, and test suite.

See the [advanced toolkit documentation](HUMAN-WRITING-SKILLS-README.md), [agent orchestration guide](docs/agent-orchestration.md), and [long-form consistency guide](docs/long-form-consistency.md).

## Recommended workflow

1. Read the combined assistant skill in SKILL.md.
2. For de-AI editing, read the original De-AI skill in de-ai-writing/SKILL.md and the signs reference in de-ai-writing/references/signs.md.
3. Choose only the advanced modules needed for the document type and task.
4. Preserve facts, numbers, names, dates, links, claims, quotations, legal wording, spelling convention, voice, tone, and length limits.
5. Review the complete result for meaning, evidence, structure, and flow. Re-scan where appropriate and explain any deliberate remaining matches.

## Non-negotiable editing rules

- Keep clean sentences. Do not rewrite text just to make it different.
- Remove padding or faulty sentence structure rather than hiding it with synonyms.
- Never invent facts, examples, sensory details, reactions, sources, or specificity to make writing seem more human.
- Preserve the author's voice and the conventions of the intended genre.
- Treat scanner and lint findings as prompts for review, not proof of authorship or errors.
- Do not force roughness, fragments, awkward wording, or open endings as evidence of naturalness.

## Repository layout

- de-ai-writing/: original De-AI Writing project, preserved together.
- humanwriting/: executable Python toolkit.
- skills/: model-executed writing and editorial modules.
- docs/: user guides and reference documentation.
- tests/: automated tests and fixtures.
- plugins/, integrations/, agents/: integrations and assistant support.
- docs/human-writing-skills-readme.md: preserved upstream toolkit README.
- HUMAN-WRITING-SKILLS.md: preserved upstream toolkit skill instructions.

## Important limitation

This project helps people edit and review writing. It does not reliably determine authorship, and no individual wording pattern proves that a human or an AI wrote a passage.

## Licensing and attribution

The original De-AI Writing project and the advanced toolkit have their own source histories and licensing information. Review the respective licence and source notes before redistributing the combined project or individual components. The original advanced toolkit licence remains at LICENSE; the original De-AI Writing files and source notes are retained under de-ai-writing/.
