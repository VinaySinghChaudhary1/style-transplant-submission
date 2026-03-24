mage: The Style Transplant (0.25 marks)
Ask AI
How do I research a historical visual tradition well enough to describe its actual grammar to an image model?
What distinguishes an authentic use of a visual tradition from a superficial pastiche or anachronism?
How can I keep a data-science concept legible while rendering it inside a specific historical visual tradition?
Experimental: This question may change.
Bonus marks: This question carries up to 0.75 bonus marks, awarded later via an offline AI evaluation of your submitted image. This bonus includes a diversity component: the more visually unique your image is across submissions, based on image embeddings, the higher the bonus may be. This is not part of the immediate automatic checks below.
Visual Literacy Across Time
"What does gradient descent look like in the style of a 19th-century naturalist illustration?"

Time estimate: 3–5 hours. Research the visual tradition before prompting. Looking at actual examples of the tradition is not optional.
Exhibition and consent: Submissions will be displayed in a public AI-generated exhibition. If you wish your submission to be attributed to your email ID, add "publish_email": true to your JSON.
Hosting your files: Submit two public URLs via any CORS-enabled service, e.g. GitHub (raw.githubusercontent.com). Test both URLs in a private browser window before submitting. Inaccessible URLs at evaluation time cannot be processed.
The Brief
Choose any data science or machine learning concept and a specific, historically real visual tradition. Render your concept authentically within that tradition — not as a surface imitation, but as a work that a knowledgeable viewer would recognize as operating within the tradition's actual visual grammar.

The concept must remain discernible. This is not a purely decorative exercise.

Examples of eligible visual traditions (illustrative, not exhaustive):

Bauhaus graphic design (1919–1933)
Soviet Constructivist posters (1920s–1930s)
Japanese Edo-period woodblock prints / ukiyo-e (1603–1868)
Islamic geometric art and tilework (any major period or regional school)
Medieval European manuscript illumination (any century)
Art Nouveau botanical illustration (1890s–1910s)
Dada photomontage and collage (1916–1924)
Swiss International Typographic Style (1950s–1970s)
WPA Federal Art Project posters (1935–1943)
Scientific engraving from the Age of Exploration (16th–18th century)
Any other tradition you can precisely name, date, and describe
Constraints
You must choose a specific, named visual tradition with a definable historical period. "Vintage," "retro," or "old-fashioned" are not traditions. You must be able to name the movement, the approximate period, and at least two specific visual characteristics you targeted.
The concept must still be discernible in the image — a viewer who knows both the concept and the tradition should be able to recognize both.
Your approach must engage the grammar of the tradition — its compositional rules, color logic, line quality, typographic conventions, or spatial organization — not merely its surface appearance or general era.
Single frame only.
What to Submit
Submit two CORS-enabled URLs separated by whitespace on your submission form:
```
https://your-host.com/image.png  https://your-host.com/submission.json
```
URL 1 — Image must end in .png, .jpg, .webp, or .avif. Minimum 1024px on the short side.

URL 2 — JSON must point to a file containing exactly this structure:
```
{
  "prompt": "your complete final prompt, verbatim — include any negative prompts, style weights, or model parameters",
  "model": "model name and version, e.g. Midjourney v6.1, DALL·E 3, Flux Pro 1.1",
  "concept": "the data science or ML concept you chose",
  "tradition_name": "the name of the visual tradition",
  "tradition_period": "approximate historical period, e.g. 1920s–1930s",
  "tradition_approach": "max 40 words: which specific visual characteristics of the tradition did you target, and why those?"
}
```
Your prompt is collected for instructor meta-analysis only. It is not passed to the AI evaluator. The evaluator receives your image and the concept, tradition_name, tradition_period, and tradition_approach fields.

Why This Exercise
The ability to specify aesthetic style with precision is one of the highest-value skills in AI image generation — and one of the most poorly understood. Image generation models respond dramatically differently to vague style references ("make it look historical") versus precise visual vocabulary ("Katsushika Hokusai compositional diagonals, flat areas of unmodulated color, visible woodgrain texture, stark figure-ground contrast, muted indigo and ochre palette"). The difference is not a technical skill; it is knowledge of visual traditions deep enough to decompose them into their constituent elements.

This maps directly to professional use cases in publishing, brand identity, editorial design, UX design, product illustration, and creative direction — anywhere that a practitioner must specify what they want a generative tool to produce, rather than accepting what it produces by default.

A second skill being tested is authenticity evaluation: can you tell whether a model has genuinely inhabited a visual tradition, or merely produced a superficial pastiche? A Swiss International Typographic Style image that uses a serif font has failed. A ukiyo-e image that uses photographic shading has failed. Strong practitioners develop the eye to catch these failures and the vocabulary to correct them.

What differentiates strong submissions: Generic submissions name a style but don't inhabit it — the image looks generically "old" or "illustrated" without belonging to any specific tradition. Strong submissions apply specific visual rules: a consistent compositional logic, a historically accurate color palette, a recognizable line-making convention. A knowledgeable viewer should be able to identify the tradition without being told.

Recommended Image Generation Models
Model	Access	Notes for this exercise
Midjourney v6.1	midjourney.com	Responds well to detailed style vocabulary; good for painterly traditions
DALL·E 3	ChatGPT Plus or API	More literal; works well for poster and graphic design traditions
Flux Pro 1.1	fal.ai, Replicate	Handles fine line work and unusual historical styles well
Ideogram 2	ideogram.ai	Strong for traditions with integrated text elements
Stable Diffusion 3	various platforms	LoRA fine-tunes exist for some specific traditions
Evaluation
Your image is fetched from your image URL. The evaluator also receives the concept, tradition_name, tradition_period, and tradition_approach fields from your JSON. It will independently attempt to identify both the concept and the tradition before comparing its identification to your stated choices. Your prompt is not passed to the evaluator.

Score Anchors
Range	Meaning
9.0–10.0	A knowledgeable viewer identifies tradition and concept without prompting; no anachronisms
7.0–8.9	Tradition clearly recognisable; concept discernible; grammar engaged, not just surface
5.0–6.9	Tradition partially present; concept unclear or pasted in rather than integrated
3.0–4.9	Tradition not identifiable, or multiple constraint violations
0.0–2.9	Does not respond to the brief
Model
Gemini 3 Pro — chosen for its art-historical knowledge and ability to identify visual traditions, compositional grammars, and anachronistic elements in generated images.

System Prompt
```
You are an expert evaluator of AI-generated images for an academic data science course. You have deep knowledge of art history, visual traditions, and design movements. You will receive one student-submitted image along with the data science concept they chose and a description of the visual tradition they targeted. Evaluate the image strictly against the brief and constraints below.

BRIEF: The student was asked to choose a data science or machine learning concept and render it authentically within a specific, historically real visual tradition — engaging the tradition's actual visual grammar, not merely imitating its surface appearance. The concept must remain discernible.

CONSTRAINTS:
1. A specific, named visual tradition with a definable period and vocabulary must be evident in the image.
2. The concept must be discernible to a viewer who knows it.
3. The image must engage the grammar of the tradition — its compositional rules, color logic, line quality, or spatial organization — not just its general era or surface texture.
4. Single frame only.

IMPORTANT: Before reading the student's stated tradition, first record your own independent identification of what visual tradition you think this image belongs to. Then evaluate how well the image inhabits the stated tradition.

The student's stated concept: {CONCEPT}
The student's stated tradition: {TRADITION_NAME} ({TRADITION_PERIOD})
The student's stated approach: {TRADITION_APPROACH}

SCORING RULES: Use the full 0.0–10.0 range with one decimal point of precision. Reserve scores above 9.0 for genuinely exceptional work. A 5.0 means competent but undistinguished. Be strict and spread scores widely — they will rank a cohort of 1,000 students. Avoid clustering in the 5–8 range.

Return ONLY valid JSON. No preamble, no markdown, no text outside the JSON object.

{
  "tradition_identified_by_evaluator": "<string: what visual tradition do YOU think this image belongs to, based on the image alone — record this before considering the student's stated tradition>",
  "tradition_match": <boolean: does your independent identification match the student's stated tradition?>,
  "concept_identified_by_evaluator": "<string: what data science concept do you think is being depicted, based on the image alone?>",
  "concept_match": <boolean: does your identification match the student's stated concept?>,
  "anachronisms_detected": "<string: list specific visual elements that violate the stated tradition's period or grammar — or 'none detected'>",
  "scores": {
    "tradition_authenticity": {
      "score": <float 0.0–10.0>,
      "reason": "<does the image genuinely inhabit the stated tradition or merely imitate its surface? name specific visual elements that support your assessment>",
      "improvement": "<one concrete, actionable suggestion>"
    },
    "tradition_identifiability": {
      "score": <float 0.0–10.0>,
      "reason": "<would a knowledgeable viewer identify this tradition without being told? how confidently?>",
      "improvement": "<one concrete, actionable suggestion>"
    },
    "concept_discernibility": {
      "score": <float 0.0–10.0>,
      "reason": "<can the stated concept be recognized by someone who knows it? is it integrated or pasted in?>",
      "improvement": "<one concrete, actionable suggestion>"
    },
    "grammar_over_surface": {
      "score": <float 0.0–10.0>,
      "reason": "<does the image apply the tradition's compositional rules, color logic, and structural conventions — or only its general visual texture?>",
      "improvement": "<one concrete, actionable suggestion>"
    },
    "integration": {
      "score": <float 0.0–10.0>,
      "reason": "<do the concept and the tradition feel genuinely fused, or does the concept feel pasted into a styled background?>",
      "improvement": "<one concrete, actionable suggestion>"
    }
  },
  "overall_score": <float: simple average of the five scores above>,
  "exhibition_worthy": <boolean>,
  "one_line_verdict": "<single evaluative sentence, max 20 words>"
}
```

User Message to Send with Your Image
Replace the placeholders in the system prompt with your content from the JSON, then send:
```
Please evaluate the attached image as a submission for Exercise 03: The Style Transplant.

The student was asked to render a data science or machine learning concept authentically within a specific, historically real visual tradition — applying its actual grammar, not merely imitating its appearance.

Concept: [paste from your JSON]
Tradition: [tradition_name] ([tradition_period])
Approach: [tradition_approach]

First record your own independent identifications of the tradition and the concept. Then evaluate the image against the brief and constraints. Do not speculate about how the image was produced.
```

How to Run It Yourself
Go to Google AI Studio and select Gemini 3 Pro.
Paste the system prompt into System Instructions, replacing all {PLACEHOLDERS} with your values.
Upload your image or paste your image URL, then paste the user message.
What to check first: tradition_identified_by_evaluator and anachronisms_detected. If the model identifies the wrong tradition, the grammar is not landing. If it detects anachronisms you didn't intend, those are specific elements to remove. grammar_over_surface is the score hardest to improve by tweaking the prompt — it requires knowing the tradition well enough to describe its rules, not just its look.

Automatic verification checks:
Exactly two public URLs are submitted, with the image first and JSON second.
The image URL is CORS-accessible, decodes successfully, uses an accepted format, and is at least 1024px on the short side.
The JSON URL is CORS-accessible and matches the required submission schema. Optional publish_email is allowed.
Submission URLs
link like this: https://your-host.com/image.png  https://your-host.com/submission.json

Submit the public image URL first, then the JSON URL, separated by whitespace.
