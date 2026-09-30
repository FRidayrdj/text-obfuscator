# text-obfuscator

A skill that helps AI models write fiction with less of the structural sameness that makes AI-generated stories easy to spot: stated morals, tidy causal chains, emotions staged through the body, closing reflections, flat escalation, uniform rhythm.

It is a **craft tool**, not a detector-evasion tool. It says so in the skill itself, and it explicitly rules out score-chasing, homoglyphs, and planted errors.

## Why

Most "avoid AI-isms" lists are word blacklists. Recent research suggests the bigger difference is in narrative structure: in StoryScope, structure alone separated AI from human fiction far better than style did, and cleaning up prose barely moved the result. This skill turns those measured differences into planning-stage habits instead of a list of banned words. (Word and construction bans are included too, for the sentence layer.)

## Layout

```
text-obfuscator/
├── SKILL.md                 core: principles, workflow, Tier A habits, Tier B levers, scaling
├── references/
│   ├── levers.md            R1–R36, R42: evidence, per-piece guidance, when to skip
│   ├── prose-surface.md     R37–R41, D1–D10: sentence-level rules, excluded techniques
│   ├── claude-delta.md      C1–C10: Claude-specific fingerprints (loaded only by Claude)
│   ├── checklist.md         short pre-delivery check
│   └── sources.md           papers and caveats
└── evals/README.md          before/after test protocol
```

## Design choices

- **Two tiers, not 43 hard rules.** Tier A is habits to drop on every piece. Tier B is levers to pick from, a few per piece. Mandating every feature in every story would just create a new template.
- **Per-piece rules, not quotas.** The paper's findings are about populations ("human stories do X more often than AI stories"). A model writing one piece can't satisfy a rate, so each is rewritten as a decision about *this* piece.
- **Scaling.** Short pieces get Tier A plus one or two levers. Subplots, multiple locations, and time-jumping are for longer work.
- **Human-typical is not the same as good.** The skill says so directly and lets the user's brief and the story's needs override any rule.
- **One core plus a delta.** The Claude-specific material is a separate reference file. The Claude file cites core rule IDs rather than repeating them.

## Install

- **Claude.ai:** zip the `text-obfuscator` folder (the folder itself should be the zip's root) and upload it as a custom skill. Code execution and file creation must be enabled for Skills to appear; the menu location has moved between UI versions, so follow Anthropic's [Using Skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude) guide.
- **Claude Code:** copy the folder into `~/.claude/skills/` (personal) or `.claude/skills/` (project).
- **Other models:** use `SKILL.md` plus `levers.md`, `prose-surface.md` and `checklist.md` as a system prompt or project instructions; skip `claude-delta.md` (and `sources.md`, which is for humans).

## Status and limitations

- **Evidence.** The guidance rests on published findings about how AI and human fiction *differ*. No one has shown that following it makes fiction *better*. See `evals/README.md` for a protocol; results will be added here. 
- **No statistics.** The skill states the *direction* of each finding and deliberately leaves out the paper's figures, which were not re-checked. The guidance doesn't depend on them. See `references/sources.md`.
- **Second paper.** Odri & Yoon (2023) concerns scientific articles and 2023-era tools. Its mechanisms (perplexity, burstiness) are borrowed, not proven for fiction.
- **Model drift.** StoryScope measured Claude Sonnet 4.6. Newer models may differ.

## Sources

- Russell, Rajendhran, Pham, Iyyer & Wieting. *StoryScope: Investigating idiosyncrasies in AI fiction.* arXiv 2604.03136.
- Odri & Yoon (2023), on detecting AI-generated text in scientific articles. *Orthopaedics & Traumatology: Surgery & Research* 109, 103706.

This project is independent and is not affiliated with or endorsed by the authors of either paper.

## License

MIT License. See [LICENSE](LICENSE).
