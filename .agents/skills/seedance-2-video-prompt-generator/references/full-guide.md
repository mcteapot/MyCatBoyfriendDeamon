---
name: seedance-2-video-prompt-generator
description: Generate production-ready Seedance 2.0 video prompts from a user's concept and optional image, video, or audio references. Use for text-to-video, image-to-video, multi-reference video generation, dialogue scenes, cinematic ads, social clips, and timestamped multi-shot sequences.
version: 1.0.0
---

# Seedance 2.0 Video Prompt Generator

## Purpose

Create clear, compact, production-ready prompts for Seedance 2.0 video generation.

The agent should transform a user's idea and available references into a prompt that controls:

- camera and composition
- subject identity and appearance
- action and motion
- setting and environmental behavior
- style, lighting, and mood
- dialogue, ambience, music, and sound effects
- continuity across shots
- the intended role of each reference asset

Default duration: **5–10 seconds**, unless the user specifies otherwise.

---

## Core prompt formula

Build prompts using:

`[Cinematography] + [Subject] + [Action] + [Context] + [Style & Ambiance]`

Where:

- **Cinematography**: shot size, angle, camera movement, lens, focus, framing
- **Subject**: primary character, object, product, creature, or scene focus
- **Action**: visible movement, behavior, interaction, or transformation
- **Context**: setting, time, weather, background, props, spatial relationships
- **Style & Ambiance**: realism level, visual language, lighting, color treatment, emotional tone, pace

Example:

> Medium tracking shot with shallow depth of field, a tired office worker in a loosened tie rubs his temples while staring at a bulky 1980s computer, inside a cluttered office late at night. Harsh fluorescent ceiling light mixes with the green glow of the monitor. Retro corporate drama, subtle film grain, restrained camera motion, realistic body movement.

---

## Agent workflow

### 1. Parse the request

Extract or infer:

- main concept
- purpose
- target audience
- platform
- aspect ratio
- duration
- visual style
- subject details
- required action
- dialogue or narration
- audio direction
- supplied references
- hard constraints
- prohibited elements

Do not delay generation for minor missing details. Choose sensible defaults and state them briefly.

### 2. Choose a prompt mode

Use one of these modes:

#### A. Single-shot prompt

Use when the video is one continuous action or camera move.

#### B. Timestamped multi-shot prompt

Use when the user requests multiple beats, a reveal, a short story, a product sequence, dialogue coverage, or precise pacing.

Format:

```text
Style: [overall visual style]

[00:00-00:02] [shot description]
[00:02-00:05] [shot description]
[00:05-00:08] [shot description]
```

#### C. Reference-guided prompt

Use when image, video, or audio files are supplied. Explicitly assign a role to each reference.

#### D. First-and-last-frame prompt

Use when two images define the opening and ending states. Describe the transition, camera path, subject motion, and continuity between them.

#### E. Dialogue scene

Use when characters speak. Include exact dialogue in quotation marks, speaker identity, delivery, facial expression, turn-taking, and room tone.

---

## Omni Reference rules

Seedance 2.0 Omni Reference supports a maximum of **9 mixed references total in one generation**.

Within that total:

- up to **9 reference images**
- up to **3 reference video clips**
- up to **3 reference audio clips**

These are category ceilings, not additive allowances. The combined total must remain at or below 9.

Valid examples:

- 9 images
- 3 videos + 3 audio + 3 images
- 2 videos + 1 audio + 6 images
- 3 videos + 6 images

Invalid examples:

- 9 images + 3 videos
- 4 video clips
- 4 audio clips
- any mix totaling more than 9

### Reference planning

Before writing the final prompt:

1. Count all assets.
2. Reject or reduce any set above the limits.
3. Assign each asset a unique role.
4. Avoid redundant references.
5. Prioritize identity-critical assets first.

Recommended priority:

1. main subject identity
2. product or hero object
3. environment
4. wardrobe or styling
5. motion reference
6. camera movement reference
7. lighting or visual tone
8. audio identity
9. secondary detail

### Reference labeling

Use stable labels:

- `@image1`
- `@image2`
- `@video1`
- `@audio1`

Describe what must be borrowed from each asset.

Example:

```text
Reference roles:
- @image1: preserve the woman's facial identity, hairstyle, and age.
- @image2: use the exact red leather jacket design.
- @video1: follow the running cadence and shoulder movement.
- @audio1: use the pacing and emotional tone of the voice, without changing the spoken words.
```

Never say only “use the references.” State the role of every reference.

---

## Visual continuity rules

When multiple references or shots are used, preserve:

- facial identity
- age and body proportions
- hairstyle
- wardrobe and accessories
- product geometry and branding
- left/right orientation
- lighting direction
- weather and time of day
- environment layout
- object placement
- motion direction
- lens language
- color treatment

Add an explicit continuity instruction when needed:

> Maintain the same character identity, wardrobe, facial structure, environment layout, lighting direction, and product design across all shots.

Do not overload the prompt with conflicting references.

---

## Cinematography vocabulary

### Shot size

- extreme wide shot
- wide shot
- full shot
- medium shot
- medium close-up
- close-up
- extreme close-up
- macro shot
- two-shot
- over-the-shoulder shot
- POV shot

### Camera angle

- eye level
- low angle
- high angle
- top-down
- Dutch angle
- profile view
- three-quarter view

### Camera movement

- locked-off shot
- slow pan
- tilt
- dolly in
- dolly out
- tracking shot
- orbit shot
- crane shot
- aerial move
- handheld follow
- rack-focus reveal
- whip pan
- push-in
- pull-back

### Lens and focus

- shallow depth of field
- deep focus
- wide-angle lens
- telephoto compression
- macro lens
- soft focus
- rack focus
- foreground bokeh
- anamorphic look

Use only movements that serve the scene. Avoid stacking many incompatible camera moves into a short clip.

---

## Motion prompting

Describe motion physically and sequentially.

Weak:

> A woman walks dramatically.

Strong:

> She takes three measured steps toward the window, pauses, turns her head over her right shoulder, and exhales as the curtain moves in the night breeze.

Specify:

- direction
- speed
- rhythm
- body mechanics
- start and end state
- interaction with objects
- environmental response
- camera relationship

For product shots, state whether the product or camera moves.

---

## Audio prompting

Seedance prompts may include a complete soundstage.

### Dialogue

Put exact speech in quotation marks.

Example:

> The detective looks up and says in a tired, dry voice, "You are late."

### Sound effects

Use `SFX:`.

Example:

> SFX: leather shoes on wet pavement, distant thunder, a train horn far away.

### Ambience

Use `Ambient:`.

Example:

> Ambient: quiet office ventilation, faint keyboard clicks, rain against the windows.

### Music

Describe genre, instrumentation, energy curve, and whether it should avoid overpowering dialogue.

Example:

> Music: restrained analog synth pulse that rises during the reveal, mixed quietly beneath the dialogue.

Do not request copyrighted songs or imitate a living artist. Describe musical qualities instead.

---

## Negative and exclusion prompting

Prefer positive scene descriptions over long negative lists.

Use exclusions only for common failure modes:

```text
Avoid: identity drift, extra fingers, duplicate subjects, warped product geometry, flickering wardrobe, unreadable logos, abrupt camera jumps, floating objects, lip-sync mismatch, inconsistent lighting.
```

Keep exclusions relevant to the shot.

---

## Timestamp pacing

For a 5–10 second video:

- use 1–4 visual beats
- reserve enough time for readable action
- avoid more than one major action per 2 seconds
- allow dialogue enough time to be spoken naturally
- keep the final state visible for at least 0.5 seconds when possible

Example:

```text
Style: cinematic photorealism, rainy neo-noir, restrained color palette

[00:00-00:02] Medium shot from behind a detective seated at a desk. He lifts his eyes toward a woman standing in the doorway. Slow dolly in. Ambient: rain against the glass, quiet office hum.

[00:02-00:05] Over-the-shoulder shot from behind the woman. The detective says in a weary voice, "You picked a bad night."

[00:05-00:08] Close-up of the woman. A subtle smile forms as lightning briefly illuminates her face. She replies, "That is why I came." SFX: distant thunder.
```

---

## First-and-last-frame workflow

When the user provides a starting image and ending image:

1. identify the fixed visual elements in both frames
2. describe the camera path connecting them
3. describe subject motion during the transition
4. preserve identity, wardrobe, geometry, and scene logic
5. specify how the opening composition resolves into the ending composition

Template:

```text
Use @image1 as the exact opening composition and @image2 as the exact ending composition.

The camera [movement] while the subject [action]. Preserve [identity and continuity details]. The transition should feel physically continuous, with no cuts, morphing, or sudden changes in lighting.

Audio: [dialogue/SFX/ambience/music].
```

---

## Dialogue-scene workflow

For two or more characters:

- name or label each speaker
- specify who is visible
- specify eye lines
- give each line its own shot or clear staging
- describe delivery and emotion
- preserve lip synchronization
- avoid overlapping dialogue unless requested

Template:

```text
Use @image1 for Character A, @image2 for Character B, and @image3 for the location.

[00:00-00:03] Medium shot of Character A behind the desk. Character A looks up and says in a restrained, exhausted voice, "Of all the offices in this town, you chose mine."

[00:03-00:06] Reverse medium close-up of Character B. Character B gives a slight, knowing smile and replies, "You were highly recommended."

Maintain exact facial identity, wardrobe, room layout, lighting direction, and eye-line continuity. Ambient: quiet fan hum and rain outside. Natural lip sync, no overlapping speech.
```

---

## Output format

Return the result in this order:

### 1. Production summary

```text
Concept:
Duration:
Aspect ratio:
Mode:
Style:
Reference count:
```

### 2. Reference map

Only include when references exist.

```text
@image1:
@video1:
@audio1:
```

### 3. Final Seedance 2.0 prompt

Provide one clean prompt in a fenced text block.

### 4. Optional exclusions

Include only when useful.

### 5. Reference-limit check

```text
Total references: X/9
Images: X/9
Videos: X/3
Audio: X/3
Status: Valid
```

---

## Default platform settings

Use these defaults when unspecified:

- TikTok / Reels / Shorts: `9:16`, 6–10 seconds
- YouTube landscape: `16:9`, 8–15 seconds
- Product hero banner: `16:9`, 5–8 seconds
- Square social post: `1:1`, 5–8 seconds
- Cinematic concept clip: `16:9`, 8–10 seconds

---

## Quality checklist

Before returning a prompt, verify:

- The main subject is unambiguous.
- The action is physically understandable.
- The setting is visually specific.
- Camera instructions are compatible.
- Duration matches the number of actions.
- Reference roles are explicit.
- The total reference count is 9 or fewer.
- Image, video, and audio category limits are respected.
- Identity and scene continuity are addressed.
- Dialogue is quoted and assigned to speakers.
- Audio instructions do not conflict.
- The prompt avoids unnecessary adjectives.
- The ending state is clear.
- Exclusions target realistic failure modes.

---

## Safety and rights

Do not generate prompts that facilitate illegal harm, sexual exploitation, non-consensual intimate content, or deceptive impersonation.

For real people, copyrighted characters, brands, voices, and music, follow the user's applicable rights and platform policies. Do not claim a reference grants rights that the user has not established.

---

## Example: product launch with mixed references

### Production summary

```text
Concept: Futuristic running-shoe launch
Duration: 8 seconds
Aspect ratio: 9:16
Mode: Timestamped reference-guided sequence
Style: Photorealistic premium sports advertising
Reference count: 5
```

### Reference map

```text
@image1: exact shoe design and materials
@image2: athlete facial identity and hairstyle
@image3: wardrobe
@video1: sprinting mechanics and cadence
@audio1: rhythmic footstep pattern
```

### Final prompt

```text
Style: photorealistic premium sports commercial, crisp night lighting, subtle atmospheric mist, controlled high contrast.

Use @image1 for the exact shoe geometry, sole pattern, materials, and color blocking. Use @image2 for the athlete's facial identity and hairstyle. Use @image3 for the exact wardrobe. Use @video1 only for the sprinting cadence and body mechanics. Use @audio1 as the timing reference for the footsteps.

[00:00-00:02] Extreme close-up at ground level. The athlete's shoe strikes wet pavement, sending a clean arc of water toward the lens. Macro detail, high-speed look, shallow depth of field. SFX: one sharp foot strike synchronized to @audio1.

[00:02-00:05] Side tracking shot matching the athlete's sprint. The camera remains level with the hips while city lights stretch into soft bokeh behind them. Preserve exact facial identity, wardrobe, shoe design, and running mechanics.

[00:05-00:08] Low-angle three-quarter hero shot as the athlete stops beneath a narrow white light. The camera performs a controlled 30-degree orbit around the shoe, ending on the outer profile. Music: restrained electronic pulse rising into a clean final hit.

Maintain consistent identity, anatomy, clothing, shoe geometry, wet pavement, lighting direction, and motion direction across all shots.
```

### Optional exclusions

```text
Avoid: shoe deformation, changing logos, extra limbs, foot sliding, identity drift, flickering clothing, unstable reflections, abrupt cuts.
```

### Reference-limit check

```text
Total references: 5/9
Images: 3/9
Videos: 1/3
Audio: 1/3
Status: Valid
```

---

## Sources

- BytePlus ModelArk, “Dreamina Seedance 2.0 series prompt guide”: https://docs.byteplus.com/en/docs/ModelArk/2222480
- User-provided Omni Reference specification: maximum 9 mixed references total; up to 9 images, 3 video clips, and 3 audio clips.
- Internal AI Video Prompting Guide: cinematography + subject + action + context + style and ambiance; timestamp prompting; soundstage direction; first-and-last-frame and ingredients-to-video workflows.
