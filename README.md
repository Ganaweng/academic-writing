# Academic Writing Skills

A modular collection of reusable AI skills for academic writing, terminology validation, manuscript polishing, literature review, citation management, and journal- or conference-oriented revision.

一套面向科研论文写作的模块化 AI Skills，适用于专业术语核验、稿件润色、文献综述、参考文献管理，以及面向期刊和会议的针对性修改。

## Repository structure

```text
skills/
└── <skill-name>/
    ├── SKILL.md
    ├── agents/
    ├── references/
    └── assets/
```

Each skill is self-contained and may include task instructions, interface metadata, domain references, and reusable assets.

## Available skills

### validate-academic-terminology

Compares, validates, standardizes, and polishes scholarly terminology using target-field literature, venue conventions, controlled vocabularies, corpus evidence, and semantic checks.

It is especially useful for:

- academic and technical term comparison;
- sentence, paragraph, and section polishing;
- manuscript-wide terminology consistency audits;
- computer vision, image processing, small-target detection, and remote sensing papers;
- IEEE journals and CVPR/ICCV-style manuscripts.

## Usage

Invoke the skill by name in a compatible ChatGPT or Codex environment:

```text
Use $validate-academic-terminology to compare these technical terms and revise the sentence using target-venue evidence.
```

## Principles

- Preserve scientific and mathematical meaning before improving style.
- Prefer target-venue literature and authoritative terminology over raw search frequency.
- Avoid unsupported claims such as “significant,” “robust,” “efficient,” or “state of the art.”
- Keep author-defined module names, abbreviations, symbols, and evidence strength consistent.

## Status

This repository will continue to expand with additional academic-writing skills.
