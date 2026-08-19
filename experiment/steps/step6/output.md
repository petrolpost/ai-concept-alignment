# Step 6 — External Vocabulary Lookup: Agent

## Purpose

Test whether established public vocabularies can provide concepts that can be aligned with, distinguished from, or used to challenge the Agent observations from Steps 1–5.

This step does **not** attempt to select a definition of AI Agent. It asks what existing vocabularies mean when they use `Agent`, `SoftwareAgent`, or related terms.

## 1. EU Vocabularies

### 1.1 EuroVoc

The EU Vocabularies catalogue describes EuroVoc as a multilingual, multidisciplinary thesaurus covering EU activities. The catalogue also exposes alignments between EuroVoc and other vocabularies. However, the public catalogue/search material reviewed for this experiment did not yield an AI/software-agent concept in EuroVoc that could serve as a direct match for the modern LLM-based `Agent` under study.

**Result:** no direct AI-Agent alignment found in EuroVoc during this lookup.

This is a lookup result, not a claim that EuroVoc contains no possible related term anywhere in its full dataset.

### 1.2 EU Corporate Body / Agent usage

The EU Publications Office does have a `Corporate body` controlled vocabulary. EU documentation also describes `Agent` as part of the Common Data Model / metadata model: `Resource type` is used together with the `Event` and `Corporate body (Agent)` controlled vocabularies to represent an event triggered by an agent associated with a resource type.

This is a useful counterexample to the current AI-centric interpretation of Agent. In this EU metadata context, `Agent` is about an entity participating in or bearing a role in a document/procedural context, not an autonomous AI system.

**Alignment:** lexical relation only; **not** a semantic match for AI Agent.

**Challenge to current observations:** the word `Agent` can denote a role-bearing participant without autonomy, reasoning, planning, tools, memory, or adaptation.

## 2. W3C PROV-O

W3C PROV-O provides a particularly useful formal vocabulary. `prov:Agent` is defined as something that bears responsibility for an activity, for the existence of an entity, or for another agent's activity. `prov:SoftwareAgent` is a subclass of `prov:Agent` and is defined simply as running software.

This is materially different from the modern AI-Agent sources in Steps 1–4.

The hierarchy is:

```text
prov:Agent
├── prov:Person
├── prov:Organization
└── prov:SoftwareAgent
```

The important observation is that `SoftwareAgent` does not require autonomy, goals, reasoning, planning, tools, memory, or adaptation in the definition. The ontology is concerned with provenance responsibility and participation.

**Alignment:** `AI Agent` could potentially be modeled as a specialization of `SoftwareAgent` in a provenance context, but this would be an application-level modeling choice, not an asserted equivalence.

**Challenge:** autonomy and LLM-based reasoning are not necessary conditions for `prov:Agent` or `prov:SoftwareAgent`.

## 3. FAA SWIM Controlled Vocabulary

The FAA SWIM vocabulary defines `software agent` as:

> "A running program that drives services, both to implement them and to access them."

The definition cites the W3C Web Services Architecture source.

This provides another stable, non-LLM interpretation of software agent. It emphasizes software that implements or accesses services, rather than autonomy, planning, memory, or reasoning.

**Alignment:** strongly related to the implementation/system dimension identified in Step 4.

**Challenge:** an agent can be defined as software acting in a service environment without the properties that dominate current LLM-agent discussions.

## 4. Finnish KTDDE Vocabulary (SKOS)

The Finnish interoperability vocabulary has a concept `agent` with preferred term `agent` and alternative labels `participant` and `actor`. Its definition describes an entity capable of acting or being assigned responsibilities in a trade process, typically a person or organization, and in some contexts an automated software agent. Its broader concept is `business actor`.

This is another strong example of `agent` as a role/actor concept rather than an AI architecture.

**Alignment:** useful for the `role / actor / responsibility` dimension.

**Challenge:** the concept explicitly spans human/organizational actors and automated software agents; it does not require autonomy or LLM capabilities.

## 5. What the external vocabularies add

The lookup produces four important observations.

### A. `Agent` is not intrinsically an AI term

The mature vocabularies reviewed use `Agent` in several established senses:

- responsibility-bearing participant (`prov:Agent`)
- person / organization / software agent (`prov:Person`, `prov:Organization`, `prov:SoftwareAgent`)
- software that drives or accesses services (FAA SWIM)
- actor/participant in a business process (KTDDE)
- corporate/document/procedural participant in EU metadata

Therefore, the modern LLM/AI usage is a domain-specific specialization or evolution of a much broader term, not the universal meaning of `Agent`.

### B. `SoftwareAgent` is a more useful bridge term than `Agent`

W3C PROV-O and FAA SWIM provide a bridge from the general `Agent` concept to software. This may be more useful for future alignment work than trying to align modern `AI Agent` directly with the generic word `Agent`.

### C. Autonomy is not a universal semantic requirement

Several established vocabularies describe agents without requiring autonomy. This directly challenges any attempt to promote autonomy to a universal necessary condition of `Agent`.

### D. The external vocabularies reinforce the need for context

The same lexical label can legitimately denote different concepts in different vocabulary schemes. Therefore, an alignment workflow should first identify the vocabulary/context and only then evaluate semantic relationships.

## 6. Preliminary alignment map

| External concept | Relationship to current `AI Agent` research concept | Useful observation |
|---|---|---|
| EuroVoc `Agent` search | No direct AI-Agent match found | Absence of a match is informative but not proof of absence |
| EU Corporate Body / Agent usage | Distinct | Agent as institutional/procedural participant |
| `prov:Agent` | Broader / different modeling purpose | Responsibility-bearing entity, not necessarily software or autonomous |
| `prov:SoftwareAgent` | Related / possible bridge | Running software; subclass of `prov:Agent` |
| FAA `software agent` | Related | Software that drives/accesses services |
| KTDDE `agent` | Related but distinct | Actor/participant/responsibility concept, with automated software as one context |

## 7. Step 6 conclusion

The external lookup **does not give us an authoritative definition of modern AI Agent**. Instead, it does something more useful for the experiment: it demonstrates that the unqualified label `Agent` already spans multiple established semantic regimes.

The strongest finding is therefore not a candidate definition but a boundary condition for alignment:

> **Do not align `Agent` by lexical identity alone. Identify the vocabulary and semantic context first.**

For the next step, `SoftwareAgent` and related concepts may be more informative comparison anchors than the bare term `Agent`.

No VocBench concept has been created yet.
