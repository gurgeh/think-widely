---
name: think-widely
description: Use when a user wants open-ended problem solving, brainstorming, strategy exploration, option generation, or an option-frontier synthesis before choosing a direction. Especially useful for high-value decisions where independent exploration, diverse lenses, critique, and structured convergence are worth the extra time.
---

# Think Widely

Use this skill for decisions or idea-generation tasks where the user wants more than a single plausible answer. The core pattern is independent exploration first, structured synthesis second, recommendation last.

## Workflow

1. Frame the task: goal, context, constraints, unknowns, success criteria, and whether the work is open-ended, technical ideation, or decision-heavy.
2. Choose a depth mode: quick, standard, or deep. Default to standard unless the user asks for speed or extra depth.
3. Choose mapper lenses that explore meaningfully different parts of the option space.
4. Run divergent exploration before judging. Use independent subagents by default when the platform and user/session permissions allow it; otherwise simulate independent mapper passes one at a time.
5. Make the breadth visible: briefly name the lenses used and preserve distinct candidate clusters before synthesis.
6. Add a provocation or analogy pass if the candidate space feels narrow.
7. Reduce the candidates into clusters, trade-offs, and a Pareto frontier. Optionally construct new candidates as combinations of the generated.
8. Run a quality gate before finalizing.
9. Recommend a path, name strong alternatives, and list experiments or next moves that reduce uncertainty.

## References

- Read `references/protocol.md` for the canonical tool-agnostic workflow.
- Read `references/depth-modes.md` to choose scope, number of mappers, and output detail.
- Read `references/open-ended.md` for presentations, product ideas, writing, personal life and other ideation-heavy tasks.
- Read `references/technical-ideation.md` for early technical projects, research questions, algorithm sketches, systems concepts, and engineering investigations.
- Read `references/mapper-briefs.md` when selecting independent exploration lenses.
- Read `references/scoring-axes.md` when choosing evaluation criteria.
- Read `references/expansion-techniques.md` when a lateral-thinking, analogy, constraint, or creativity-technique pass would help.
- Read `references/quality-gates.md` before finalizing the answer.
- Read `references/output-formats.md` when producing the final result.
