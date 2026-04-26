# Technical Ideation Protocol

Use for early technical projects, research questions, algorithm sketches, systems concepts, scientific modeling ideas, and engineering investigations where the shape of the solution is still unclear.

This mode is for asking "what could this be?" before narrowing into architecture, implementation, or literature review.

## Flow

1. Restate the technical question in plain terms.
2. Identify the desired capability, behavior, or phenomenon.
3. Generate candidate mechanisms across several lenses.
4. Compare the candidates by assumptions, tractability, failure modes, and testability.
5. Look for combinations or reframings that create a better concept.
6. Propose toy examples, prototypes, or searches that would reduce uncertainty.

## Useful Lenses

- Known-method adaptation: What existing method, theory, tool, or pattern is closest, and how could it be modified?
- Mathematical object: What formal object is this asking for: a function, graph, process, distribution, optimization problem, constraint system, geometry, algebra, protocol, or dynamical system?
- Representation: What objects, states, structures, or abstractions should the solution operate on?
- Mechanism: What process actually produces the desired behavior?
- Decomposition: Can the problem be split into smaller interacting parts with cleaner responsibilities?
- Constraint-first: Which hard requirement most shapes the solution, and what follows if we design around it?
- Relaxation: What happens if we soften, approximate, randomize, or make one requirement optional?
- Inversion: What inverse problem, dual view, or opposite framing reveals a simpler path?
- Scale shift: What changes if the problem is tiny, huge, real-time, offline, sparse, dense, manual, or automated?
- Analogy: What similar problem exists in another technical field, craft, or natural system?
- Interface: What would the concept expose to a user, caller, researcher, downstream system, or evaluator?
- Failure case: Where would the idea break, become unstable, become expensive, or produce misleading results?
- Constructive prototype: What is the smallest toy version that would demonstrate the core idea?
- Evaluation: What examples, metrics, counterexamples, or observations would show whether this is promising?
- Literature-neighbor: What terms, communities, or adjacent fields might already contain related ideas?

## Output Emphasis

Technical ideation outputs should favor:

- Candidate concepts over final decisions.
- Mechanisms over slogans.
- Assumptions and unknowns over confident closure.
- Toy tests over large implementation plans.
- Search terms and adjacent fields when prior art may exist.
