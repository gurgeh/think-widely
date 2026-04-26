# Depth Modes

Choose a depth mode before selecting mapper lenses. Default to standard unless the user asks for speed, explicitly asks for depth, or the decision is unusually high stakes.

## Quick

Use when the user wants a fast answer, the decision is low stakes, or the prompt is narrow.

- Use two to three lenses.
- Usually keep the work local rather than using subagents.
- Include a compact search strategy, best default, strong alternatives, trade-offs, and next moves.
- Skip scoring unless it clarifies a real trade-off.
- Use one provocation only if the first options are obviously generic.

## Standard

Use for normal `think-widely` requests.

- Use three to five lenses.
- Use independent subagents by default when the platform and user/session permissions allow it.
- Include at least one practical lens and one lens designed to create non-obvious options.
- Keep divergent mapper outputs separate from synthesis.
- Include candidate clusters, a frontier, a recommendation, and uncertainty-reducing next moves.
- Run a provocation or analogy pass if the options converge too early.

## Deep

Use when the user asks for breadth, the decision is expensive or hard to reverse, or the option space is genuinely unclear.

- Use five to seven lenses.
- Use subagents for independent mapper passes when available and allowed.
- Add a deliberate expansion pass: analogy, provocation, constraint manipulation, or morphological recombination.
- Consider a light scorecard across three to five axes.
- Preserve multiple frontier options that win for different values or constraints.
- Name what would change the recommendation.

## Downgrading Or Upgrading

Move down a mode when the user needs speed, the answer is obvious after framing, or added breadth would only create noise.

Move up a mode when early candidates are too similar, the user's values conflict, the stakes are high, or the best path depends on unknowns that cheap experiments can reduce.
