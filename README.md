# Junction-LLM

**A local open-source LLM at every major junction of every pipeline — thinking, acting, responding, autonomously.**

The pattern: wherever a pipeline has a decision point, put a local LLM with hands (tools), eyes (context), and engine (runtime) right there. It thinks, acts, and hands off to the next junction. No cloud. No API bills. No babysitting.

*Entry for the Amazon Developer Hackathon ($138,000 prize pool) — AI agents track.*

## The pattern

```
Pipeline:  SOURCE → [SCREEN] → [DRAFT] → [FILE] → [TRACK]
                    LLM        LLM       LLM       LLM
                    hands      hands     hands     hands
```

Each junction is an LLM with tools that:
1. **Thinks** — reads the situation with a local open-source model
2. **Acts** — uses its tools (browser, API, files) to do the work
3. **Hands off** — passes clean output to the next junction

Junctions hand failures backward too: verify-fail → rebuild, rejection → fix → resubmit.

## First implementation: the gig worker

A local Qwen 2.5 Coder 7B that screens freelance gigs, drafts proposals, and files applications — running on a CPU box for $0. See [local-gig-agent](https://github.com/michaelwoolum50-cmyk/local-gig-agent).

## Why it matters

Cloud agents charge per token and phone home with your data. Junction-LLMs run on hardware you own, cost nothing to operate, and answer to nobody but you. Same intelligence, zero rent.

## Status

🚧 **In build** — deadline: October 23, 2026.
