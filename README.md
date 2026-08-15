# The Prompt Stack

A four-stage method for getting reliable answers out of AI — on any decision. Built by Ben Dixon at [dixon.ai](https://dixon.ai).

Canonical home, with worked examples and a documented failure log: **[dixon.ai/prompt-stack](https://dixon.ai/prompt-stack/)**.

<!-- Last synced with dixon.ai/prompt-stack: 2026-08-15 (method unchanged at v2.0.0; docs + companion artefact refreshed) -->

---

## What it is

AI sounds exactly as sure when it's wrong as when it's right. A made-up figure arrives in the same calm, helpful voice as a correct one, so tone tells you nothing — and tone is what most of us are quietly judging on.

The Prompt Stack is one quick check on any answer, then four questions you run in order. It works on a holiday deal or a doctor's letter; it's pushed hardest where a wrong answer costs real money. The default AI response is fluent and quietly agreeable. The check and the four stages fight that.

Run them on any AI assistant — ChatGPT, Claude, Gemini, Perplexity.

---

## Before the four stages: one quick check

Before any of the four stages, run one quick check on the answer in front of you. It takes under a minute, and it's aimed at one specific trap: an answer that's confident, fluent, and quietly about something other than your problem.

The check is two questions — ask them before you trust a word:

1. **Name the exact thing.** Make it tell you precisely what it's looking at — the specific page, document or item — before it summarises anything. *"Which one is this, exactly?"*
2. **Hand me one fact I can check in under a minute.** One date, one number, one name you can hold against the real thing yourself.

**Check one, bin the lot.** Fail either question and the whole answer goes — not the wrong line, all of it. The good-looking paragraphs aren't a consolation prize. They're the part that nearly fooled you. Passing both questions doesn't make the answer right — it means it's about the right thing, and worth running the four stages on.

```
Before you answer anything else: name exactly what you're looking at — the
specific document or page in front of you. Then give me one fact about it I
can check myself in under a minute. If you're not sure what you're looking
at, say so before you go any further.
```

That clears the first trap. The four stages below are for the answer once you trust it's about the right thing.

---

## The four stages

Run in order. One question gets you one cheerful answer. Four questions, asked in order, each clear the ground for the next.

### 01 — SCOPE — Fence in what it can use, and let it say "I don't know"

Telling an AI to "be sceptical" changes its tone, not its accuracy. The move that actually cuts error is to fence it in: tell it exactly what it is allowed to draw on, and make it say plainly when a question is past its knowledge or training cutoff, rather than filling the gap. A grand job title buys you nothing. Constraining the source, and licensing an honest "I'm not sure," does.

```
Work only from the material I give you here, plus published sources you can
name (filings, official guidance, dated data). Do not fill gaps from memory.
If something I'm asking about is the kind of thing that changes over time (a
price, a rate, a current rule), or is past what you can verify, say so
plainly instead of guessing.
```

Good output: it works inside the fence, and flags what it can't stand behind. If it answers a live, moving question with a confident figure and no caveat, the scope hasn't taken. Most of what the later stages depend on gets set right here.

---

### 02 — FILTER — Make it label every claim

Most AI answers blend what the source actually says with what the model added on top, in the same confident tone. Don't just ask it to "be honest about uncertainty"; it can't reliably tell. Make it LABEL every claim: sourced, inferred, or guessed. You stop reading smooth prose and start reading a map of what to trust, and the "guessed" tags are where you look first.

```
Before forming any view, produce two lists, and tag every line.

LIST A — Observable facts, verifiable from the material above (stated
figures, dates, direct quotes, published data). Tag each one
[sourced: where it came from].

LIST B — Assumptions and inferences: anything depending on extrapolation,
projection, or interpretation. Tag each one [inferred] or [guessed]. If
uncertain which list a claim belongs on, put it in List B.

Do not move to analysis until both lists exist.
```

Good output: two clean lists with a tag on every line. Models smuggle assumptions into List A constantly; the tag forces the call into the open. Once the lists are clean, everything that follows is built on something you can check.

---

### 03 — RISK — Name what would prove the case wrong

"What are the risks?" gets you a checklist, and a checklist isn't the point. The question that matters is the one almost nobody asks: what exact thing would prove this wrong — a tripwire, not a vague worry. A risk you can't see in advance is background noise. A risk with a specific signal is something you can act on.

```
Identify:
(a) What could go wrong
(b) What would have to be true for the entire case to be wrong
(c) What observable signal would tell you it's going wrong — something
    specific enough to act on, with a timeframe

If you can't give a specific answer to (c), say so.
```

Good output: a tripwire, not a list of general risks. "Things might slow down" is not a tripwire; "the total at checkout comes out over £900" is. If the AI can't give a specific observable signal, it doesn't really have a view — it's pattern-matching off the consensus. That's a useful signal in itself.

---

### 04 — VERDICT — One action with a confidence level

Nobody standing at the checkout with their card out has ever been helped by a balanced six-paragraph essay on both sides. The last step stops the hedging: one answer, and how sure it is — low, medium or high. A confidence label you can hold it to later is worth more than a summary it can hide behind.

```
Give one practical action and a confidence level (Low / Medium / High) with
one sentence of rationale. State which assumption from List B the verdict
depends on most.

No hedged summary. One action.
```

Good output: one action, one confidence level, one sentence on the limiting factor. "Low confidence" is a valid answer. The honest upgrade, when it matters, is to ask the same thing again a different way and see if the answer holds — a verdict that survives a re-ask is one you can lean on.

---

## Run all four in one prompt

Copy this, paste your decision at the bottom, run. Running each stage separately lets you review and correct the output between steps — worth doing when real money is involved.

```
Work through this in four stages, in order. Do not combine stages or skip ahead.

STAGE 1 — SCOPE
Work only from the material I give you below, plus published sources you can
name (filings, official guidance, dated data). Do not fill gaps from memory.
If a figure is the kind that moves (a current price, rate or rule), or a
question is past what you can verify, say so plainly instead of guessing.

STAGE 2 — FILTER
Before forming any view, produce two lists, and tag every line:
LIST A — Observable facts, verifiable from the material above. Tag each
[sourced: where it came from].
LIST B — Assumptions and inferences: anything depending on extrapolation,
projection or interpretation. Tag each [inferred] or [guessed]. If uncertain,
put it in List B.
Do not proceed to Stage 3 until both lists exist.

STAGE 3 — RISK
Based on List A and List B only, identify:
(a) What could go wrong
(b) What would have to be true for the entire case to be wrong
(c) What observable signal would tell you it's going wrong — something
specific enough to act on, with a timeframe

STAGE 4 — VERDICT
Give one practical action and a confidence level (Low / Medium / High) with
one sentence of rationale. State which assumption in List B the verdict
depends on most. No hedged summary. One action.

Decision: [WHAT YOU'RE DECIDING — add any brief context here]
```

For anything that really matters, add one more step: run this same prompt through a second AI from a different lab, and dig wherever the two answers disagree. Different models fail in different places, so agreement narrows the odds and disagreement flags the thing to check. It's the idea behind the [AI Reliability Scoreboard](https://dixon.ai/scoreboard/).

---

## Where it's pushed hardest: real money

The same four stages run on real investing positions, where a confident wrong answer costs money. Worked examples, the exact finance prompts, and the posts where each one met a live decision:

- [The single prompt change that made AI analysis worth using](https://dixon.ai/posts/the-single-prompt-change-that-made-ai-analysis-useful/) — the FILTER stage, with a real worked example.
- [5 questions to ask AI before buying any stock](https://dixon.ai/posts/5-questions-to-ask-ai-before-buying-any-stock/) — the VERDICT stage, for the hour before you place the order.
- [7 AI prompts for covered calls](https://dixon.ai/posts/7-ai-prompts-for-covered-calls/) — the full stack applied to options income.

The full failure catalogue — every AI fabrication caught across these tests, with the prompt, the output, and the screenshot — is in the evidence register at [dixon.ai/evidence](https://dixon.ai/evidence/).

---

## The ready-to-paste version: the Bluff Filter

The Prompt Stack rewritten as standing instructions you hand to an AI assistant, so it runs the checks on itself. Five stages in that form (USE, then the four above), one page, CC BY 4.0. In this repo at [`BLUFF-FILTER.md`](BLUFF-FILTER.md), versioned separately from the Stack; delivered free, with the full method and worked examples, at **[dixon.ai/method](https://dixon.ai/method/)**.

The fortnightly newsletter, Confidently Wrong, covers what each AI model got wrong and which one was bluffing: [dixon.ai/join](https://dixon.ai/join/).

---

## Teaching or building on this?

The licence below means yes, freely — courses, videos, tools, forks, all welcome. One ask: **link the canonical method page** ([dixon.ai/prompt-stack](https://dixon.ai/prompt-stack/)) wherever you teach or implement it, so your readers can find the original method, the worked examples, and the documented failure log behind it.

Badge, if you want one:

```markdown
[![Built on the Prompt Stack](https://img.shields.io/badge/built%20on-the%20Prompt%20Stack-E85423)](https://dixon.ai/prompt-stack/)
```

---

## Who made it

The Prompt Stack is by **Ben Dixon** at [dixon.ai](https://dixon.ai) — an editorial site about getting reliable answers out of AI, tested on real decisions. The method is run against a real investment portfolio: real money, real decisions, no demos.

---

## Licence

[CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) — share and adapt freely, credit "Ben Dixon, dixon.ai". See [`LICENSE`](LICENSE) for the full legal code and [`NOTICE`](NOTICE) for the attribution format.

---

*Not financial advice. This is a prompting method, not investment advice.*
