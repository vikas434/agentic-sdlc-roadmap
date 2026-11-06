# Notes — 2026-11-06

Typed from the PDF beside it.

## Added notes

I am building a structured mental roadmap for working on any repository, brownfield or greenfield. It has to be
structured so an agent can understand it and deliver predictably. This is the first step: a glossary from
domain-driven design, plus grilling with docs. Later steps go from glossary to grill with docs, then to tickets,
implementation, PR reviews and deployment.

## Domain language

- We need a common language that a human or an agent can understand.
- We can name it `GLOSSARY.md`.
- We need a "domain modelling" skill.
- Diagram: a human on the left, an agent on the right, the product on top. All three point into one box, "Domain
  language". Under it: TALK IN SAME LANGUAGE.
- Inspired by "Domain Driven Design".
- Explore: read the internals of the book and create a skill from it.

## Grill with docs

- Relentlessly ask the AI to grill you, so both of you are on the same page.
- Before that, we need the same glossary.
- Example: "Refund" or "Return" or "Cancel".

## Domain modelling

- Keep ADRs (Architecture Decision Records).
- Offer an ADR when a decision is:
  - hard to reverse
  - based on a trade-off
- Diagram, the folder layout:
  - `GLOSSARY.md`: understand what is difficult to understand
  - `docs/adr/0001`, `docs/adr/0002`: hard decision records

## Writing an ADR

- While grilling, we update the glossary, then decide which decisions should be recorded.
- A decision can be a tech decision or a business decision.
- Think about any business decision being made, using another skill called `/grill-me-with-docs`.
- Once the glossary is updated, the skill really helps. It asks the right questions.
- This exercise has to be done manually.

## Try this

- Try this in each repository.
- Open question: do we create a glossary for one repo or for multiple repos?

## Pruning the glossary

- Over time the glossary keeps getting bloated.
- It needs cleaning on a regular basis.
- Use `/grill-with-docs` to discuss and prune unused glossary entries.
- Tip 1: implementation details should not be added, e.g. "Refund" DB details. The implementation can change, and the
  code should be the source of truth.
- Tip 2: no coding-language details (React, Java, etc.). We don't need them here.

## Pruning ADRs

- We need to clean ADRs in the same way.
- Remember, ADRs are (based on the DDD book):
  1. hard to reverse
  2. surprising
  3. based on a trade-off
- Use the same skill, `/grill-with-docs`, to prune ADRs.
- Idea: can we make these documentation updates (glossary, ADR) a loop?
  - On every merge: crossed out, too much change.
  - A regular async job: chosen.

## Summary of chapter 1

- In DDD, a company uses a single language to talk. Try to keep that language.
- For this, keep the same bounded context. Use the `/domain-modelling` skill.
- Diagram, the pipeline: grill with docs → to specs → to tickets → to implement → code review.

## Choosing good words

- The language should use the words users might be using. This makes it easy to use.
- Go slowly: create only the entries we need, and grow as needed.
- Terms to look up: bounded context, ubiquitous language.
- To read: "Domain Driven Design".
