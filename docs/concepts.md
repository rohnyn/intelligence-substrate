# Current Conceptual Model

Intelligence Substrate explores a general computational abstraction for constructing different forms of artificial intelligence. This document describes current concepts, architectural commitments, and working hypotheses. It does not define a complete theory of intelligence or a fixed implementation architecture.

## Intelligence as a general computational abstraction

The substrate should support different forms of intelligence without prescribing how they interact with their environments. Personal assistants, embodied intelligences, autonomous researchers, and collectives are potential applications. None supplies the mandatory organizing model for the substrate.

Computation may use different inference mechanisms, and an intelligence need not be identified with any particular model or execution. Observation, interaction, and action may occur through different environments and interfaces. A privileged human user or request-driven conversation is not assumed.

## Abilities

Abilities are first-class, composable cognitive capabilities. Candidate abilities include:

- **Observing:** Acquiring and interpreting information from an environment.
- **Learning:** Adapting representations or behavior in response to experience or feedback.
- **Reasoning:** Working with information and interpretations to draw conclusions or consider possibilities.
- **Acting:** Producing effects in an environment within the applicable authority.
- **Introspecting:** Examining accessible internal state or processes.
- **Initiating:** Starting activity without requiring an immediate external request.

An ability may compose other abilities or functionality supplied by multiple systems. Reasoning, for example, may use observations, retained evidence, and a current goal. A memory system may support both reasoning and learning.

An ability does not necessarily correspond to a service or process. This list is provisional, and its boundaries should be tested rather than treated as a complete inventory of cognition.

## First-class systems

Systems own particular responsibilities, state, and domain logic, and expose capabilities through explicit contracts. Candidate systems include:

- Memory
- Knowledge
- Senses
- Identity
- Relationships
- Self-model
- Goals and motivation
- Attention
- Actions and authorization

These are exploratory conceptual boundaries, not a finalized service architecture. Naming a system does not require a separate module, process, or deployment, nor does it establish that every intelligence instance needs it.

Systems should be independently evolvable and composable. State ownership and exposed capabilities should be explicit enough that implementations can change without requiring other components to depend on their internal representations. State and computational mechanisms should be independently replaceable through suitable contracts; how to preserve meaning across replacements remains an open design problem.

Abilities describe capabilities, while systems describe responsibility and supporting functionality. Their relationship may be many-to-many. Whether this distinction remains useful in ambiguous cases, including learning, attention, and self-modeling, requires validation.

## Intelligence instances

An intelligence instance is provisionally understood as an entity with continuity across inference executions, environments, and computational components. Its continuity would be represented beyond any one execution, so that changing a computational mechanism need not define a new instance.

Persistence and identity are working hypotheses about useful instances, not established universal properties of intelligence. The criteria for continuity, the minimum state involved, and the consequences of copying or branching an instance remain unresolved. Identity also need not imply self-modeling: distinguishing an instance from another is a different concern from its ability to represent aspects of itself.

## Memory and knowledge

Several distinctions help keep retained information and its interpretation clear:

- **Observations and experiences** record situated inputs or interactions, including their context where available.
- **Beliefs and interpretations** express what an intelligence provisionally concludes from information.
- **Evidence and provenance** connect claims to supporting material, sources, and circumstances.
- **Associative retrieval** finds potentially relevant material, including through similarity.
- **Knowledge revision and uncertainty** concern how interpretations change, how conflicting claims coexist, and what remains unknown.

A reported statement is evidence that the report occurred; its content may still be mistaken. Retrieving a similar statement does not establish its truth or justify adopting it as a belief. Information retrieval and belief formation therefore need separate consideration.

Vector embeddings may support associative retrieval. Explicit structured representations may help express precise relationships. Neither is mandated as a universal knowledge representation, and neither independently resolves provenance, uncertainty, or contradiction.

The working preference is to distinguish stored observations and evidence from revisable interpretations and the mechanisms used to retrieve them. How beliefs depend on evidence, how corrections affect dependent conclusions, and how uncertainty is represented remain open. No storage technology is selected by these distinctions.

## Distributed cognition

Systems should be able to evolve independently and communicate through explicit contracts. Relevant state should have defined ownership, without requiring every component to share one mutable representation of cognition.

The architecture should not require:

- A single central agent loop.
- A global mutable cognitive state.
- A universal cognitive event taxonomy.
- A fixed hierarchy of cognitive processes.
- A one-to-one correspondence between cognitive concepts and deployed services.

Distributed execution should be possible without forcing every component into a microservice. Multiple responsibilities may share a process, and a capability may involve several components. A centralized coordinator may be useful in a particular implementation without becoming a universal architectural requirement.

Independent execution does not itself establish coherent behavior. Coordination, conflicting updates, failure, and the relationship between local state and shared commitments remain questions to investigate. No transport, scheduling mechanism, or consistency model is prescribed here.

## Identity, perspective, and authority

The architecture should distinguish:

- Who or what an entity is.
- What information an entity provides.
- What an intelligence believes about that information.
- What relationships exist between entities.
- What authority an entity has to request or authorize an action.

Information and instructions are not interchangeable. Content can be observed without being adopted as a belief or accepted as a directive. A belief about a source's credibility does not itself grant that source authority to authorize an action, and a relationship does not imply unrestricted authorization.

Different perspectives and conflicting accounts may coexist. Identity, credibility, relationships, and authorization should remain distinguishable even when an application relates them. The policies that connect them require explicit treatment rather than assumptions about a single controlling user.

## Conceptual layers

Three levels of description should remain distinct:

1. **Properties and capabilities of intelligence:** Concepts such as observation, learning, continuity, and reasoning.
2. **Software systems implementing those properties:** Responsibilities, representations, state ownership, and contracts.
3. **Computational infrastructure and deployment topology:** Where and how components execute and communicate.

These levels need not mirror one another. A conceptual distinction does not automatically imply a software component, and a software component does not automatically imply an independently deployed service. Infrastructure choices should support the chosen architecture without defining the meaning of intelligence.

## Design philosophy

Favor minimal abstractions, orthogonal responsibilities, replaceable implementations, and empirical validation. Treat the boundaries above as candidates to test through small, meaningful implementations.

Architectural commitments concern openness to different implementations, explicit contracts, and distinctions between information, belief, identity, and authority. Claims about universal primitives, persistent identity, and the sufficiency of distributed composition remain hypotheses.

An abstraction should earn its place by supporting observable behavior or enabling useful substitution and composition. Elaborate cognitive ontologies should wait until their necessity is demonstrated. The unresolved boundaries are collected in [Open Questions](open-questions.md).
