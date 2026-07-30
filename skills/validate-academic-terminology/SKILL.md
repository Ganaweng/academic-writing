---
name: validate-academic-terminology
description: Compare, validate, standardize, and polish terminology in scholarly English using target-field literature, venue conventions, controlled vocabularies, corpus evidence, and semantic checks. Use when the user asks which academic or technical term is better, whether a phrase is professional or idiomatic, how to rewrite a sentence or section for a journal or conference, how to distinguish near-synonyms, or how to audit terminology consistency across a manuscript. Especially useful for computer vision, image processing, small-target detection, remote sensing, IEEE journals, and CVPR/ICCV-style papers.
---

# Validate Academic Terminology

Apply a reproducible evidence hierarchy to terminology decisions and academic
polishing. Preserve the scientific claim, mathematical meaning, module behavior,
and evidence strength before improving style.

## Select the task mode

Classify the request before working:

1. **Term comparison** — compare two or more words or phrases.
2. **Usage validation** — determine whether one term, collocation, or sentence is
   technically accurate and natural.
3. **Passage polishing** — revise a sentence, paragraph, subsection, abstract, or
   caption while standardizing terminology.
4. **Manuscript audit** — find inconsistent names, capitalization, hyphenation,
   abbreviations, symbols, metric names, or semantic drift across a document.

For a document, use the applicable document/PDF skill for extraction and layout
preservation. Do not alter equations, citations, figure/table numbering, or
formatting unless the user asks.

Ask at most one clarifying question only when the domain, intended meaning, or
target venue would materially reverse the terminology decision. Otherwise infer
the likely context from the manuscript and state the assumption briefly.

## Run the validation workflow

### 1. Establish meaning before wording

Identify:

- the exact concept or tensor/entity being named;
- the scientific claim and its evidence strength;
- whether the term concerns geometry, signal strength, semantics, computation,
  statistics, or implementation;
- the target field and venue;
- any author-defined module names or terms that must remain locked.

Do not treat near-synonyms as interchangeable. Preserve distinctions such as
feature versus representation, noise versus clutter, performance versus
accuracy, and small versus weak.

### 2. Build candidate expressions

Keep the user's candidates and add at most three credible alternatives. Normalize
only spelling, capitalization, plurality, and hyphenation needed for a fair
comparison.

Exclude candidates that:

- overclaim novelty, causality, robustness, efficiency, significance, or
  state-of-the-art status;
- change the mathematical or implementation meaning;
- use impressive but vague wording;
- conflate task terminology with dataset-specific terminology.

### 3. Gather evidence

Follow the source and query rules in
[references/evidence-protocol.md](references/evidence-protocol.md).

Use current web or literature search when the request depends on present venue
usage, recent papers, or an external standard. Prefer exact-phrase searches and
inspect sentence-level context rather than relying on result counts.

When the user names a target venue or asks for venue-style wording, perform at
least one venue-matched literature search and cite representative evidence,
unless the user explicitly forbids browsing or source access is unavailable.
Without that check, label any venue-convention judgment as provisional. Do not
call a term *standard*, *dominant*, or *preferred by the venue* from intuition
alone.

For computer-vision or small-target language, also read
[references/computer-vision-terminology.md](references/computer-vision-terminology.md).

### 4. Decide by evidence hierarchy

Apply this priority order:

1. conceptual and mathematical accuracy;
2. compatibility with the implemented method and reported evidence;
3. convention in the target research community and target venue;
4. use in recent, strong, directly relevant papers;
5. academic collocation and grammar;
6. concision and stylistic preference.

Never select a term merely because it returns more search results. Frequency is
supporting evidence only after contextual relevance and meaning agree.

If evidence conflicts, explain the scope:

- use candidate A for one technical sense;
- use candidate B for another;
- recommend a manuscript-wide default and list justified exceptions.

### 5. Revise without semantic inflation

Produce the smallest change that fixes the issue. Preserve:

- author-defined module and dataset names;
- causal direction;
- modality, scale, tensor level, and processing stage;
- uncertainty and limitation language;
- metric-specific claims;
- symbols and variable scope.

Do not turn an observation into a mechanism, a correlation into causation, or a
single-dataset gain into general robustness. Do not use *significant* without
statistical support, *efficient* without resource evidence, *real-time* without a
declared measurement protocol, or *state of the art* without a controlled
comparison.

### 6. Record the decision

When the term is likely to recur, add a terminology-ledger entry containing:

| Field | Content |
| --- | --- |
| Preferred term | Manuscript-wide default |
| Definition/scope | What it denotes here |
| Allowed variant | Context-specific variant, if any |
| Avoid | Rejected or misleading alternatives |
| First-use form | Full name followed by abbreviation |
| Rationale | Semantic and venue-based reason |

Treat this ledger as the source of truth for later sections. Do not silently
change a locked decision. If a later context requires an exception, name it.

## Return the result

Use the matching compact format in
[references/output-formats.md](references/output-formats.md).

Always lead with the recommended wording. For a simple question, give the
decision, semantic distinction, and one revised example. For a passage or
manuscript, provide:

1. the revised text;
2. only material terminology issues;
3. the updated terminology ledger;
4. unresolved claims that require author or experimental confirmation.

When external evidence was used, cite the relevant sources near the associated
decision. Paraphrase usage patterns; do not copy distinctive sentences from
published work.

## Quality gate

Before returning, verify:

- one concept has one default term;
- capitalization and hyphenation are consistent;
- abbreviation is defined once and reused unchanged;
- the recommended term matches equations, figures, code behavior, and metrics;
- no polishing change strengthens the claim without evidence;
- the sentence remains concise and readable;
- rejected alternatives are explained only when the distinction matters.
