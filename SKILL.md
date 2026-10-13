---
name: advanced-de-ai-writing-skills
description: Advanced Human Writing & AI Humanizer. Multilingual AI humanizer for genre-aware generation, humanize AI text, de-AI writing, natural rewriting, fiction and novels, novel writing assistant, story continuity, long-form audit, chunked audit, writing style unification, character consistency review, scene ending audit, and rewrite fidelity. Also supports de-AI editing, academic and formal writing, protected-content checks, and long-document review. 增强版去 AI 写作 Skill、高级 AI 写作工具、去AI味、去AI写作、消除AI腔、AI文本润色、小说润色、小说续写、AI式结尾、生硬结尾审查、长文一致性、分块审查、全书审查、文风统一、人物设定统一、人物一致性审查、人物对白审查、翻译腔.
---

# Advanced De-AI Writing Skills

This project combines two complementary layers. Use the original De-AI Writing standard as the authoritative editing guide for requests to de-AI, humanise, make writing sound less robotic, or remove AI-like patterns. Use the broader Human Writing Skills modules when the task also needs genre-specific guidance, generation-time quality controls, specialist editorial audits, or long-form continuity.

## Priority rule for De-AI editing

Before rewriting, read de-ai-writing/SKILL.md and de-ai-writing/references/signs.md. Preserve the author's ideas and wording wherever they work. Fix what the sentence is doing, not merely the words it uses.

Preserve all facts, numbers, names, dates, links, claims, quotations, titles, legal text, spelling convention, tone, formatting requirements, and length limits. Do not invent details to make writing vivid. Do not rewrite clean sentences just to make them different. Do not treat a scanner match as proof of AI authorship.

## Workflow

1. Identify the user's actual task, audience, genre, spelling convention, and constraints.
2. For de-AI editing, use the original field guide as the source of truth for covered signs.
3. Select only the advanced modules relevant to the task. The skills/ directory contains genre and review modules; humanwriting/ contains executable Python tools.
4. Preserve meaning and voice while removing padding, vague praise, unsupported interpretation, repetition, and formulaic structure where present.
5. Where available, use the relevant scanner, linter, protected-content checks, rewrite-fidelity checks, or staged audit tools. Findings are evidence for review, not automatic verdicts.
6. Re-read the complete text for accuracy, evidence, flow, and genre fit. Leave justified matches alone and report them briefly when relevant.

## Do not

- Do not swap a flagged word for a synonym while leaving the underlying problem intact.
- Do not invent sources, facts, examples, reactions, sensory details, or claims.
- Do not alter quotations, titles, legal wording, numbers, links, or protected content without explicit instruction.
- Do not force short sentences, fragments, awkward grammar, roughness, or open endings as proof of natural writing.
- Do not flatten the author's personality or add material the user did not ask for.
- Do not describe pattern matching as reliable AI detection.

## Tooling and specialist modules

Use the root-level humanwriting/ package and skills/ modules for the broader toolkit. Consult HUMAN-WRITING-SKILLS-README.md for the upstream toolkit overview and docs/agent-orchestration.md for local multi-agent long-form coordination. The original De-AI scanner remains available at de-ai-writing/scripts/check_ai_signs.py.

## Output

Return the edited text or state clearly which files were changed. Keep explanations concise. When a scan or audit was run, report its findings accurately and distinguish automated results from manual editorial judgement.
