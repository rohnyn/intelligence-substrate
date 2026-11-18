# Intelligence Substrate

An open architecture for constructing persistent, composable, distributed artificial intelligences.

## Thesis

Intelligence should not be defined by a particular model, interaction paradigm, embodiment, or relationship with a user.

We are exploring a general-purpose substrate on which different forms of artificial intelligence can be constructed.

The architecture distinguishes three concepts:

- **Intelligence instances:** Persistent entities with continuity across computation, environments, and time.
- **Systems:** Independently evolving components that maintain state, implement domain-specific logic, and expose capabilities.
- **Abilities:** Composable behaviors such as observing, learning, reasoning, and acting, potentially involving multiple systems.

These are provisional abstractions, not a complete theory of intelligence.

## Principles

- No mandatory assistant, agent, or symbiote model.
- No dependency on a particular inference architecture, including LLMs.
- No requirement for a single centralized cognitive loop.
- State and computation should be independently replaceable.
- Abilities and systems should compose through explicit contracts.
- Logical components should support distributed execution without requiring separate services.
- Information, belief, identity, and authority must remain distinguishable.

## Approach

Start from conceptual invariants, validate them through small working implementations, and generalize only when necessary.

The goal is not to prescribe what intelligence must look like.

The goal is to make different implementations of intelligence possible.
