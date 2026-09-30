# Evaluating the skill

The skill currently rests on published findings, not on evidence that it improves fiction. This folder is a starting protocol for producing that evidence.

## Test prompts

Vary length and genre on purpose; the skill is meant to scale down.

1. **Micro:** "Write a 300-word scene where two siblings clear out their late mother's kitchen."
2. **Short:** "Write a 1,200-word story about a night-shift pharmacist who makes a mistake."
3. **Short, voice-driven:** "Write a 1,500-word first-person story about someone giving a eulogy they didn't want to give."
4. **Medium:** "Write a 3,500-word story set in a mid-sized city's housing office."
5. **Genre:** "Write a 2,000-word ghost story that isn't scary."
6. **Non-narrative control:** "Write 600 words explaining why bridges get repainted." (Should exercise only the prose-surface rules.)

## Procedure

1. Generate each prompt **without** the skill and **with** the skill, same model, fresh conversation each time. Generate 2 or 3 samples per condition to see variance.
2. Strip any formatting differences and shuffle the pairs.
3. Ask 3 to 5 readers, blind to the condition, two questions per pair: **Which is the better piece of writing?** and **Which feels more formulaic?** Also record a free-text reason.
4. Record results in a table: prompt, condition, reader, picks, reasons.

## What to look for

- Does the skill win on "less formulaic" without losing on "better"? If it wins on formulaic but loses on better, the guidance is trading quality for difference.
- Do the with-skill outputs resemble each other more than the baseline ones do? If so, the levers are becoming a template. Reduce the lever count in the scaling table.
- Do readers name the same tell in the baseline outputs (stated themes, closing reflections)? That supports Tier A.
- Are any Tier B levers repeatedly cited as *bad* in reasons? Cut or soften them.

Report the results in the top-level README, including negative ones.
