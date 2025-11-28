This document outlines the plan for creating a playable AI education game for the Vibe-athon.

IMPORTANT:
It all needs to be ONE html file.

1. Playable AI Education Game
Create a small, top‑down 2D game inspired by Stardew Valley’s perspective, but limited to a single village map with a few key locations (start area, quiz gate, blocked bridge, goal area). The player’s goal is to cross a series of obstacles (e.g. gates, locked paths, moving hazards) by “using AI” in the right way.​

The game teaches how AI works by turning core LLM concepts into mechanics:

The player answers short multiple‑choice quizzes about AI basics (prompts, tokens, hallucinations, limitations).

Correct answers reward “AI tokens” (coins) that can be spent to request in‑game changes via a “smartphone” item.

The smartphone simulates AI: when you spend tokens and choose a request from a menu, the world changes (e.g. “summarise the path” reveals hints, “generate a bridge” spawns a bridge tile, “refactor code” removes a bugged obstacle).

The “AI” does not actually recode arbitrary game logic at runtime. Instead, it triggers predefined world state changes that feel like AI powers: unlocking shortcuts, changing NPC dialogue, enabling new abilities, and toggling obstacles. This keeps it realistic for a single‑file, 3‑hour build.

Core gameplay loop:

Explore the village and find an obstacle.

Talk to an NPC or sign that hints at an AI concept.

Take a mini‑quiz at an AI terminal; earn tokens for correct answers.

Open the smartphone, choose an AI action, spend tokens, and modify the world to progress.

Reach the final area that celebrates “You used AI effectively”.

Target scope for 3 hours:

One HTML file with embedded CSS and JavaScript.

Simple tile‑based layout using coloured rectangles or a tiny tileset.

Keyboard movement, collision, and 3–5 obstacles.

6–10 quiz questions.

A basic win state screen.

2. Icon
Concept: A simple brain with a graduation cap, with small glowing “tokens” orbiting it, representing AI‑powered learning.

Style: Flat, minimal, and readable when shrunk. Solid background colour with high contrast.

Specifications: 1:1 aspect ratio, preferably 1024x1024 pixels, PNG format for export. Generated using a free/AI image tool (e.g. free‑tier image generator) and then down‑scaled as needed, ensuring licence allows free distribution.

3. Guide
Format: A short, in‑game tutorial overlay plus a short text section in the HTML below the canvas.

Content (in‑game tutorial):

Movement instructions (e.g. “Use arrow keys or WASD to move”).

How to open and use the smartphone (e.g. press “E” to open, select an AI action from a list).

Explanation of AI tokens: “Earn tokens by answering AI quiz questions correctly. Spend them on actions like ‘build bridge’ or ‘reveal hint’.”

A clear note that the in‑game AI is simulated: “In real life, AI tools generate text or images. Here, your ‘prompts’ are choices that change the game world.”

Content (HTML guide section):

Brief explanation of the basic AI concepts demonstrated: prompts, tokens, hallucinations, limitations, and cost/constraints.

Tips and tricks:

“Be specific with your AI requests” (aligned with choosing the right smartphone option).

“AI can help, but you still have to make decisions” (you choose when to spend tokens).

“You can’t do everything at once – tokens are limited, so plan ahead.”

4. Soundtrack
Style: Lo‑fi, ambient, slightly futuristic to create a relaxed “vibe” while thinking about AI.

Generation: Use a free AI music generation tool that allows export for non‑commercial use, or select a royalty‑free lo‑fi loop from a free library (e.g. attribution‑friendly track) and embed it via HTML audio. Ensure:

No login‑walled or paid playback for players.

The audio file is either embedded as a small base64 string or loaded from a free, hot‑link‑friendly source to keep the project self‑contained and cost‑free for players.​

Implementation: One background loop with a simple mute button in the UI.

5. 4-Minute Presentation
Structure:

Introduction (30s)

Ask: “What if anyone could learn how AI works just by playing a simple browser game?”

Show the icon and a quick glimpse of the main screen.

The Problem (30s)

Explain that AI is powerful but confusing, and many people only see it as a “black box”.

Mention that most AI education either feels too technical or too abstract.

Our Solution (1m)

Introduce “Token Trail” as a browser‑based mini‑adventure built using vibe‑coding (AI‑assisted development) at the Vibe‑athon.​

Explain how the game turns AI ideas (prompts, tokens, limitations) into concrete game mechanics: quizzes, tokens, and the smartphone that “changes the world”.

Demo (1m 30s)

Live walk‑through: move the character, encounter an obstacle, answer a quiz, earn tokens, open the smartphone, spend tokens to generate a bridge or reveal a hint, and cross to the next area.

Highlight where AI tools helped: generating quiz questions, writing game logic snippets, creating the icon and soundtrack.

Conclusion (30s)

Emphasise that anyone with curiosity can now “feel” how AI works by playing, not just reading.

Note that the project is a fully playable, single‑file web game that costs nothing to access, making it easy to share with schools and communities.

6. Demo
Format: Live browser demo during the presentation.

Content:

Start at the initial spawn area with a short tutorial text bubble.

Walk up to the first obstacle (e.g. a closed gate).

Interact with an AI terminal to trigger a 2–3 question quiz.

Show rewards: tokens appear in the HUD.

Open the smartphone UI, pick an “AI action” (e.g. “ask AI to build a bridge”), spend tokens, and visibly change the map so the player can pass.

Reach the final goal area to show the “You completed the Token Trail” screen.

7. AI Usage Explanation
LLM-assisted Development:

Used AI tools (e.g. Gemini, ChatGPT, Claude) to generate and refine HTML/CSS/JS snippets, sprite ideas, quiz content, and text for the in‑game guide.

Applied vibe‑coding: describe the desired behaviour in natural language, let the model propose code, then iterate rapidly with small tests, keeping everything in one HTML file.​

Asset Generation:

Used AI image generation (free tier) for the brain‑with‑cap icon, then resized and exported as PNG.

Used an AI music generator or royalty‑free track for the lo‑fi background loop, ensuring free usage for players.

In-Game AI:

The in‑game “AI phone” uses scripted rules that simulate AI behaviour (predefined outcomes mapped to “requests”) rather than calling paid APIs or running large models.

The game explains the difference between real AI (LLMs responding to prompts) and this simplified simulation, making the game playable entirely offline and free for all users.
