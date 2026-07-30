# Evidence Protocol

## Evidence hierarchy

Use the strongest relevant source available:

1. **Authoritative terminology** — official standards, controlled vocabularies,
   publisher style manuals, benchmark definitions, and original method papers.
2. **Target-venue literature** — recent accepted papers in the same subfield and
   venue family.
3. **Directly related scholarly literature** — strong journals and conferences
   with the same technical meaning.
4. **Academic corpora** — Writefull, COCA Academic, or comparable scholarly
   corpora for collocation and grammatical behavior.
5. **General language corpora** — Linggle, Ludwig, SKELL, or general COCA for
   idiomaticity.
6. **AI language suggestions** — use only to generate candidates, never as final
   evidence for a technical distinction.

Use authoritative definitions and direct technical context ahead of raw
frequency. A recent, field-matched example is more probative than many unrelated
hits.

If the user explicitly names a journal or conference, include at least one
search restricted to that venue or its official proceedings. Cite one or two
representative sources whose surrounding context uses the candidate in the same
technical sense. If this cannot be done, describe the venue-specific conclusion
as provisional rather than established.

## Source routing

Choose sources by purpose:

| Need | Preferred source |
| --- | --- |
| Computer-vision venue usage | CVF Open Access, IEEE Xplore, ECCV proceedings |
| IEEE index terms or house style | IEEE Thesaurus/Taxonomy and IEEE Author Center |
| Broad scholarly occurrence | Google Scholar, Web of Science, Scopus |
| Exact academic phrasing | Writefull or a target-paper corpus |
| Near-synonym collocations | COCA Compare and academic subcorpus |
| Grammar, prepositions, idiomaticity | Linggle, Ludwig, SKELL |
| Section-level rhetorical phrases | Manchester Academic Phrasebank |
| Final grammar and consistency pass | Writefull, Paperpal, or Trinka |

Do not upload an unpublished full manuscript to an external service unless the
user has chosen that service and accepts its data terms. Prefer local inspection
or short, non-sensitive excerpts.

## Query construction

### Exact phrase

Search each candidate in quotation marks:

```text
"candidate phrase"
```

Add the technical anchor and venue:

```text
"candidate phrase" "object detection"
"candidate phrase" CVPR
"candidate phrase" site:openaccess.thecvf.com
"candidate phrase" site:ieeexplore.ieee.org
```

For a contrast, run symmetric queries with the same filters. Do not compare
counts from different databases or different filters.

### Semantic neighborhood

Search the candidate with nouns and verbs that reveal its meaning:

```text
"feature response" activation
"background clutter" detection
"robustness" corruption benchmark
"real-time" FPS hardware
```

Inspect at least several full contexts when available. Record whether each
occurrence is:

- the same technical sense;
- a different sense;
- author-defined terminology;
- title/abstract language or incidental full-text language.

### Venue and date

Use a recent five-year window by default for evolving terminology, supplemented
with seminal sources where definitions originate. Adapt the window when the user
specifies another period.

For manuscript wording, favor accepted papers over preprints when equivalent
versions exist. Use preprints when the work is current and no accepted version is
available, but label that status.

## Evidence interpretation

Do not report precise occurrence counts unless the search system exposes stable,
comparable counts and the query method is stated. Prefer calibrated conclusions:

- dominant in the target subfield;
- common but broader in meaning;
- uncommon in this sense;
- used mainly in an adjacent field;
- grammatically valid but technically misleading.

If only titles or snippets are accessible, say the evidence is indicative and do
not claim a full-corpus result.

## Citation and reuse

Link the official standard or representative paper supporting a technical
definition. Cite representative examples rather than a long list of hits.
Paraphrase patterns and keep any quoted fragment short. Never reconstruct or
reuse a distinctive sentence merely to make the prose look venue-like.
