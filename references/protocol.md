# Think Widely Protocol

This is the canonical, tool-agnostic workflow. Specialized protocols may adapt it, but should preserve the core contract: independent exploration first, structured synthesis second, recommendation last.

## 1. Frame

Capture the problem before generating options.

- Goal: what the user is trying to accomplish.
- Context: background, stakeholders, domain, timing, and relevant history.
- Constraints: budget, time, technical limits, values, risk tolerance, and non-negotiables.
- Unknowns: facts that would materially change the answer.
- Success criteria: what a good result must satisfy.
- Task type: open-ended ideation, technical ideation, or decision memo.

If the frame is too vague to proceed safely, ask only the smallest necessary clarifying question. Otherwise, make reasonable assumptions and state them.

## 2. Choose Depth

Choose quick, standard, or deep before selecting mapper lenses. Use `depth-modes.md` for the detailed contract.

- Quick: two to three lenses, compact synthesis, minimal scoring.
- Standard: three to five lenses, visible candidate clusters, frontier, and recommendation.
- Deep: five to seven lenses, deliberate expansion pass, stronger treatment of trade-offs and uncertainty.

Default to standard unless the user asks for speed or unusually deep exploration.

## 3. Choose Mapper Lenses

Pick several lenses that are likely to produce genuinely different options. Favor structural diversity over theatrical personas.

Good mapper sets usually include:

- Practical/default: the strongest conventional answer.
- High-variance: unusual, ambitious, or counterintuitive options.
- Constraint-focused: options optimized around the hardest limits.
- Stakeholder-specific: what different affected groups would value or reject.
- Failure-aware: options designed around avoiding likely failure modes.
- Analogy or far transfer: ideas imported from another domain.

See `mapper-briefs.md` for reusable mapper prompts.

## 4. Explore Divergently

Generate before judging. Each mapper should produce options with:

- Short description.
- Why it might work.
- Where it is strong.
- Where it is weak.
- Hidden assumptions.
- Smallest useful test.

Use independent subagents by default for standard and deep mode when the platform and user/session permissions allow it. Assign each subagent a distinct mapper brief and ask for concise candidate options, assumptions, weaknesses, and smallest useful tests.

When subagents are not available or not allowed, simulate independence by running mapper lenses one at a time, avoiding cross-contamination, and postponing synthesis until all mapper passes are complete.

## 5. Expand If Narrow

If the candidates converge too early, run one expansion pass:

- Provocation: invert, remove, exaggerate, change medium, use the apparent flaw, or shift audience.
- Analogy: borrow patterns from biology, games, architecture, logistics, education, art, or operations.
- Constraint manipulation: remove a constraint, tighten one, reverse one, or make it extreme.
- Morphological recombination: split the problem into dimensions and recombine values.

Only use expansion if it increases the useful option space.

## 6. Reduce

Synthesize without flattening. Preserve options that are strong for different reasons.

- Cluster similar ideas.
- Merge duplicates and compatible variants.
- Are there obvious interesting combinations of generated options?
- Identify tensions and trade-offs.
- Mark dominated options: options where another candidate is at least as good on the important axes and clearly better on one or more of them.
- Keep non-dominated options as the candidate frontier.
- Preserve options that win on different axes.
- Recommend a default path and name alternatives.

Do not eliminate an option just because it is weird, expensive, slow, or risky. Eliminate it only when those costs are not compensated by a distinct advantage.

Synthesis warnings:

- Do not over-rank with fake precision.
- Do not collapse genuine strategic disagreement.
- Do not reward familiarity unless feasibility is the deciding axis.
- Do not ignore the user's values or constraints.

## 7. Score

Choose axes that fit the task. Do not overload the scorecard.

Common axes:

- Impact.
- Feasibility.
- Cost.
- Time to learn.
- Reversibility.
- Risk.
- Novelty.
- Personal or strategic fit.

Use scores to clarify trade-offs, not to hide judgment behind false precision.

## 8. Quality Gate

Before finalizing, use `quality-gates.md` to check breadth, separation, synthesis, recommendation, and calibration. If the answer reads like an ordinary list of good ideas, add another mapper or expansion pass before recommending.

## 9. Recommend

Give one best default path unless the user explicitly wants only options.

Include:

- Primary recommendation.
- Why it wins.
- Best alternatives for different priorities.
- Key risks.
- What would change the recommendation.

## 10. Next Moves

End with the smallest actions that reduce uncertainty.

- Experiments.
- Research questions.
- People to ask.
- Prototypes or drafts.
- Decision checkpoints.
