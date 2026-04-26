# Output Formats

Use the format that fits the user's task and desired depth.

## Option Frontier Result

```markdown
# Option Frontier Result

## 1. Problem Framing

- Goal:
- Context:
- Constraints:
- Unknowns:
- Success criteria:

## 2. Search Strategy

List the depth mode, mapper lenses used, and whether mappers were run through subagents or simulated independent passes.

## 3. Mapper Findings

Briefly preserve the distinct options or insights from each mapper before synthesis.

## 4. Candidate Option Space

Grouped clusters, not final ranking.

## 5. Pareto Frontier

The non-dominated options across the key axes.

## 6. Recommended Path

One primary recommendation, plus why.

## 7. Experiments / Next Moves

The smallest actions that reduce uncertainty.

## 8. Rejected Or Dominated Options

What was considered and why it fell off the frontier.

## 9. What Would Change My Mind

Critical assumptions or missing facts.
```

## Short Form

Use when the user wants a quick answer:

```markdown
## Search Strategy

## Best Default

## Strong Alternatives

## Trade-Offs

## Next Moves
```
