Overview
“Token Trail” is a small, top‑down 2D browser game where players learn core AI/LLM concepts by solving obstacles using an in‑game “smartphone” powered by AI tokens. The game runs entirely in a single HTML file (inline CSS + JS) and is free to play in any modern browser. The design is scoped for a ~3‑hour vibe‑coding session and focuses on one small map, a clear core loop, and simple, scripted “AI” behaviour.

High-level Goals
Teach basic AI/LLM concepts (prompts, tokens, limitations, hallucinations, cost) through a short playable experience.

Showcase vibe‑coding: AI‑assisted development of HTML/JS, text, questions, icon, and soundtrack.

Ship a complete, no‑login, no‑cost browser game that runs from a single HTML file and can be easily shared (e.g. via GitHub Pages or local file).

Success criteria:

Playable start‑to‑finish in 3–8 minutes.

Player can:

Move around the map.

Answer quiz questions.

Earn and spend AI tokens.

Trigger smartphone actions that change the world.

Reach a clear win state.

Concept And Fantasy
Working title: Token Trail
Tagline: “Spend AI tokens, change the world, learn how AI really works.”

Fantasy: You’re a curious learner in a small tech‑village. The village terrain has broken bridges, locked gates, and confusing signs. A friendly AI lab gives you an experimental smartphone that can “ask AI” to reshape parts of the world—if you feed it AI tokens earned by answering questions and using it responsibly.

Core theme: AI is powerful but constrained; you need good prompts and careful spending of limited tokens to reach your goal.

Core Player Experience
Feel: Light, cosy, Stardew‑inspired perspective, but with jam‑scope minimal art.

Session length: 5–10 minutes per playthrough.

Complexity: Suitable for beginners (teens/adults) with no coding background.

Player should feel:

Curious: “What will happen if I use AI this way?”

Empowered: “I learned something about AI and used that knowledge to solve a puzzle.”

Constrained: “I can’t just brute‑force; tokens are limited, so I must think.”

Platform And Technical Constraints
Platform: Desktop browser (Chrome/Edge/Firefox). Mobile-friendly if time allows, but not required.

Technology:

Single HTML file.

Inline <style> and <script> only.

No external JS frameworks required (vanilla JS).

Optional: one small audio file (lo‑fi loop), either embedded as base64 or hosted from a free source.

No runtime network or paid API calls:

No calls to cloud LLMs from the game.

All “AI” behaviour is deterministic and scripted in JS.

Game Mechanics
Core Loop
Explore: Move around the small map and find an obstacle (gate, broken bridge, hazard).

Learn: Interact with an NPC or terminal that explains or hints at an AI concept.

Quiz: Take a short quiz (1–3 multiple‑choice questions) and earn AI tokens for correct answers.

Plan: Decide how to use tokens (which AI action to buy).

Act: Open the smartphone, select an AI action, spend tokens, and change the world.

Progress: The map updates (bridge appears, gate opens, hint is revealed). Move on to the next obstacle.

Complete: Reach the final goal area and see a short end screen summarising what you “learned”.

Player Actions
Movement:

WASD or arrow keys for up/down/left/right.

Interact:

Space or Enter near an interactive object/NPC to talk or open UI.

Smartphone:

E (or another key) to open/close the smartphone menu.

Up/down arrows (or mouse) to select an AI action.

Enter/space (or mouse click) to confirm an action.

Systems
Tokens (AI currency)

Earn tokens:

Each correct quiz answer: +1 token (configurable).

Optional: bonus tokens for answering all questions in a set correctly.

Spend tokens:

Each smartphone AI action has a token cost (e.g. 1–3 tokens).

Display:

Token count visible in a simple HUD (e.g. top‑left: “Tokens: X”).

Obstacles and AI Actions

Obstacles:

Gate: Blocks path; can be opened by a “unlock gate” action.

Gap/river: Requires a “build bridge” action.

Fog or hidden hints: Reveal with “summarise” or “reveal hints” action.

Buggy hazard: Can be “debugged” to disappear.

AI Actions (example list):

“Generate Bridge” (cost 2): Spawns walkable tiles across a gap.

“Open Gate” (cost 1): Changes gate tile from blocked to open.

“Explain the Path” (cost 1): Shows directional hints or marks path on the ground.

“Refactor Code” (cost 1–2): Removes a “bug” obstacle, like a glitchy tile.

“Ask for Clarification” (free or cheap): Shows a text hint about the current puzzle.

These actions are mapped to simple JS functions that modify tile data or show UI.

Quiz System

Format:

Multiple‑choice questions (A/B/C or A/B/C/D).

Each question is a small snippet of text and 2–4 options.

Topics:

What is a prompt?

What are tokens?

What is hallucination in AI?

Why can’t AI always be trusted?

Why do more tokens cost more?

Flow:

Interact with a quiz terminal (e.g., AI Lab computer).

Show 1–3 questions in a simple dialog.

For each correct answer: immediate feedback + tokens.

At the end: summary and maybe a tip.

Learning Explanations (In-game)

Short info text for each concept, shown at:

NPC dialogue (e.g., a researcher).

After each quiz question.

In the final summary screen.

Example structure (you’d write your own wording):

Prompt: “A prompt is the message or instruction you give to an AI to get it to do something.”

Token: “Tokens are tiny pieces of text that AI counts. Long prompts and responses cost more tokens.”

Hallucination: “Sometimes AI makes things up—this is called hallucination. You should still check important information.”

Win/Lose Conditions
Win:

Reaching the final goal tile/area (e.g., on the far side of the river).

Trigger an end‑screen overlay:

“You completed the Token Trail!”

A short recap of concepts.

Lose:

No hard lose state required for jam scope.

Soft‑failures: running out of tokens, wrong answers etc.

If you run out of tokens before finishing:

Provide a way to earn at least a small number of tokens again (e.g., a repeatable quiz or a “daily reward” terminal), or

Provide a free “Reset Level” button that restarts.

World And Level Design
Map Layout (Single Level)
Size: e.g. 20×15 tiles viewport (or scrolling if comfortable).

Regions:

Start area:

Spawn point.

Tutorial NPC/sign (“Use arrows to move, E to open phone”).

AI Lab:

Quiz terminal #1: prompts and tokens.

Basic explanation text.

River/Gap Area:

Broken bridge.

Requires “Generate Bridge” action (cost 2).

Gate Area:

Locked gate blocking straight path.

Requires “Open Gate” action (cost 1).

Fogged Path:

Tiles with “fog” overlay.

“Explain Path” removes fog or shows arrows.

Goal Area:

NPC or sign: “You reached the end of the Token Trail!”

End‑screen trigger.

Visual Style
Art approach:

Minimal tile style: rectangles or simple pixel‑art blocks.

Colour palette: a handful of soft colours for ground, obstacles, buildings, characters.

Characters:

Player: Small, single‑colour square with a simple sprite or 2‑frame animation if time allows.

NPCs: Stationary characters with different colour.

UI:

HUD: token count; optional small icon for the phone.

Dialog boxes: simple rectangles with text and a “Press space to continue” hint.

Smartphone menu: full‑screen or panel overlay with list of actions and their token costs.

Audio And Icon
Soundtrack
One ambient lo‑fi loop (30–120 seconds), looped.

Must be:

Free to use (e.g., AI‑generated on a free tier or CC‑licensed with attribution).

Kept small to avoid bloat.

Controls:

Simple mute/unmute button in UI, visible but unobtrusive.

Icon
Brain + graduation cap, maybe a small sparkle/token.

Generated via free AI image tool.

Export as 1024×1024 PNG and then resize for favicon/use in presentation.

Tutorial And Guide Content
In-game Tutorial Steps
Movement and Interaction:

On spawn, show text: “Use arrow keys or WASD to move. Press space near signs to read them.”

Phone:

Sign near lab: “Press E to open your AI Phone. Use Up/Down to pick an AI action.”

Tokens:

First terminal: text explaining tokens and that quizzes give tokens.

Using AI:

After first quiz, prompt: “Try spending tokens to build a bridge at the river.”

HTML Guide Section
Below the game canvas (or in a collapsible section), include:

“How to Play”:

Controls.

Goal of the game.

Loop summary.

“AI Concepts in This Game”:

Short, plain‑language blurbs for key concepts.

“Tips & Tricks”:

Plan your token spend.

Try reading all hints before using the phone.

Remember AI can be wrong in real life.

AI Usage During Development
Document (for the presentation and README):

Code:

Used AI coding assistants to:

Generate basic movement and collision code.

Set up tile map arrays and rendering loops.

Create simple state machines (exploring, in dialog, in quiz).

Content:

Used AI to:

Draft quiz questions and multiple‑choice options.

Suggest short explanation text for prompts/tokens/hallucinations.

Propose names for actions and map obstacles.

Assets:

Icon from an AI image generator.

Music from an AI audio tool or free library.

Clarify that:

In‑game AI is simulated with scripted logic.

Real AI tools were used “behind the scenes” to build the game and assets.

Implementation Plan (Jam-oriented)
Time‑boxed breakdown (~3 hours):

0:00–0:30 – Skeleton

Create one HTML file with:

Basic layout (canvas or div game area, HUD, placeholder text).

Inline CSS for layout.

Empty JS structure: game loop, input handling.

0:30–1:15 – Core Gameplay

Implement player movement and collisions.

Implement tile map and rendering.

Implement one obstacle and one smartphone action (e.g. build bridge).

Implement token counter and basic quiz with 1–2 questions.

1:15–2:00 – Content & Map

Expand map to include all key areas.

Add more quiz questions and terminals.

Add 2–3 more AI actions and obstacles (gate, fog).

2:00–2:30 – Tutorial, Guide, and Polish

Add tutorial text, minimal UI polish, token icon.

Add HTML “How to Play” and “AI Concepts” sections.

Hook up end screen.

2:30–3:00 – Audio, Icon, Testing

Integrate audio loop and mute button.

Finalise icon file and references.

Run through start‑to‑finish a few times to check flow and difficulty.

Accessibility And Performance
Accessibility:

Provide keyboard‑only controls.

Avoid tiny fonts; use high‑contrast colours.

Consider a “Text speed: instant” mode (no slow typewriter effect) if you add one.

Performance:

Minimal asset sizes, no large images.

Simple JS loop; no heavy libraries.
