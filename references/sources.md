# Sources

This skill is an independent project. It is **not affiliated with, endorsed by, or reviewed by** the authors of either paper. It encodes one reader's interpretation of their findings as writing guidance.

## Papers

**StoryScope** (narrative structure; drives `levers.md`, parts of `prose-surface.md`, and `claude-delta.md`)
- Russell, Rajendhran, Pham, Iyyer & Wieting. *StoryScope: Investigating idiosyncrasies in AI fiction.*
- arXiv: https://arxiv.org/abs/2604.03136
- The paper has been revised on arXiv more than once. This skill uses only the *direction* of its findings (for example, "AI stories state their themes more than human stories do"), so it doesn't depend on any one version's numbers.

**Odri & Yoon** (perplexity, burstiness, detector unreliability; drives D1-D10)
- Odri & Yoon (2023), a study of detecting AI-generated text in scientific articles and of how detection tools can be evaded. *Orthopaedics & Traumatology: Surgery & Research*, vol. 109, article 103706.
- This paper is about scientific articles and 2023-era tools, not fiction. The mechanisms are borrowed. See D10.

**LAMP artifact taxonomy**
- Chakrabarty et al. (2025), cited via StoryScope for the R40 categories. See StoryScope's reference list for the full citation.

## What this skill does and doesn't claim

- It reproduces **no statistics** from either paper. Earlier drafts included hand-extracted figures, which were removed because they had not been checked against the papers. The advice doesn't depend on them.
- The directions of findings were read from the papers by the skill's author and have not been independently verified. If a rule matters to you, check it against the paper.
- Thresholds in the skill itself (for example, about one em-dash per 1,000 words, or three similar-length sentences in a row) are **heuristics chosen by the skill's author**, not findings from the papers.

## Known limitations

- The guidance describes *differences between AI and human fiction*. It is not evidence that following it makes fiction better. Nobody has shown that yet; see `evals/`.
- StoryScope measured Claude Sonnet 4.6. Newer models may behave differently.
- Some levers (for example, R7 on emotional naming) can read as weaker craft if applied mechanically.
