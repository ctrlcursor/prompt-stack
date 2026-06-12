# Prompt Stack

A four-stage method for AI investment analysis. Built by Ben Dixon at [dixon.ai](https://dixon.ai).

<!-- Last synced with dixon.ai/prompt-stack: 2026-05-24 -->

---

## What it is

Four prompts, run in order. Each stage has a job. Run them on any AI assistant before making an investment decision.

The method works because the default AI response is helpful and quietly bullish. These prompts fight that.

---

## The four stages

### ROLE — Set a sceptical stance

Before asking your question, set the stance.

```
You are a cautious analyst reviewing this for a risk committee, not a salesperson.
Your job is to find what could go wrong, not to validate the idea. Be specific.
```

Good output: a distinct framing, not generic hedging. If the model sounds like a disclaimer generator, the role hasn't taken.

---

### FILTER — Separate facts from inference

```
List only what is directly observable from the source material — prices, dates,
stated figures, management quotes. Label everything else as inference or assumption.
```

Good output: two columns (observable / inference). If column one is thin, you don't have enough data to proceed.

---

### RISK — Name what would prove the case wrong

```
Name the single timing risk, the realistic downside scenario, and one observable
signal that would prove this view wrong within [your timeframe].
```

Good output: a tripwire, not a list of general risks. "Revenue growth slows" is not a tripwire. "Revenue guide comes in below $X next quarter" is.

---

### VERDICT — One action with a confidence level

```
Based only on the observable facts identified above, give one specific action
(buy / sell / hold / wait for X event) with a confidence level (high / medium / low).
Hedging into a balanced summary is not an answer.
```

Good output: one action, one confidence level, one sentence explaining the limiting factor. "Low confidence" is a valid answer.

---

## How to use it

Run the stages in order on the same question. Each stage uses the output of the previous one as context. Takes 10–15 minutes on a real position. Works with any AI assistant (ChatGPT, Claude, Gemini, Perplexity).

---

## What it doesn't cover

- Live market data — AI assistants have knowledge cutoffs and most fabricate options chain data when asked
- Options pricing and Greeks — requires real-time chain data, not LLM inference
- Tax implications — jurisdiction-specific, consult a professional
- Position sizing — the method flags risks; it doesn't size trades

---

## See it in practice

Real trade examples from a real portfolio:

- [7 AI prompts for covered calls — the ones I actually use](https://dixon.ai/posts/7-ai-prompts-for-covered-calls/)
- [The single prompt change that made AI analysis worth using](https://dixon.ai/posts/the-single-prompt-change-that-made-ai-analysis-useful/)
- [5 questions to ask AI before buying any stock](https://dixon.ai/posts/5-questions-to-ask-ai-before-buying-any-stock/)

---

## Full methodology and Field Guide

Complete documentation, real trade examples, and the free Field Guide PDF (~20 pages):
[dixon.ai/prompt-stack](https://dixon.ai/prompt-stack/)

---

## Stay updated

The weekly newsletter — new prompts tested on real positions, plus what each model got wrong — at [dixon.ai/newsletter](https://dixon.ai/newsletter/).

---

## Teaching or building on this?

The licence below means yes, freely — courses, videos, tools, forks, all welcome. One ask: **link the canonical method page** ([dixon.ai/prompt-stack](https://dixon.ai/prompt-stack/)) wherever you teach or implement it, so your readers can find the original method, the worked examples, and the documented failure log behind it.

Badge, if you want one:

```markdown
[![Built on the Prompt Stack](https://img.shields.io/badge/built%20on-the%20Prompt%20Stack-FF5A00)](https://dixon.ai/prompt-stack/)
```

---

## License

[CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) — share and adapt freely, credit "Ben Dixon, dixon.ai".

---

*Not financial advice. This is a prompting methodology, not investment advice.*
