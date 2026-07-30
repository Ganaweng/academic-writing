# Computer-Vision Terminology Guide

Load this guide for computer vision, image processing, remote sensing, Anti-UAV,
or weak/small-target manuscripts. These are decision rules, not automatic
replacements; validate the intended meaning and target literature.

## Object, target, size, and signal strength

| Term | Prefer when | Do not imply |
| --- | --- | --- |
| small object | Referring to the standard object-detection size regime or a general CV task | Low contrast or weak signal |
| tiny object | Referring to an explicitly more extreme size regime supported by statistics or established task naming | Merely any small object |
| small target | Emphasizing a surveillance, remote-sensing, infrared, or signal-processing target against a background | A universal COCO-style category definition |
| weak target | Emphasizing low signal strength, contrast, or response | Small spatial extent by itself |
| weak and small target | Both low observability and small spatial extent are established | That *weak* and *small* are synonyms |

Use a hyphen in attributive compounds such as *small-object detector* and
*high-frequency branch*; normally omit it when the phrase is predicative or a
noun phrase, such as *the objects are small*.

## Feature vocabulary

| Term | Scope |
| --- | --- |
| feature map | A concrete spatial tensor with channels |
| feature | A generic learned descriptor or tensor; define local scope |
| representation | The encoded information or representational state, often broader than one tensor |
| response | An activation or output induced by an operator, filter, attention unit, or target |
| cue | Evidence used by a downstream decision, such as boundary, texture, motion, or frequency cues |
| component | A decomposed part, such as a frequency or wavelet component |
| detail | Semantically meaningful fine-scale image or feature structure |

Do not replace these only to avoid repetition. Repetition is preferable to
semantic drift in a Methods section.

## Background and degradation vocabulary

| Term | Prefer when |
| --- | --- |
| noise | Stochastic sensor, acquisition, or modeled perturbation |
| clutter | Structured, task-irrelevant background patterns or distractors |
| interference | Undesired competing signals or responses that impair the target representation |
| artifact | A spurious pattern introduced by sensing, processing, resampling, compression, or reconstruction |
| aliasing | Frequency folding or distortion caused by insufficient sampling or resampling |

Do not call all unwanted high-frequency content *noise*. Specify whether the
method suppresses stochastic noise, structured clutter, aliasing artifacts, or
inconsistent feature responses.

## Claims and evaluation

| Word | Required support |
| --- | --- |
| performance | Name the relevant metrics when possible |
| accuracy | Use for an accuracy metric or broadly correct detection/localization only when unambiguous |
| robustness | Evaluate perturbations, domains, scenes, or conditions beyond one ordinary test split |
| efficiency | Provide latency, throughput, computation, memory, energy, or parameter evidence |
| lightweight | Provide a meaningful resource comparison |
| real-time | Report speed, hardware, input size, batch size, precision, and timing protocol |
| significant | Provide a statistical test or use a non-statistical alternative such as *substantial* only when justified |
| state of the art | Use a controlled, current, protocol-matched comparison |

Prefer metric-specific statements such as “improves Recall by …” over vague
phrases such as “greatly improves detection performance.”

## Frequency-domain wording

Distinguish:

- **high-frequency component** — a decomposed spectral or wavelet part;
- **high-frequency response** — an operator or network activation;
- **high-frequency detail** — fine-scale structure with potential semantic value;
- **high-frequency cue** — detail used as detection evidence;
- **high-frequency enhancement** — an operation that increases selected
  responses, not proof that detection improves.

Avoid assuming that stronger high-frequency responses are beneficial. State
selection, calibration, suppression, alignment, or transfer only when the module
actually performs that operation.

## Cross-scale wording

Use:

- **alignment** for bringing features into spatial, geometric, or representational
  correspondence;
- **consistency** for agreement under an explicitly defined relation;
- **correlation** for statistical or learned dependence;
- **fusion** for combining information;
- **aggregation** for collecting or summarizing information;
- **interaction** for bidirectional or conditioned exchange.

Do not describe concatenation alone as alignment, or element-wise addition alone
as consistency calibration.

## Magnus-DETR naming preset

Apply only when working on the user's Magnus-DETR manuscript:

- `Magnus-DETR`
- `Dynamic Wavelet-Gated Convolution (DWGConv)`
- `MDHiFi` — preserve this capitalization; do not invent or change its full
  expansion without an author-confirmed definition.
- `High-Frequency Scale-Consistency Calibration (HF-SCC)`

Define each abbreviation at first use and retain the exact capitalization and
hyphenation afterward. Flag, rather than silently reconcile, any conflict between
the manuscript, figure labels, equations, and implementation.

