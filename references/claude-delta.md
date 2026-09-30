# Claude-specific delta (C1–C10)

Read this if you are Claude. It applies on top of the core skill (SKILL.md, `levers.md`, `prose-surface.md`). Rule IDs R1–R43 and D1–D10 refer to those files. Nothing here overrides them; where this file adds pressure, it says so.

## What the paper found about Claude

StoryScope measured **Claude Sonnet 4.6** specifically. Among the AI models studied, Claude showed a distinctive narrative profile. The paper characterizes it as restrained, consistent, careful, and tonally controlled. This file gives the direction of each finding and leaves out the statistics, which were not re-checked against the paper (see `sources.md`).

The findings are family-level tendencies. The newer models that use this skill were not the ones measured, so treat this file as a guide to Claude's *likely* defaults, and trust your own read of a draft over any single statistic.

## How these differ from the core

The core skill mostly says *stop doing what all AI models do*. This file covers what Claude does **more than other AI models**. Those are the habits to check hardest, and they cluster around competence: coherence, control, and tidiness.

Each item below is a counter-default. None is a quota. Apply the ones that fit the piece, and skip any that would hurt it.

## The fingerprints

**C1 — Flat escalation** (a key Claude fingerprint).
The paper's finding: event intensity escalates less than in any other source. Claude's defining flaw here is flatness. Don't smooth the curve. Let stakes move unevenly: a quiet stretch, a sharp jump, a plateau, another jump. In pieces with room, let one event be larger, more sudden, or more destructive than the gradient before it has earned. (See R42.)

**C2 — Narrow event types.**
Claude builds stories from a small set of beat types: conversation, realization, quiet observation, gentle reversal. Vary the types. In a medium piece, aim for a physical event, a social or institutional event, an accident, and an act of speech that *does* something (a threat, a refusal, a lie that lands) rather than merely reveals something. In short pieces, two distinct types are enough.

**C3 — Epilogues and terminal flash-forwards.**
The paper: Claude favors epilogues. Don't end with a coda, a years-later paragraph, or a what-became-of-them summary. End inside the last scene, mid-consequence. This is about the *final* time-jump only. A flash-forward earlier in the piece is a legitimate lever (R24), because it withholds rather than settles.

**C4 — Dreams and unreality.**
Claude avoids dream sequences and unmarked unreality more than other models do. This is an *available* lever, not a requirement. Where the premise supports it, consider a dream, vision, hallucination, or unflagged unreality, presented without telling the reader it's unreal. Don't add one to every story; a mandatory dream is a new template, and it is also GPT's habit (see C10), so treat it as an occasional option, not a fix.

**C5 — The uncanny register.**
Claude over-reaches for the uncanny and the quietly haunted: hush, wrongness, things not quite right. Don't default to it. Let settings be banal, bureaucratic, cheerful, ugly, boring, or plainly pleasant, and let the strangeness come from events.

**C6 — Reverence toward literary tradition** (more often than other sources).
Claude honors and extends storytelling conventions. Consider subverting one on purpose: refuse the resolution the shape promises, abandon a structure partway, let the story fail at being the kind of story it appeared to be. Only when the premise gains from it.

**C7 — Quiet endings.**
The paper characterizes Claude's stories as careful and consistent, favoring quiet endings. Don't default to the settling close or the last soft image. Choose the ending's tempo on purpose. Consider one that arrives too fast, too loud, or interrupted (mid-sentence, mid-fight, mid-phone-call). (Reinforces R6.)

**C8 — Uniform narrative voice.**
Claude's narrative voice tends to be more uniform than other sources'. R41 applies with extra weight: let register shift, and make speakers distinguishable in vocabulary, sentence length, and grammar. Consider one passage in a voice that doesn't match the rest, if the piece can carry it.

**C9 — Restraint as the signature.**
Restraint, consistency, care, and tonal control are Claude's fingerprint. Don't sand every passage to the same level of control. A section can be rawer, more overheated, or less well-behaved than the rest, when the moment calls for it.
Craft caveat: the point is to notice the reflex, not to be sloppy on purpose. Uneven by choice is craft; unpolished by accident is not.

**C10 — Don't import another model's fingerprint.**
Fixing C1–C9 must not mean adopting another AI model's tics: gossip and rumor as plot mechanism, distant-retrospective framing, or a habit of dream sequences (GPT; the StoryScope abstract says GPT over-indexes on dreams); the tidiest endings, extended denouements, or bleak oppressive settings (Gemini); front-loaded crucial context (DeepSeek); in-action character introduction with no explicit trait labels used as a formula (Kimi). In the paper's analysis, the AI models occupy one shared region of narrative space, with human stories sitting further from them than they sit from one another. Moving toward another model is lateral motion inside the same region. The goal is to leave it.
Overlap with R20: introducing characters through action is not wrong. Doing it the same way every time is the fingerprint. Lead with dialogue or another character's report (R20) and vary the method between pieces.

## Working habits for capable models

These are engineering judgment, not paper findings.

- **Decide structural choices before drafting.** A model that plans well tends to produce coherence by default, and coherence is exactly what several of the fingerprints above are made of. Before writing, decide where the causal chain bends (R14), which thread stays unresolved, where an uneven jump lands (C1), and how the piece ends (C3, C7).
- **Resist smoothing in the final pass.** Revision is where the tidy instinct reasserts itself: fixing the unresolved thread, softening the loud event, reconciling the voice shift, evening out a jagged run of sentence lengths (D2). If a rough edge was chosen, leave it. Revise structurally, not by rephrasing (D6).
- **For short outputs, do less, but do it.** Brevity is not an exemption from the Tier A habits. The cheapest structural moves at short length are: open in dialogue (R20), name an emotion plainly (R7), leave one thread unresolved (R14), end on a concrete detail rather than a reflection (R6), and vary sentence length (D2). Don't let a short piece collapse into a single tidy track.
- **Check length against the target.** In the paper, Claude models tended to overshoot requested lengths. Verify before delivering (R43), with a code tool if available; trim rather than extend.
