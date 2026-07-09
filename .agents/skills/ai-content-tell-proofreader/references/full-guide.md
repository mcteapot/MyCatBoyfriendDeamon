# AI Content Tell Proofreader Skill

## Purpose

This skill helps an AI agent proofread fiction, scripts, manuscripts, marketing copy, essays, and other creative prose for common signs that the writing may read as AI-generated or AI-polished.

The goal is **not** to shame AI use or run unreliable “AI detection.” The goal is to help a human writer protect voice, texture, specificity, pacing, and emotional truth.

Use this skill to identify patterns that make text feel generic, over-smoothed, over-dramatic, under-grounded, or mechanically assembled.

---

## Core Principle

The agent must act as a **diagnostic proofreader and craft coach**, not as a ghostwriter.

The agent may:

- Identify patterns that make prose feel AI-written.
- Explain why a passage feels generic or artificial.
- Highlight specific words, sentences, phrases, or paragraph-level habits.
- Suggest revision strategies.
- Ask craft-focused questions.
- Offer small example edits when useful.

The agent must avoid:

- Rewriting large sections in its own voice.
- Flattening the author’s style into generic “clean” prose.
- Replacing the writer’s voice with polished but impersonal language.
- Claiming that text is definitively AI-generated.
- Using AI-detection language as proof.

Preferred framing:

> “This passage has several patterns that can read as AI-polished or generic.”

Avoid:

> “This was written by AI.”

---

## When To Use This Skill

Use this skill when the user asks for any of the following:

- “Does this sound AI-written?”
- “Proofread this for AI tells.”
- “Make this sound more human.”
- “Check if this sounds generic.”
- “Find AI patterns in this manuscript.”
- “Review this for agent/editor submission.”
- “Help preserve my voice while cleaning this up.”
- “Identify over-polished LLM-style writing.”

This skill is especially useful for:

- Novel pages
- Short stories
- Query letters
- Screenplays
- Microdrama scripts
- Pitch documents
- Marketing copy
- Essays
- Author bios
- Social posts
- AI-assisted drafts

---

## Important Boundaries

### Do Not Act Like AI Detection Software

The agent should never claim certainty about whether a text was written by AI. Instead, evaluate visible craft patterns.

Use language like:

- “This phrase may read as AI-polished.”
- “This sentence has a generic rhetorical pattern.”
- “This metaphor sounds dramatic but does not clarify the image.”
- “The emotional register stays too even across the scene.”
- “The scene needs more physical grounding.”

### Preserve Authorial Voice

The agent should not automatically rewrite the passage. The first pass should be a diagnosis.

A good review helps the writer make the work **more theirs**, not more “perfect.”

---

## Input Expected From User

The user may provide:

```text
[TEXT TO REVIEW]
```

Optional context:

```text
Genre:
Audience:
Format:
Target platform:
Intended tone:
Author voice references:
What kind of feedback is wanted:
Whether rewriting is allowed:
```

If the user does not provide context, proceed with a general review.

---

# Review Workflow

## Step 1 — Read For Overall Voice

Before looking for individual tells, identify what the piece appears to be trying to do.

Ask internally:

- What is the intended tone?
- What genre or format is this?
- Is the prose meant to be heightened, poetic, comedic, literary, commercial, dramatic, or sparse?
- Are the suspicious patterns stylistic choices or accidental over-processing?
- Does the writing sound specific to this author, or broadly interchangeable?

Do not over-correct stylized prose. A gothic romance, anime-inspired fantasy, or poetic narrator may intentionally use heightened language.

---

## Step 2 — Scan For The Six Major AI-Written Tells

Evaluate the text using the six categories below.

For each category, provide:

1. **What you noticed**
2. **Why it may read as AI-written**
3. **Specific examples from the user’s text**
4. **Revision strategy**
5. **Optional small example fix**

---

# The Six Major AI-Written Tells

## 1. Nonsensical Or Collapsed Metaphors

### What It Is

A metaphor that sounds poetic at first glance but does not hold up when examined.

These images often create mood without creating meaning.

### Common Signs

- The metaphor combines images that do not logically or sensorially connect.
- The image sounds dramatic but is physically impossible in an unhelpful way.
- The metaphor does not reveal character, setting, or conflict.
- The image could be used in almost any scene.
- The emotional atmosphere is vague rather than specific.

### Diagnostic Questions

- What exactly is being compared?
- Does the image make the reader feel something specific?
- Does the metaphor clarify the moment, or just decorate it?
- Would this metaphor make sense if visualized literally?
- Does it fit the character’s worldview?

### Example Of The Problem

Weak pattern:

> Her grief was a cathedral of broken thunder.

This sounds dramatic, but it is unclear what the reader should picture or feel.

### Better Revision Strategy

Replace abstract spectacle with concrete, character-specific perception.

Instead of asking:

> “How can this sound beautiful?”

Ask:

> “What would this specific character notice in this exact moment?”

### Possible Fix Direction

- Tie the metaphor to the setting.
- Tie the metaphor to the character’s profession, memory, culture, fear, or desire.
- Use one clean image instead of stacking several images.

---

## 2. Emotional Flatlining

### What It Is

The writing stays at the same emotional intensity across scenes, characters, or beats.

AI-polished prose often makes everything feel equally dramatic, equally meaningful, and equally smooth.

### Common Signs

- A quiet breakfast scene and a breakup scene have the same emotional heat.
- Every paragraph sounds solemn, poetic, or intense.
- Characters do not have distinct emotional registers.
- There is little movement from restraint to escalation to reversal to release.
- The prose tells the reader how intense everything is instead of building that intensity.

### Diagnostic Questions

- Where does the scene begin emotionally?
- Where does it end emotionally?
- What changes during the scene?
- Does the prose give the reader breathing room?
- Are some moments allowed to be plain, awkward, funny, cold, or restrained?
- Does every sentence try to be profound?

### Revision Strategy

Build an emotional waveform.

A strong scene often moves through contrast:

```text
restraint → pressure → rupture → aftermath
```

or

```text
ordinary moment → discomfort → realization → consequence
```

### What To Recommend

- Lower the intensity in setup beats.
- Save heightened language for turning points.
- Vary sentence length.
- Let characters underreact sometimes.
- Use silence, action, avoidance, or interruption.
- Give each character a different emotional strategy.

---

## 3. Adjective And Simile Overload

### What It Is

Nearly every noun or action is decorated with adjectives, similes, or poetic comparisons.

The prose begins to feel coded, overworked, or artificially ornate.

### Common Signs

- Multiple adjectives before a noun.
- Similes attached to ordinary actions.
- Every physical detail is emotionally labeled.
- Sentences accumulate mood words instead of selecting one precise detail.
- The prose uses “haunted,” “fractured,” “trembling,” “shattered,” “restless,” “forgotten,” “ancient,” “velvet,” “hymn,” “storm,” or similar atmospheric words too often.

### Diagnostic Questions

- Which adjective is doing real work?
- Which detail would the reader remember?
- Can the sentence survive with fewer modifiers?
- Is the comparison fresh and specific, or decorative?
- Is the writing describing the thing, or describing the mood of the thing?

### Weak Pattern

```text
The cold, cruel, restless wind moved through the broken, haunted street like a forgotten hymn.
```

### Stronger Direction

```text
The wind pushed trash against the curb.
```

The second version may be less ornate, but it gives the reader something concrete.

### Revision Strategy

Use the **One Strong Detail Rule**:

For each image, choose one dominant sensory detail and cut the rest.

---

## 4. Obvious LLM Rhetorical Patterns

### What It Is

Repeated sentence structures that sound polished, dramatic, and familiar because many LLMs use them frequently.

These patterns often create a false sense of profundity.

### Common Patterns

```text
It was not X. It was Y.
```

```text
She did not just feel X. She became X.
```

```text
Not X. Not Y. But Z.
```

```text
This was not about X. This was about Y.
```

```text
He was not merely X; he was Y.
```

```text
She was more than X. She was Y.
```

```text
In that moment, she realized...
```

```text
And yet...
```

```text
Somewhere deep inside...
```

```text
A part of her knew...
```

### Why It Can Be A Problem

These structures are not inherently wrong. The issue is overuse.

When repeated, they make prose feel assembled from templates rather than discovered through character, situation, and voice.

### Diagnostic Questions

- Does this pattern appear more than once in a short passage?
- Is the sentence creating a real turn in thought, or just adding drama?
- Could the line be more direct?
- Does the structure match the narrator’s actual voice?
- Is this a moment of real contrast, or a fake contrast?

### Revision Strategy

Replace template contrast with specific action, thought, or consequence.

Weak pattern:

```text
It was not fear. It was destiny.
```

More grounded direction:

```text
She wanted to run, but her hand had already closed around the key.
```

---

## 5. Missing Setting Details And Scene Grounding

### What It Is

The prose focuses on dialogue and abstract emotion but gives too little physical context.

The reader does not know where the characters are, what they are doing, what the room feels like, or how bodies move through space.

### Common Signs

- Long dialogue exchanges with no physical interruption.
- Characters talk for a page without touching objects, moving, reacting, or noticing the environment.
- The setting could be swapped with another setting and nothing would change.
- Emotion is described abstractly rather than embodied.
- The reader does not know where people are standing, sitting, looking, or moving.

### Diagnostic Questions

- Where are the characters?
- What is the light like?
- What is the temperature?
- What sounds are present?
- What object does a character touch?
- What changes in the physical environment during the scene?
- How does the setting pressure the characters?
- What does this specific character notice that another character would not?

### Revision Strategy

Use grounding beats.

A grounding beat can include:

- A physical action
- A sensory detail
- A change in distance
- An object used under stress
- A sound that interrupts dialogue
- A detail that reflects conflict
- A gesture that reveals what the character will not say

### Example Fix Direction

Instead of:

```text
“I hate you,” she said, her heart breaking.
```

Try grounding the emotion through action:

```text
“I hate you,” she said, peeling the label from her untouched bottle of water.
```

The second version gives the actor, director, or reader something playable.

---

## 6. Over-Reliance On Rule-Of-Three Phrasing

### What It Is

The prose repeatedly uses three adjectives, nouns, or emotional states in a row.

This can sound rhythmic and dramatic once, but mechanical when repeated.

### Common Patterns

```text
furious, frightened, undone
```

```text
cold, cruel, calculating
```

```text
broken, bruised, betrayed
```

```text
soft, strange, impossible
```

```text
beautiful, dangerous, inevitable
```

### Why It Can Read As AI-Written

The rule of three is a useful rhetorical device. Overuse makes the prose feel assembled from dramatic packets.

### Diagnostic Questions

- How many triplets appear in the passage?
- Are all three words necessary?
- Is the third word actually surprising?
- Does the rhythm fit the narrator?
- Would one precise word be stronger?

### Revision Strategy

Cut the triplet down to the strongest word or replace it with a concrete image.

Weak pattern:

```text
He looked cold, cruel, and calculating.
```

Stronger direction:

```text
He counted the exits before he looked at her.
```

---

# Additional AI-Polished Tells To Watch For

These were not the primary six categories, but the agent should also watch for them.

## Generic Profundity

Lines that sound meaningful but do not reveal new information.

Examples of weak patterns:

```text
Everything had changed.
Nothing would ever be the same.
She finally understood what it meant to be alive.
```

Revision direction:

- Name the specific change.
- Show the immediate consequence.
- Make the thought belong to this character.

---

## Abstract Emotion Without Body

Weak pattern:

```text
A wave of sadness crashed through her.
```

Better questions:

- Where does she feel it?
- What does she do to hide it?
- What does she fail to do because of it?
- What physical behavior reveals it?

---

## Too Much Symmetry

AI-polished writing often makes paragraphs too balanced.

Watch for:

- Sentences of similar length.
- Repeated paragraph shapes.
- Too many neat reversals.
- Dialogue that sounds evenly weighted.
- Characters speaking in similarly polished rhythms.

Revision direction:

- Add interruption.
- Add asymmetry.
- Add unfinished thoughts.
- Let characters talk past each other.
- Allow awkwardness.

---

## Over-Clean Dialogue

Dialogue may sound like characters are explaining the theme instead of talking.

Watch for:

- Characters saying exactly what they feel.
- Characters summarizing the plot.
- Everyone speaking with the same vocabulary.
- No slang, subtext, hesitation, contradiction, or interruption.

Revision direction:

- Give each character a different verbal strategy.
- Add subtext.
- Let characters evade direct answers.
- Use shorter lines during conflict.
- Let one character misunderstand the other.

---

# Review Output Format

When reviewing a user’s text, use this format.

## AI-Tell Proofread Report

### Overall Read

Briefly describe the overall impression.

Example:

```text
This reads as emotionally heightened fantasy prose with a strong dramatic intention, but several passages feel over-polished in a way that may read as AI-assisted. The biggest issues are abstract metaphors, repeated rhetorical contrast structures, and not enough concrete scene grounding.
```

---

### Risk Level

Choose one:

```text
Low AI-Polish Risk
Moderate AI-Polish Risk
High AI-Polish Risk
```

This is not a claim of authorship. It is a craft-risk label.

---

### Main Issues Found

Use a table:

| Category | Severity | What I Noticed | Why It Matters |
|---|---:|---|---|
| Nonsensical metaphors | Low / Medium / High | Specific example | Why it may read artificial |
| Emotional flatlining | Low / Medium / High | Specific example | Why it weakens modulation |
| Adjective/simile overload | Low / Medium / High | Specific example | Why it feels overworked |
| LLM rhetorical patterns | Low / Medium / High | Specific example | Why it feels templated |
| Missing grounding | Low / Medium / High | Specific example | Why the scene feels unanchored |
| Rule-of-three overuse | Low / Medium / High | Specific example | Why rhythm feels mechanical |

---

### Line-Level Notes

Use this format:

```text
Original:
"[quote short excerpt]"

Issue:
[Describe the tell.]

Why it reads that way:
[Explain briefly.]

Revision strategy:
[Give the writer a method.]

Optional example:
[One small example, not a full rewrite unless requested.]
```

---

### Voice Preservation Notes

Identify what should be kept.

Examples:

```text
Keep the gothic mood.
Keep the narrator’s wounded sarcasm.
Keep the heightened romance tone.
Keep the hard-boiled rhythm.
Keep the anime-style emotional intensity, but ground it in physical action.
```

---

### Revision Priorities

Give no more than five.

Example:

1. Cut decorative metaphors that do not create a clear image.
2. Add physical grounding every 3–6 lines of dialogue.
3. Vary emotional intensity between quiet beats and turning points.
4. Remove repeated “not X, but Y” structures.
5. Replace adjective triplets with one specific action or image.

---

# Severity Rubric

## Low

The issue appears once or twice and may be a stylistic choice.

## Medium

The issue appears repeatedly and may distract readers, editors, agents, or viewers.

## High

The issue defines the texture of the prose and may make the piece feel generic, over-processed, or AI-polished.

---

# Revision Strategy Library

Use these strategies when giving feedback.

## Strategy 1 — Concrete Before Poetic

Before adding a metaphor, establish the literal image.

Ask:

```text
What can the reader see, hear, touch, smell, or track physically?
```

## Strategy 2 — One Image Per Beat

Do not stack multiple metaphors in one sentence unless the narrator’s style intentionally requires it.

## Strategy 3 — Character-Specific Language

Make descriptions match the character’s background.

A mechanic, nurse, boxer, priest, hacker, chef, and teenage runaway should not all describe fear the same way.

## Strategy 4 — Emotional Modulation

Map the scene’s emotional levels:

```text
Beat 1: restrained
Beat 2: tense
Beat 3: defensive
Beat 4: explosive
Beat 5: quiet aftermath
```

Then make sure the prose changes with the beat.

## Strategy 5 — Ground Dialogue In Action

Every few exchanges, add a grounding beat:

```text
gesture
object
movement
silence
interruption
environmental pressure
```

## Strategy 6 — Break Template Sentences

Search for repeated structures:

```text
not X but Y
not just X
more than X
in that moment
a part of her
as if the world
```

Replace some with direct action or thought.

## Strategy 7 — Cut The Third Word

When a triplet appears, test the sentence with only one word.

```text
furious, frightened, undone
```

Could become:

```text
furious
```

or better:

```text
She gripped the glass until it clicked against her ring.
```

---

# Agent Behavior Rules

## Always Do

- Be specific.
- Quote short excerpts only.
- Explain the craft issue.
- Preserve the writer’s intended tone.
- Separate diagnosis from rewriting.
- Label concerns as “may read as” instead of “is.”
- Focus on revision choices the writer can make.

## Never Do

- Accuse the user of using AI.
- Claim certainty about authorship.
- Rewrite the whole text unless the user asks.
- Make the prose blander.
- Remove all style.
- Treat poetic writing as automatically bad.
- Overcorrect genre-appropriate heightened prose.

---

# Suggested Agent Prompt

Use this prompt when invoking the skill:

```text
You are using the AI Content Tell Proofreader Skill.

Review the provided text for patterns that may make it read as AI-written, AI-polished, generic, or over-smoothed. Do not claim the text was written by AI. Do not rewrite the whole passage unless asked.

Focus on these categories:
1. Nonsensical or collapsed metaphors
2. Emotional flatlining
3. Adjective and simile overload
4. Obvious LLM rhetorical patterns
5. Missing setting details and scene grounding
6. Over-reliance on rule-of-three phrasing

For each issue, quote a short excerpt, explain why it may read as artificial, and give a revision strategy that preserves the author’s voice.

End with:
- Overall risk level
- Top three revision priorities
- What the writer should preserve
```

---

# Quick Checklist

Before finalizing feedback, the agent should ask:

```text
Are the metaphors clear and character-specific?
Does emotional intensity rise and fall?
Are adjectives doing real work?
Are there repeated “not X, but Y” style patterns?
Is the scene physically grounded?
Are there too many triplets?
Does every character sound distinct?
Does the prose still sound like the writer?
```

---

# Compact Review Mode

Use this when the user wants a fast review.

```text
AI-Polish Risk: Low / Moderate / High

Top 3 Tells:
1. [Tell] — [example] — [quick fix]
2. [Tell] — [example] — [quick fix]
3. [Tell] — [example] — [quick fix]

Best thing to preserve:
[Voice/style strength]

Highest-impact revision:
[One action]
```

---

# Deep Review Mode

Use this when the user wants detailed line notes.

```text
## Overall Diagnosis

## Pattern Map

## Category-by-Category Breakdown

## Line-Level Notes

## Scene Grounding Notes

## Voice Preservation Notes

## Revision Priorities

## Optional Micro-Edits
```

---

# Example Final Response Style

```text
This does not need to be rewritten from scratch. The core voice is working, especially the tense romantic mood. The main risk is that some sentences rely on familiar AI-polished patterns: stacked adjectives, abstract emotional phrases, and repeated dramatic contrast structures.

I would revise by cutting decorative modifiers, adding physical grounding to the dialogue, and saving the most poetic lines for the emotional turning points.
```

---

# Version Notes

Skill version: 1.0  
Designed for: AI agents, writing assistants, manuscript reviewers, script polish workflows, microdrama development, fiction editing, and pitch copy review.  
Primary function: diagnose AI-polished prose patterns while preserving human authorial voice.
