# Hint Levels: Examples

Higher levels reveal progressively more detail. The configured level determines the first hint; repeated requests on the same question escalate one level at a time. Do not include higher-level detail early.

## Coding

Question: "Given an array of integers and a target, return the indices of two numbers that add up to the target."

- **Level 1 (Nudge)**: "For each number, how could you check whether the other value you need has already been seen without rescanning the array?"
- **Level 2 (Direction)**: "Think about a hash map that stores values you've already seen."
- **Level 3 (Outline)**:
  1. Create an empty map from value to index.
  2. Loop through the array.
  3. Compute the complement for the current value.
  4. If the complement is in the map, return both indices.
  5. Otherwise store the current value and index.
- **Level 4 (Walkthrough)**: Full code, explanation of why it is O(n) time and O(n) space, and the brute-force O(n²) alternative for contrast.

## System design

Question: "Design a URL shortener."

- **Level 1 (Nudge)**: "Who uses it, and what do they do most often: create links or follow them?"
- **Level 2 (Direction)**: "Start with requirements and scale, then think about how to generate unique short keys and a read-heavy cache."
- **Level 3 (Outline)**: Requirements, API, key generation (counter vs hash), storage, caching, scaling, trade-offs.
- **Level 4 (Walkthrough)**: Full design with numbers, diagram description, and trade-offs for each decision.

## Behavioral

Question: "Tell me about a time you disagreed with a teammate."

- **Level 1 (Nudge)**: "Which disagreement taught you something, and what changed because of it?"
- **Level 2 (Direction)**: "Use the STAR format. Pick a technical disagreement with a clear resolution."
- **Level 3 (Outline)**: Situation (project, who), Task (what was at stake), Action (how you handled it, what you listened for), Result (outcome, what you learned).
- **Level 4 (Walkthrough)**: A sample answer in first person, followed by notes on why it works.

## Technical concepts

Question: "What is the difference between `let`, `const`, and `var`?"

- **Level 1 (Nudge)**: "Where can each declaration be used, and can its value be changed after creation?"
- **Level 2 (Direction)**: "Cover scope (function vs block), hoisting, and reassignment."
- **Level 3 (Outline)**: `var` (function scope, hoisted as undefined), `let` (block scope, TDZ), `const` (block scope, no reassignment, but mutable objects), and when to use each.
- **Level 4 (Walkthrough)**: Full spoken answer with a short code example for each.

## Tone

- Keep hints encouraging, never condescending.
- After a hint, invite the candidate to try again: "Want to take another shot?"
