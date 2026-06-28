# Changelog

All notable changes to the Prompt Stack are recorded here. The canonical method page is [dixon.ai/prompt-stack](https://dixon.ai/prompt-stack/); this repository tracks it.

## Unreleased

## 2.0.0 — 2026-06-28

A method revision (breaking: the first stage is renamed and re-scoped). Prompted by an independent critique from three frontier models from different labs (GLM, DeepSeek, Qwen), which all flagged the same thing: telling an AI to "be sceptical" changes its tone, not its accuracy. The field has moved past stance-prompting, so the method moved with it.

- **ROLE → SCOPE (breaking).** The first stage no longer sets a sceptical stance. It now *fences in what the AI may use* and *forces it to admit uncertainty or a knowledge cutoff* instead of guessing. This is the change with the most effect on real error, especially on questions whose answer moves over time (prices, rates, current rules).
- **FILTER strengthened.** No longer just "split facts from inference." The model must now *label every claim* `[sourced]` / `[inferred]` / `[guessed]`, so the answer becomes a checkable map of what to trust rather than smooth prose.
- **RISK and VERDICT unchanged.** Both still earn their place exactly as in 1.0.0.
- **The quick-check pre-step ("Check One, Bin the Lot") unchanged.**
- **New cross-model capstone (not a fifth stage).** For high-stakes answers: run the same prompt through a second AI from a different lab and investigate wherever they disagree. Drawn from the AI Reliability Scoreboard work at dixon.ai.
- Combined one-prompt version updated to match; `CITATION.cff` bumped to 2.0.0.

## 1.0.0 — 2026-06-15

First versioned release, brought in line with the rewritten method page at [dixon.ai/prompt-stack](https://dixon.ai/prompt-stack/).

- **Universal-first framing.** The method is now described as working on any decision — a holiday deal, a doctor's letter, a phone contract — and pushed hardest where a wrong answer costs real money. Investing is the proving ground, not the scope. Replaces the earlier "for AI investment analysis" framing.
- **Two-layer structure.** A universal core (the everyday method) above a finance proof layer (the same four stages run on real positions, with the exact finance prompts and worked examples).
- **ROLE reframed — stance, not costume.** ROLE sets the sceptical stance you want the answer judged by, not a job title or persona. A grand title buys no accuracy; the sceptical instruction does.
- **Added the quick-check pre-step.** A two-question check, run before the four stages, that the answer is even about the right thing: name the exact thing it's looking at, and hand over one fact you can check in under a minute. Deliberately un-named.
- **Added the combined ~200-word prompt** that runs all four stages in one pass.
- Added `CITATION.cff` and this changelog.
