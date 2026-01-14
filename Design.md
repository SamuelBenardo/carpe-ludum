# Design (Revised)

## Primary Idea (Clarified Up Front)

A Super Smash Bros–style arena fighter where **the map, objects, and potential characters are generated from a screenshot of whatever is on the player’s screen**. Certain detected items become structures or interactable objects, and certain detected items can become playable characters. The result is that maps and characters can feel effectively infinite, because they can be created and shared by sharing screenshots.

---

## Example Scenario (How It Feels)

Three friends sit in separate corners of a classroom while students take notes on Google Docs. With just a glance, they all know what to do.

- They open the app on their computers.
- One player takes a screenshot of their Google Docs page and starts a lobby.
- While the AI identifies structures, items, and characters, the friends vote on game settings (including whether to allow saved characters, pausing, etc.).
- The map loads. The friends customize a few map elements (examples: adding health boosts, making walls sticky, placing trampolines).
- They choose characters in different ways:
  - One loads an “unbeatable” saved character.
  - One creates a character from a logo visible in the screenshot.
  - One lets AI generate the stats/properties for a character that corresponds to their profile picture.
- The match starts: assignments, fonts, and teleportation portals are flying everywhere, and the Google Docs page slowly starts crumbling, changing the terrain.
- When the teacher walks around, they hit the in-game return button, which instantly switches back to the original tab and auto-pauses the game. Once the teacher leaves, they continue playing.

---

## Core Loop (Step-by-Step)

1. **Capture Input**
   - Player takes a screenshot of their current screen.
2. **Generate Arena**
   - AI identifies items and classifies them into:
     - **Structures** (arena geometry)
     - **Interactive objects** (items with behaviors)
     - **Potential characters** (items eligible to become playable characters)
3. **Set Match Rules (Group Choice)**
   - Players vote on settings (examples: allow saved characters, allow pausing, other features).
4. **Optional Customization (Before the Match)**
   - Players can choose certain map/item behaviors.
5. **Choose Characters**
   - Characters can be AI-generated or player-generated (with restrictions).
6. **Play**
   - Objects can have physics so the arena can change in real time.
7. **Share / Save**
   - The screenshot itself is the “seed” that can be shared.
   - Interesting/powerful characters and maps can be saved for reuse (if enabled).

---

## Screenshot-to-Arena System

### Object Identification

The game uses the screenshot to identify and label on-screen elements as:

- **Structures** (arena pieces)
- **Interactive objects** (usable or behavior-driven elements)
- **Playable characters** (eligible elements that can be controlled by players)

### Physics and Real-Time Map Change

Certain objects in the screenshot can be assigned physics so the map can **change in real time** as play unfolds.

### Player-Chosen Behaviors (Map / Objects)

Some behaviors of items or map elements can be player-chosen before the match (examples shown in the scenario: health boosts, sticky walls, trampolines).

---

## Characters

### What Can Become a Character

Certain items on screen can be marked as playable characters.

### How Character Properties Are Determined

A character’s **moveset, movement, and stats** can be determined in one of two ways:

- **AI-generated**
- **Player-generated**, but subject to clear restrictions so characters don’t become overpowered

### Saved Characters

If a player creates or finds a character that is particularly interesting or powerful, that character can be saved and reused in later games **if the players agree and if the match settings allow it**.

---

## Stat & Ability Restrictions (Clarification to Prevent Overpowered Characters)

Player creativity is a core feature of the game, so player-generated characters remain an option — but **the restrictions must be explicit**.

### Budget System (Point Allocation)

A basic restriction model is a **point-budget system (diep.io-style)**:

- Players are given a **maximum number of points** to allocate across character stats.
- The game includes **many different stat categories** so characters can be customized “from head to toe.”
- Because the point cap is limited, **players cannot max out every stat**.

### Baseline vs Optional Stats

- Certain core stats (for example: **health, damage, speed**) have a baseline.
- Other stats are **not automatic**. If a player assigns **no points** into a category, the character simply **does not have that property** (example: if no points are placed into “body damage,” the character has no body-damage property at all).

### Ongoing Tuning Philosophy

These regulations are important, but will likely need refinement as the game evolves. The goal is the **highest degree of freedom possible while keeping the game fair and fun**.

---

## Transparency vs Mystery (Match Setting)

Players can decide whether:

- The game **informs everyone** about the properties of the map/mechanics, or
- Some properties remain **unknown**, keeping the match “mysterious.”

---

## Controls

Basic controls:

- **W** = jump  
- **A** = move left  
- **S** = character ability  
- **D** = move right  
- **SPACEBAR** = another ability  
- **SHIFT** = another ability  

---

## Play Modes

- **Online multiplayer**
- **Local multiplayer on one computer** (two or more players)

---

## Designed to Be Playable in Class

The game is designed to be playable in class:

- With one button, the screen **immediately switches back** to the tab/app the screenshot came from.
- The game also **auto-pauses** when switching back.
- This feature can be **disabled** if an opponent abuses it in non-urgent situations.

---

## Saving & Sharing

### Sharing

- Maps and characters can be shared simply by **sharing screenshots**.

### Saving

- Maps and characters can be **saved** if they are particularly interesting/powerful.
- Saved characters can be reused in later maps **if enabled** and if players agree.

---

## Future Features & Expansion

### Competitive Features

After the main game is built, adding the following would “professionalize” the game:

- Leaderboards
- Ranking
- Tournaments

### Mobile Version

A mobile version could replace controls with:

- A joystick
- Tappable buttons

### Player-Programmed Abilities (If Needed)

It may be necessary to allow players to program abilities and import them into the game, with safeguards so that if the code is dysfunctional, the game does not break.

---

## Food for Thought / Crazy Secondary Ideas (Not Core)

These ideas are explicitly secondary and build off the base concept:

- **Bossfight / Infinite rounds mode** where players cooperate against generated enemies (also from the screenshot).
- **Screen recordings** as input (like screenshots, but the map constantly changes).
- **Phone idea**: placed here intentionally as a non-core concept, and open to reevaluation based on what people like — but not treated as part of the main design.

---

# Appendix A — Original Proposal Text (Reference)

*(Original text preserved as reference; the sections above are the clarified/rewritten design.)*

This game takes a screenshot and identifies different items on screen as structures and interactive objects that are used to set the arena for a super smash bros type game. Giving certain objects in the screenshot physics lets the map change in real time. Certain items on screen are marked as playable characters, whose moveset, movement, and stats are either AI generated or player generated (stat sum limits are placed on player made stats). The basic controls are W (jump) A (move left) S (character ability) D (move right) SPACEBAR (another ability) SHIFT (another ability). Certain map or item behaviours can also be player-chosen. This way, map and character variations and possibilities are infinite and can be shared simply by sharing screenshots. You can play in ANYTHING as ANYTHING. These maps and characters can be saved if the player finds and creates one that is particularly interesting or powerful. If enabled, this saved character can then be reused in a new map and game depending on what the players agree on for that game. The players can agree to share their chosen mechanics, and have the game inform them of the properties of the map, or to keep it all a mystery.

The game is designed to be playable in class; with the click of a button, the screen immediately switches back to the tab or app the screenshot was taken from, as well as auto-pauses the game (this can be disabled if the opponent abuses the feature in non-urgent situations). The game can be played online, or on one computer, with two or more players. In my opinion the crux of this idea, and the main appeal of the game, is that its scope and enjoyability is limited only by the imaginations of the users.

After the main game is built, leaderboard, ranking, and tournament feature implementation would professionalize the game. A mobile version would simply replace the controls with a joystick and tappable buttons. It may be necessary to let players program the abilities of their own characters and import it into the game, with safeguards in place that ensure when the code is disfunctional, the game does not break. Going off the rails here, there can be a bossfight, or infinite rounds mode, where players work together to defeat generated enemies (of course also from the screenshot). Why stop at screenshots? Screen recordings are like screenshots, but now the map is constantly changing. Absolute pandemonium! But, these concepts are secondary and only build off of the base game idea since it is so versatile.

Three friends sit in separate corners of a classroom. The teacher is lecturing the most boring topic imaginable, and students are taking notes on google docs. With just a glance, the three know what to do. All three students open the app on their computer while one screenshots their google docs page and starts a lobby in the game. While the AI identifies structures, items, and characters, the friends vote on the settings of the game and decide to allow premade characters, game pausing, and all other features available. The map loads in, and the friends each customize different items around the map, adding health boosts, making walls sticky, and placing trampolines. One player chooses to load in their self-proclaimed unbeatable saved character, the canvas logo, while another creates one out of the google docs logo, and the final player lets an AI generate the stats and properties on their character that is their profile picture. The game starts, and assignments, fonts, and teleportation portals are flying everywhere, while the google docs page slowly starts crumbling, complicating the terrain. Inevitably, the teacher starts walking around the classroom. Thankfully the friends all linked their in-game return buttons to the tab they were supposed to be working on, and after the teacher continued their lecture, completely unsuspecting of foul play, the game continued.

# Appendix B — Feedback Text (Reference)

I really like this idea of making the game entirely customizable and from the user’s screen! However, I think it's a bit unclear what this actually means until you reach the second paragraph, so I would clarify the primary idea upfront. Here, you can probably move the final paragraph at the bottom to the top since it's a more general description of the idea, rather than an explanation of the logistics. I think this proposal would also benefit from being broken down like the samples rather than in one long paragraph for readability.

I think using AI or random generation is the right approach, rather than having the player determine stats. Even with the limit, I think it would be easy for players to just max everything out.

To me, the phone idea loses the primary concept. Would there be a faux joystick & buttons on the phone? If so, it loses the idea of it being undetectable (also not as plausible w/ the phone being out in the first place).

While I like the idea of this being expanded to screen recording, I think it could very quickly get out of hand and make the game very unbalanced.
