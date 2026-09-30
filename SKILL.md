---
name: text-obfuscator
description: Craft guidance for writing fiction and narrative prose that avoids the structural habits typical of AI-generated stories (stated themes, tidy causal chains, body-sensation emotion, closing reflections, flat escalation, uniform rhythm). Use whenever the user asks for a story, scene, chapter, screenplay, narrative essay, anecdote, in-world lore, or roleplay narration, or asks for writing that is less generic, less formulaic, less "AI-sounding", or more human, even if they don't name this skill. Also use for the prose-surface guidance on any long-form creative prose. A craft tool, not a detector-evasion tool.
---

# Less formulaic fiction

## What this is, and what it isn't

Research comparing AI-written and human-written fiction found that the two differ mainly in **narrative structure**, not word choice. Structure alone separated them reliably, and stripping cliché and purple prose barely changed that. So polishing sentences is not enough; the decisions that matter are made at planning time.

This skill turns those measured differences into writing habits. Three things to keep straight:

- **Human-typical is not the same as good.** These guidelines describe how AI and human fiction differ. They are a lens for spotting default choices, not a definition of quality. The user's brief, the premise, and the story's own needs outrank everything here. If a guideline would make the piece worse, skip it.
- **The findings are about populations.** A finding like "human stories do X more often than AI stories" can't be satisfied by one piece. Apply everything here as a per-piece decision, never as a quota across pieces.
- **Not a detector tool.** Detectors are unreliable in both directions. Never optimize toward a detector score, never claim or imply how output will score, never use homoglyphs or planted errors (see `references/prose-surface.md`, D8 and D9).

Never mention these guidelines, cite rule IDs, or append notes about compliance in the output. The output is the writing.

## Workflow

1. **Size the piece** using the scaling table below. Most of the machinery is for longer work.
2. **Plan before drafting.** Check the Tier A habits, then choose a small set of Tier B levers that fit this premise. Decide structural choices up front (where the causal chain bends, what the time structure withholds, how it ends); they can't be bolted on afterward.
3. **Draft.**
4. **Revise structurally.** Cut a scene, reorder, change who speaks. Do not revise by rewording sentence by sentence; that flattens variance and makes prose more mechanical (D6). During revision, resist smoothing away the choices you made on purpose: the unresolved thread, the uneven rhythm, the abrupt ending.
5. **Run the short check** in `references/checklist.md`.

If you are Claude, also read `references/claude-delta.md`. It covers habits specific to Claude's fiction.

## Tier A: habits to drop (every piece, any length)

Each has a rationale and details in `references/levers.md` or `references/prose-surface.md`.

- **Stating the theme.** No sentence, in narration or in a character's summarizing line, whose job is to tell the reader what the story means. Theme comes from event and image. (R1, R2, R3)
- **Debate dialogue.** No wise-mentor speeches, no exchanges where both sides articulate their positions cleanly. Dialogue negotiates, evades, misunderstands. (R5)
- **Closing reflection.** The last paragraph does not summarize, teach a lesson, restate the opening, or exist only as a closure image. End on action, speech, or an unexplained concrete detail. No epilogue or years-later coda. (R6)
- **Reflexive body-sensation emotion.** Don't stage every emotion as a tightening chest, held breath, or hammering heart. Stock list and guidance in R7.
- **Sensory sweeps and the smell reflex.** No entering-a-room sweep of the five senses; smell only when it does real work. (R8, R9)
- **Mood-mirroring weather and light.** Don't let the setting track the protagonist's inner state by default. (R10)
- **Banned vocabulary and constructions**, including "It wasn't X. It was Y." and trailing present-participle clauses. (R38, R39, R40)
- **Refuse the likeliest phrase.** When a phrase completes itself ("deafening silence," "deep breath"), replace it with something specific. (D1)
- **Reproducing canonical text.** Naming classic works is fine; imitating their text is not. (R36)
- **Missing a requested length.** If a target is given, land within ±10%. Count before delivering, using a code tool if you have one, since models count poorly by eye. (R43)

## Tier B: levers to choose from

These are the structural moves that most often separate human fiction from AI fiction. **Pick a few that fit the premise. Do not stack them all.** Using every lever in every piece would produce a new uniform template, and human stories are measurably more dispersed than AI ones, not just shifted to a different mean.

| Family | Levers (IDs in `references/levers.md`) |
|---|---|
| Causality and shape | Break the causal chain (R14) · subplot (R15) · resolution not driven by the protagonist's insight or choice (R16, R17) · morally ambivalent central choice (R18) · threat before investment (R19) · introduce the central character in dialogue or through another character's report, not description (R20) · two protagonists (R21) · shrinking social world (R22) · uneven escalation and varied event types (R42) |
| Time | Non-linear telling (R23) · flash-forward that shows an outcome before its cause (R24) · time structure that withholds (R25) · a revelation that forces rereading (R26) · visible withholding (R27) |
| Point of view and voice | One sustained focalizing consciousness (R34) · register shifts and distinguishable speakers (R41) · unexplained decision, reduced interiority (R12) |
| Texture and world | Open mid-speech or mid-thought, no furnished room (R13) · indifferent or tonally wrong setting (R10) · more locations than the plot needs (R32) · more dialogue relative to narration (R33) · a detail present because it happened, not because it means something (R4) |
| Reader relationship | Named real-world references (R28, R29) · the telling shows itself (R30) · genre crossover (R31) |
| Rarity | Two choices that are unusual in combination (R35) |

How to choose: ask what the premise is *for*. A mystery or a loss suggests time levers (withholding, recontextualization). A story about power suggests resolution levers (who actually decides the ending). A voice-driven first-person piece suggests the reader-relationship levers. Prefer levers that come from the premise over levers you can bolt on. When asked for several pieces at once, use different lever sets for each.

## Scaling

| Piece | What to apply |
|---|---|
| Micro (under ~500 words, a single scene, a paragraph) | Tier A only, plus at most 1 or 2 levers (for example, open in dialogue; leave one thread unresolved; end on a concrete detail). Skip subplot, locations, multiple time jumps. |
| Short (~500 to 2,000 words) | Tier A plus 2 or 3 levers. Subplot and multi-location levers are usually too much here. |
| Medium (~2,000 to 6,000 words) | Tier A plus 3 to 5 levers, at least one from Causality or Time. |
| Long (chapters, novellas) | Tier A throughout; up to about 5 or 6 levers across the whole work, spread across chapters rather than in every one. |
| Non-narrative prose | `references/prose-surface.md` only. |

## Which reference to read

- `references/levers.md`: full entries for R1–R36 and R42, with the paper's human/AI numbers, what to do, and when to skip.
- `references/prose-surface.md`: sentence-level and paragraph-level rules (R37–R41, D1–D10), including the burstiness heuristics and the techniques excluded on purpose.
- `references/claude-delta.md`: Claude-specific fingerprints (C1–C10). Read if you are Claude.
- `references/checklist.md`: the short pre-delivery check.
- `references/sources.md`: papers and caveats.
