# Think Widely
This is an agent skill for open-ended problem solving and brainstorming. Meant to be used by Claude Code and Codex.
This skill approach tries a task from many different angles by spawning subagents with separate context, then summarizing.

It can for example be used early in software projects or for idea generation for other things (next family vacation, conference presentation topic, etc). It is meant to be used for decision points where it really matters and it is worth waiting a few minutes to get the "option frontier".

The different angles are inspired by
1. Techniques that have been shown to be effective (for example for creativity) in humans.
2. Techniques that have at some point worked for LLMs.
3. Creativity provocations, like Brian Eno's "Oblique Strategies".

## Human creativity / problem-solving techniques

This should be one reference file, probably references/expansion-techniques.md.

Include techniques like:
- Divergent → convergent split. Generate first, judge later.
- SCAMPER. Substitute, Combine, Adapt, Modify, Put to another use, Eliminate, Reverse.
- Analogy / far transfer. “What is this like in biology, games, architecture, parenting, logistics?”
- Morphological analysis. Break the problem into dimensions, recombine values.
- Constraint manipulation. Remove a constraint, exaggerate one, invert one.
- Nominal brainstorming / brainwriting. Generate ideas independently before combining, to reduce anchoring and production blocking.

## Techniques that have worked for LLMs

These should inform the main protocol where they add concrete behavior, rather than living in a separate reference file.

Examples:
- Self-consistency: sample multiple reasoning paths, then choose the answer supported by the most consistent paths. This improved performance across several arithmetic and commonsense benchmarks in the original paper.
- Tree of Thoughts: explore multiple intermediate “thoughts,” evaluate them, branch/backtrack when useful. The paper showed large gains on planning/search-like tasks such as Game of 24 and mini crosswords.
- Reflexion / critique loops: try, evaluate, learn from failure, retry.
- Divergent-convergent prompting: separate exploration from constraint satisfaction. Recent LLM creativity work has explicitly used this structure to improve diversity and novelty while preserving utility.
- Role/lens diversity, but carefully. Recent large-scale creativity comparisons suggest that “act as a genius/persona” prompting can be mixed or even counterproductive beyond a point, so the skill should favor structural diversity over theatrical persona stacking

## Oblique Strategies-like provocations

Oblique Strategies was created by Brian Eno and Peter Schmidt as a deck of provocative constraints/instructions to break creative blocks and induce lateral thinking. In the skill, this is a controlled randomness module, not the main workflow.

Include oblique-style prompts in references/expansion-techniques.md, grouped by function:
- Invert: What if the opposite were true?
- Remove: What assumption can be deleted?
- Exaggerate: What if this had to be 10× bigger/smaller?
- Change medium: What would this look like as a game, map, ritual, API, workshop, or story?
- Use the mistake: What apparent flaw could become the core?
- Shift audience: What would a child, skeptic, operator, artist, CFO, or future user see?

## Open-ended idea generation

For presentations, product ideas, strategy, writing, personal life, and other broad ideation tasks:

Constraint extraction
Divergent generation
Provocation pass
Analogy pass
Clustering
Ranking by criteria
Shortlist + next actions

Useful lenses:

Practical/default
Weird/high-variance
Personal-fit
Stakeholder-specific
Trend/zeitgeist
Budget/time constrained
“Delight” / emotional resonance
Failure-mode avoidance

## Technical ideation

For early technical projects, research questions, algorithm sketches, systems concepts, scientific modeling ideas, and engineering investigations:

Plain-language restatement
Desired behavior or capability
Candidate mechanisms
Assumption and failure-mode analysis
Toy examples or prototypes
Search terms and adjacent fields

# Design
It could be designed with a portable protocol bundle:
think-widely/
├── SKILL.md                      # ChatGPT / Codex Skill entrypoint
├── agents/
│   └── openai.yaml
├── references/
│   ├── protocol.md               # canonical tool-agnostic workflow
│   ├── technical-ideation.md     # early technical/research exploration workflow
│   ├── open-ended.md             # ideation workflow
│   ├── mapper-briefs.md          # independent exploration roles
│   ├── scoring-axes.md           # reusable axes by task type
│   ├── expansion-techniques.md   # creativity techniques and oblique-style prompts
│   └── output-formats.md

Each separate angle would produce one or more brief solution/option descriptions. A final summarizer step would then go through all produced options and preserve a diverse set of the best options along various axes.

It could produce something like an md file with:
# Option Frontier Result

## 1. Problem framing
- Goal:
- Context:
- Constraints:
- Unknowns:
- Success criteria:

## 2. Search strategy
Briefly list which mapper lenses were used.

## 3. Candidate option space
Grouped clusters, not yet final ranking.

## 4. Pareto frontier
The non-dominated options across the key axes.

## 5. Recommended path
One primary recommendation, plus why.

## 6. Experiments / next moves
The smallest actions that reduce uncertainty.

## 7. Rejected or dominated options
What was considered and why it fell off the frontier.

## 8. What would change my mind
Critical assumptions or missing facts.
