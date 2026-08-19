# Step 5 — Dimension Audit

## Purpose

Audit the analytical dimensions produced in Step 4. The goal is not to define Agent, but to distinguish source-grounded observations from cross-source analytical constructs and model-generated abstractions.

## Audit result

### R1 — Source-grounded

These are properties or distinctions that can be traced to at least one of the four source analyses in Step 2, without requiring the Step 4 framework itself:

- autonomy / autonomous operation
- goal or objective orientation
- perception / interaction with an environment
- action / execution
- reasoning
- planning
- adaptation
- internal state / context
- persistence / operation over time
- tool use / external interaction
- multi-step task execution
- collaboration or handoff with other agents
- identity / authentication
- human oversight / governance
- LLM or AI model as an implementation or, in A2, a defining engineering configuration
- prompts / instructions, tools, guardrails, hooks and orchestration as engineering mechanisms in A2

Important qualification: being source-grounded does **not** mean being a necessary or defining property of Agent. It only means that the source actually assigns the property some semantic role.

### R2 — Cross-source analytical constructs

These are useful dimensions for comparing the sources, but they are not themselves claims that the sources share a common ontology:

- **What is it?** — groups entity, role, identity and conceptual-status statements.
- **What does it do?** — groups externally observable behavior and task effects.
- **How does it operate?** — groups internal/runtime behavior such as reasoning, planning, state and adaptation.
- **How is it implemented?** — groups technical mechanisms and components.
- **How is it exposed & governed?** — groups interfaces, protocols, authentication, guardrails and human oversight.

These dimensions are analytical lenses created to compare heterogeneous source material. They should not be entered into the vocabulary as Agent ontology categories merely because they organize the current evidence.

### R3 — Model-generated abstractions / claims requiring caution

The following should not currently be treated as established source facts:

- “Autonomous software entity/system” as *the* core or necessary definition of Agent.
- “Perceive & Act” as a condition required by all four sources.
- A single unified Agent architecture such as `Profiling + Memory + Planning + Action` as a general definition of Agent.
- The claim that LLM, tools, memory, identity or name are simultaneously intrinsic conceptual properties across all sources.
- “Business value” as an intrinsic Agent property rather than an evaluation or product concern.
- “Human-like intelligence” as an Agent property; in the current material it is better treated as an aspiration or characterization.
- Any inferred hierarchy among the five Step 4 dimensions.

## Cross-cutting observations

### 1. A property can change semantic role by source

LLM, tools, memory/state and identity/name illustrate this. A property can be conceptual in one source, an operational mechanism in another, and an implementation or interface concern in another. Therefore a flat attribute list is insufficient for alignment.

### 2. “Required” has multiple meanings

A field being required by an API schema must not be interpreted as a conceptual necessary condition. Likewise, an implementation component being central to a framework does not establish that it is conceptually necessary for Agent.

### 3. Dimension boundaries are analytical, not ontological

The Step 4 dimensions are useful for asking different questions of the sources, but they should remain analysis scaffolding until independently validated.

### 4. Unclassified material is legitimate

Step 4 identified opaqueness and human-like intelligence as difficult to classify. This should be preserved rather than forced into a dimension. “Unclassified” is preferable to premature ontology.

## Step 5 conclusion

The Step 4 framework is **useful as a comparison lens, but not yet suitable as a vocabulary model**.

The experiment therefore should not encode these dimensions or their classifications in VocBench yet.

The next step can proceed to external vocabulary lookup, but the lookup should test the evidence rather than assume the Step 4 dimensions are part of the target vocabulary.
