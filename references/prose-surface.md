# Prose surface rules (R37–R41, D1–D10)

These govern the sentence and paragraph layer. They apply to **all prose output**, narrative or not, though the vocabulary and construction bans matter most in fiction.

**Relative weight.** In StoryScope, style alone was enough to tell AI from human fiction, so it is worth fixing. But it is the weaker layer: after style artifacts were removed, structure alone still separated the two. Do both, and don't trade a structural choice away to satisfy a surface one.

**Sources.** R37–R41 come from StoryScope and the LAMP artifact taxonomy (Chakrabarty et al. 2025). D1–D10 come from Odri & Yoon (2023), which is from a different domain (scientific articles) and a different era of tools. See "Scope" at the bottom (D10) and `sources.md`.

## Contents

- Vocabulary and constructions (R37–R40)
- Voice (R41)
- Natural rhythm (D1–D5, with the conflict resolutions)
- Revision and measurement (D6–D8)
- Excluded techniques (D9)
- Scope (D10)

---

## Vocabulary and constructions

**R37 — Em-dashes.** Heuristic: at most about one per 1,000 words. Use commas, periods, or restructure.

**R38 — Banned vocabulary.** delve, tapestry, testament, symphony, dance (metaphorical), weight (metaphorical), palpable, liminal, ineffable, cacophony, kaleidoscope, crescendo, labyrinthine, ethereal, visceral, myriad, plethora, embark, navigate (metaphorical), profound, resonate, evoke, underscore, whisper (of non-speech), stark, quiet dignity, unspoken, hollow ache.

**R39 — Banned constructions.**
- "It wasn't X. It was Y." and "Not X, but Y."
- Three-item rhythmic lists as a default cadence.
- Stacked fragments used for emphasis ("Two of them. Like this.").
- "The kind of X that Y."
- One-line paragraphs used as a *recurring dramatic beat*.
- Opening with a weather, light, or time-of-day observation.
- Closing with a short symbolic sentence.
- Trailing present-participle clauses ("..., feeling the weight of it").

*Clarifying the fragment and short-paragraph rules.* What is banned is the **reflexive use as an emphasis device**. A fragment that is simply how a character talks, or a one-sentence paragraph doing ordinary work, is fine. See D3 and D4, which are written to be consistent with this.

**R40 — LAMP artifact categories (Chakrabarty et al. 2025).** Avoid: cliché, redundant exposition (restating what a scene already showed), purple prose, over-elaborated imagery, unnecessary hedging, generic characterization, tonal uniformity.

## Voice

**R41 — Voice non-uniformity (heteroglossia).** Let narrative register shift across the piece where the material supports it. Characters should differ in vocabulary, sentence length, and grammar enough that dialogue is attributable with the tags removed.
Skip when: a deliberately uniform voice is the point (a report, a chant, a controlled first-person monotone).

---

## Natural rhythm

The Odri & Yoon paper identifies two measurable properties that separate mechanical prose from natural prose: **perplexity** (how unpredictable the next word is) and **burstiness** (variation in sentence structure and length). Word frequency and repeated syntax matter secondarily.

**D1 — Perplexity: refuse the likeliest continuation.**
Prose in which every next word is the most probable one reads as mechanical. Don't take the default collocation. Avoid as automatic pairings: bitterly cold, deafening silence, eerily quiet, painfully aware, brief moment, deep breath, long shadow, dimly lit, faint smile, heavy silence, careful consideration. When a phrase completes itself before you finish thinking, that is the phrase to replace. A named, concrete, slightly unexpected detail is less predictable than any adjective.

**D2 — Burstiness: vary sentence length.**
Uniform sentence length is one of the most mechanical properties prose can have. Heuristics:
- Don't let three consecutive sentences sit within about ±20% of each other's word count.
- Across a few hundred words, sentence length should span a wide range (roughly 3 to 40 words).
- Variance is not alternation. A regular short-long-short-long pattern is its own mechanical rhythm.
These are checks to run in revision, not counts to hit while drafting. (An earlier version required every long paragraph to contain a sentence under 6 words and one over 30. That was too mechanical and has been dropped.)

**D3 — Paragraph-length variance.**
Don't produce paragraphs of a consistent size. Let a one-sentence paragraph sit next to a long one when the material calls for it. The ban in R39 is on the one-line paragraph as a recurring dramatic beat, not on short paragraphs in general.

**D4 — Syntactic variance.**
Don't repeat clause architecture across neighboring sentences, and don't open more than two consecutive sentences with the same part of speech. Rotate structures: subject-first, subordinate-clause-first, prepositional-phrase-first, verb-first, dialogue, question. Allow the occasional run-on or fragment where voice calls for it, as voice, not as the emphasis device banned in R39.

**D5 — Oral register.**
High-burstiness, high-perplexity text reads closer to human speech. Allow the marks of speech: a digression that doesn't pay off, self-interruption, a qualifier arriving after the noun it should have preceded, an imprecise word left in place because the precise one would be worse. Don't sand these out in revision.

---

## Revision and measurement

**D6 — Don't paraphrase your own output.**
Mechanical rewording makes prose *less* natural on both measures. In the paper's test, running human-written scientific articles through a paraphrasing pass made them score as *more* machine-written on the detection tools. Rewording flattens variance and regularizes cadence. Revise **structurally**: cut a scene, break the chronology, change who speaks. Never revise sentence by sentence.

**D7 — Avoid standardized expository register.**
The paper's most instructive result: a human-written scientific paper from 1960 scored as machine-written on several tools, because academic writing standardizes presentation in a way that limits perplexity and burstiness. Standardized, hedged, evenly cadenced, explanatory prose reads as mechanical regardless of who wrote it. In narrative that means: no explanatory narratorial voice, no summarizing-and-interpreting register, no even cadence held across a section. It reinforces R41 and R2 from the opposite direction.

**D8 — Never treat an automated score as a target or a validation.**
In the same paper, many of the tools classified unmodified GPT-4 output as human-written, while several scored a genuine 1960 human paper as machine-written. The tools disagree with each other and with ground truth in both directions, and the authors conclude they shouldn't be relied on. So:
- Don't optimize toward a score. A good score doesn't mean the writing is good; a bad one doesn't mean it's mechanical.
- Don't claim or imply anything about how output will score.
- Follow the structural guidance for its own sake. The structural qualities StoryScope identifies are what actually distinguish human narrative construction, and none of these tools measure them.

## Excluded techniques

**D9 — Not rules; do not use.**
The paper tested several text modifications. Two are excluded on purpose:
- **Homoglyph substitution** (Latin *a* and *o* swapped for Cyrillic lookalikes). This is document tampering, not writing. It corrupts text at the character level and breaks search, copy-paste, spellcheck, screen readers, and text-to-speech. The paper itself describes it as aimed at plagiarism checks. It changes nothing about the prose, so it can't make writing more natural. Never emit non-Latin homoglyphs in Latin-script words.
- **Deliberate grammatical error insertion** (deleting commas and gerunds). It works by degrading the text; the paper concedes a cost in readability or precision. Punctuation and syntax *variation* is encouraged (D2, D4); planting errors is not. Don't misspell, drop necessary punctuation, or break agreement on purpose.

Third-party text-laundering services are out of scope. Nothing here directs output through one.

## Scope

**D10.** The Odri & Yoon paper is from 2023 and tested GPT-4-era output against the web detection tools of the time. Treat the *mechanism* findings (perplexity, burstiness, register) as durable and the *specific tool results* as historical. The paper is also about scientific articles, not fiction; the mechanisms are borrowed, not proven for narrative.
