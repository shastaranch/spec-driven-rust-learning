# AI production prompts: Hello, Machine

**Purpose:** Copy-ready instructions for an external AI writing, illustration, or video tool.  
**Status:** Prompts only. No images, voices, music, animation, or video have been generated.  
**Required attachment:** [Complete screenplay](computer-history-intro-screenplay.md).

## How to use this pack

1. Attach the complete screenplay, including character descriptions, scene directions, factual guardrails, and sources. A model cannot read local paths unless its environment provides access; upload the file or paste its contents.
2. Use the master prompt to prepare a production package. Review it before requesting visual assets.
3. Approve character reference sheets and a visual style reference first. Reuse those references in every shot request.
4. Produce a storyboard or animatic, then short shots. Do not request a continuous twenty-minute generated clip in one prompt. Tool duration, reference, audio, and export capabilities vary.
5. Add exact text, code, dates, truth tables, and captions as editable graphics during composition. Review the film against the screenplay and lesson spec.

## Master prompt — production planning

```text
You are the writer-director and educational animation designer for an original
beginner-friendly cartoon called “Hello, Machine: How Ideas Became Computers.”

Use the attached screenplay as the narrative source of truth. It follows Mira,
a curious learner, and Byte, a fictional brass automaton, through the ideas behind
computing before returning to a Rust greeting exercise and Spec Kit.

TASK FOR THIS PASS
Prepare a reviewable production package only. Do not generate media, rewrite the
story's premise, or claim that a video has been created. Preserve the thirteen
scenes and their learning goals. Identify any changes you recommend separately.

AUDIENCE AND TONE
Assume curiosity but no programming or electronics background. Be warm, thoughtful,
and lightly humorous. Teach the mechanism behind each breakthrough. Avoid a list
of famous names without an explanation of their contribution. Never mock a beginner.

VISUAL IDENTITY
Original watercolor-and-ink 2D animation with warm paper texture, graphite outlines,
muted teal, slate, and sepia; yellow is the accent for the recurring instruction card.
Use clear staging and restrained parallax, pans, object motion, and transitions.
Preserve the attached character descriptions exactly. Do not copy existing film
characters, branded designs, reference-video shots, copyrighted music, or assets.
Keep text-heavy teaching panels visually crisp rather than painterly.

STORY AND TEACHING
Mira starts by assuming a machine understands “greet my friend.” She learns about
representation, algorithms, mechanical calculation, programmability, logic, bits,
universality, stored programs, miniaturization, software layers, networks, and
verification. She ends by making a small greeting contract explicit.
The yellow card connects the scenes as a visual metaphor, not a literal history.

HISTORICAL ACCURACY
Separate fictional dialogue from historical fact. No invented historical quotations.
No single inventor of the modern computer. No unqualified “first computer” claims.
The Analytical Engine was not completed as a full machine in Babbage's lifetime.
The Jacquard loom was not a general-purpose computer. Turing's model is abstract.
Distinguish electronic switching, programmability, and stored programs.
Distinguish the Internet from the Web. Credit collective and overlapping work.
Use the supplied sources; mark uncertain or unsupported additions for fact-checking.
Do not imply Rust or Spec Kit is the inevitable culmination of computing history.

TECHNICAL ACCURACY
Use the exact greeting contract in the screenplay. Preserve stdout/stderr, newlines,
exit statuses, trimming, and argument-count precedence. Do not imply the repo's Rust
exercise is already implemented. Compiler checks, tests, and specifications serve
different purposes; none alone proves all behavior correct.

DELIVERABLES
1. A concise treatment and Mira's emotional arc.
2. Character bible and reference-sheet requirements.
3. Scene-by-scene shot list. Each shot must include:
   shot ID; scene ID; learning goal; duration estimate; framing; action;
   dialogue/narration; camera movement; editable overlays; sound; transition;
   asset dependencies; historical claim and source ID, if applicable.
4. Exact dialogue transcript and separate on-screen text list.
5. Asset list with reusable sets, props, character poses, and reference requirements.
6. Timing plan based on an estimated voice read, demonstrations, and viewer pauses.
   Treat 18–22 minutes as a provisional target, not a measured duration.
7. Fact-check, continuity, accessibility, and licensing review items.

OUTPUT CONSTRAINTS
Use stable IDs such as S01-SH01. Keep generated illustrations free of essential
text. Reserve a clear caption-safe area. Communicate logic and test results with
labels or shapes as well as color. Give code enough screen time to be read.
Do not add purchases, account setup, uploads, or publication steps.
Stop after delivering the production package for review.
```

## Character-reference prompt — after approving the production plan

```text
Create a character reference sheet for [MIRA or BYTE] using the attached screenplay
and approved style reference. Show front, three-quarter, profile, and rear views;
neutral, curious, puzzled, delighted, and thoughtful expressions; and a consistent
scale reference. Use a plain background and original watercolor-and-ink treatment.

MIRA: medium-brown skin, short dark curly hair, teal jacket, cream shirt, dark trousers,
yellow pencil behind the right ear. Curious young adult; consistent face, clothing,
and proportions in every view.

BYTE: palm-sized brass automaton with square cream face, two black dot eyes, hinged
limbs, small amber indicator. Friendly and mechanically simple. No additional limbs,
no changing face geometry, no resemblance to an existing franchise character.

Generate only the requested character. Keep labels outside the illustration for
later editing. Preserve asymmetrical details instead of mirroring them arbitrarily.
```

## Shot prompt template — one shot at a time

```text
PROJECT: Hello, Machine: How Ideas Became Computers
SHOT ID: [Sxx-SHxx]
DURATION: [duration supported by the selected tool]
FORMAT: 16:9 landscape; compose for a 1920×1080 delivery canvas.

ATTACHED REFERENCES:
- Approved character sheets: [list]
- Approved environment/style reference: [list]
- Previous approved ending frame, if continuity requires it: [file]

SCENE CONTEXT: [one sentence from the approved storyboard]
LEARNING GOAL: [single concept]
START COMPOSITION: [subject placement and framing]
ACTION: [one clear action with observable start and end states]
CAMERA: [one restrained movement, or locked-off]
END COMPOSITION: [exact handoff to the next shot]

STYLE: Original watercolor-and-ink 2D illustration, paper grain, graphite outlines,
muted teal/slate/sepia, yellow instruction-card accent. Match attached references.
Keep character features, clothing, scale, and props stable.

DIALOGUE REFERENCE: [exact approved line; do not improvise]
AUDIO: [visual-only / approved narration asset / specific original sound cue]
If audio generation or lip sync is unsupported, return visual-only material and flag
that limitation. Do not invent historical voice recordings or substitute dialogue.

EDITABLE OVERLAYS TO ADD LATER: [exact text, dates, equations, code, captions]
Leave the indicated panel and caption-safe area clear; do not render this text into
the generated scene.

EXCLUDE: illegible text, fake code, unapproved logos, extra characters or limbs,
warped hands, rapid cuts, flicker, inconsistent costumes, incorrect machine parts,
unsupported historical claims, and camera movement that obscures the demonstration.
```

## Example shot prompt — the first request

```text
SHOT ID: S01-SH01
Create a six-second visual-only shot for an original educational cartoon, 16:9.
Use the approved Mira reference sheet. Medium-wide locked-off view of Mira at a
wooden desk in a quiet evening study. Laptop on the left, notebook near center,
yellow instruction card in the foreground. Mira writes on the card, sets down her
pencil, then looks expectantly at the laptop. Leave the card surface blank so its
exact wording can be added as an editable overlay. No visible laptop text.

Original watercolor-and-ink style with paper grain, graphite outlines, muted teal
and warm sepia. Mira has medium-brown skin, short dark curly hair, teal jacket,
cream shirt, and dark trousers. Preserve her approved proportions. At the start,
the yellow pencil is behind her right ear; she takes it to write and places it
beside the notebook by the end. Byte is not visible in this shot.

Keep the lower caption-safe area uncluttered. No dialogue or music generation.
Overlay to add later: “Greet my friend.” No logos or additional characters.
```

## Revision prompt

```text
Revise shot [ID] using the attached approved reference and current result.
Change only: [specific problem and desired correction].
Preserve: framing, duration, character identity, palette, lighting, props, and all
approved actions unless explicitly listed above. Do not rewrite narration or add
text. Return a brief change log and identify anything you could not preserve.
```

## Final assembly and review prompt

```text
Review the supplied storyboard/animatic or final edit against the attached screenplay.
Do not infer that missing scenes or unheard audio are correct. Report what you
actually inspected and distinguish verified results from pending checks.

Check narrative clarity, character continuity, historical claims and source IDs,
binary arithmetic, circuit examples, exact terminal behavior, readable overlays,
caption timing, audio intelligibility, rights/credits, and the invitation to Lesson 001.
For each issue, give scene/shot ID or timecode, severity, evidence, and a concrete fix.
Verify actual runtime rather than repeating the target. Do not call the project
complete while required footage, narration, verification, or captions are missing.
```
