# Open Questions

These questions identify current architectural uncertainties. They guide investigation without assuming that the provisional conceptual model is complete or that every question requires a new component.

## Instances, continuity, and self-modeling

1. **What constitutes an intelligence instance?** What defines its boundary across computation, state, and environments? What would distinguish continuation, copying, and branching?
2. **Is persistence fundamental to intelligence or optional?** Which capabilities require continuity, and which could be supported by short-lived instances?
3. **Is identity fundamental, constructed, or emergent?** What establishes that an instance remains the same entity as its state and computational components change?
4. **Is self-modeling a system, an ability, or a consequence of more primitive mechanisms?** What would a self-model need to represent, and how would its usefulness be assessed independently of identity?

## Cognitive boundaries and adaptation

5. **What is the smallest useful set of cognitive primitives?** Which distinctions apply across different forms of intelligence, and which depend on an application or computational mechanism?
6. **What distinguishes abilities from systems?** Does the distinction clarify composition and state ownership, including cases where a capability spans several systems or a system supports several abilities?
7. **Is learning fundamentally different from general adaptation of internal state?** What makes a change count as learning, and does that distinction require additional semantics?

## Memory, evidence, and interpretation

8. **How should memories, beliefs, evidence, and uncertainty be represented?** How should provenance, conflicting observations, and revisable interpretations relate? When evidence changes, how should dependent beliefs be reconsidered without conflating retrieval with belief formation?

## Composition, coordination, and initiation

9. **Can distributed cognitive processes produce coherent behavior without centralized orchestration?** What coordination is necessary for compatible beliefs, commitments, and actions when components evolve or execute independently?
10. **What contracts are necessary for composability without prematurely standardizing cognition?** What must components share, and what representations and implementation choices can remain local?
11. **How should goals, intentions, and autonomous initiation be modeled?** What distinguishes a goal from an active commitment or a trigger for activity? How should initiation relate to attention, resource limits, and authority to act?

## Empirical validation

12. **How can the architecture be validated through small, meaningful experiments?** What behavior would test a proposed boundary or contract? What results would justify retaining, revising, or removing an abstraction, and how can those results be distinguished from the capabilities of one implementation?
