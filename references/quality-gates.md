# Quality Gates

Run these checks before finalizing a `think-widely` answer. Fix the answer if any important check fails.

## Breadth

- Did the answer use several meaningfully different lenses?
- Are at least some candidates non-obvious, high-variance, or imported from another frame?
- Did the answer avoid collapsing too quickly into the most familiar option?
- If subagents were available and allowed in standard or deep mode, were mapper passes kept independent?

## Separation

- Is divergent exploration visibly separate from synthesis?
- Are mapper outputs or candidate clusters shown before the final recommendation?
- Is critique delayed until after initial generation?

## Synthesis

- Are similar ideas clustered or merged?
- Are real trade-offs named instead of hidden behind a single ranking?
- Are dominated options rejected for clear reasons?
- Are weird, expensive, slow, or risky options preserved when they have a distinct compensating advantage?

## Recommendation

- Is there one best default path unless the user asked only for options?
- Are strong alternatives named for different priorities?
- Does the answer explain what would change the recommendation?
- Are next moves small enough to reduce uncertainty quickly?

## Calibration

- Does the answer avoid fake precision?
- Are key assumptions and unknowns explicit?
- Does the output match the chosen depth mode?
- Does the answer respect the user's stated values, constraints, and appetite for risk?
