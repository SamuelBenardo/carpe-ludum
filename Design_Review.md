# Design_Review.md

## 1. Design Review

**Objective:** Assessment of core features, user flow, and interactive elements.

* **Character Selection Flow:**
The design mentions that "certain detected items can become playable characters" and one player can choose a "saved character" while another lets AI generate one.

* **Question:** How is the conflict resolved if two players want to be the same object on the screen? Is there a drafting phase (Turn 1, Turn 2) for picking objects, or is it first-come-first-served?
* **Question:** If the AI identifies 50 objects, how does the UI prevent clutter when selecting a character? Does the user click the object directly on the screenshot, or select from a list?

* **The "Panic Button" Mechanics:**
The game features a button to "instantly switch back to the original tab and auto-pause".

* **Question:** In an **Online Multiplayer** context, how does this affect other players? If Player A hits the panic button because their teacher is walking by, does the game pause for Player B (who is safe at home)? If it pauses for everyone, this could be used to troll opponents during critical combat moments.

* **Map "Crumbling" & Evolution:**
The scenario describes the page "slowly starts crumbling, changing the terrain".

* **Question:** Is this destruction permanent for the round? If players destroy too much of the "Google Doc," is it possible to destroy all platforms and make the map unplayable/impossible to navigate? There might need to be a "regeneration" mechanic or indestructible base floor.

* **Visibility:**
* **Question:** Since the background is a static screenshot (e.g., text on a white page), how does the design ensure the characters (which are also cut from the screenshot) are visible? A character cut from a black letter "A" might be invisible against a black header bar.

---

## 2. Honor Code and Law Violations

**Objective:** Compliance with school, state, and government rules.

* **Academic Integrity & School Rules (Major Concern):**
* 
**Finding:** The "Designed to Be Playable in Class" section and the "Panic Button" feature are explicitly designed to deceive teachers and facilitate non-educational activities during class time.

* **Recommendation:** While the "Boss Key" is a classic gaming trope, explicitly marketing it as a tool to fool teachers violates the spirit of the School Honor Code regarding responsible use of technology and respect for the learning environment.
* **Adjustment:** Reframe this feature as a "Quick-Minimize" for privacy or convenience, rather than a tool for academic dishonesty. Remove the specific scenario describing students ignoring a lecture.

* **Intellectual Property (Copyright/Trademark):**
* 
**Finding:** The scenario mentions playing as the "Canvas logo" or "Google Docs logo".

* **Recommendation:** While likely falling under fair use/parody for a school project, distributing a game that encourages generating characters from trademarked logos could be an issue if the game is published.
* 
**Adjustment:** Add a disclaimer that the user is responsible for the content they generate, or ensure the "Shared/Saved" characters  are vetted for IP infringement before being shared publicly online.

* **Privacy (Data Protection):**
* 
**Finding:** The core loop involves taking a screenshot of the user's *current screen*  and uploading it to a lobby.

* **Recommendation:** Users might accidentally screenshot sensitive data (personal emails, grades, private messages) and share them as a map.
* **Adjustment:** The design should include a "Review Screenshot" step before the map is generated/shared to confirm no sensitive PII (Personally Identifiable Information) is visible.

---

## 3. Constructive Ideas

**Objective:** Suggestions to improve design, aesthetics, and fun factor.

### Strengths (The Rizz)

* 
**Infinite Replayability:** The core concept that "maps and characters can be effectively infinite"  is a fantastic hook. The idea that players create the content just by browsing the web is very engaging.

* 
**Diep.io-Style Stat Budget:** The "Point Allocation" system  is a smart design choice. It solves the "overpowered character" problem without removing player creativity. It forces players to make strategic builds (Glass Cannon vs. Tank) rather than just making "God Mode" characters.

### Suggested Improvements

* **1. Visual "Pop" for Characters:**
* **Issue:** Characters generated from the background will blend in with the background.
* **Suggestion:** Add a design rule that all active characters get a thick, colored outline (Player 1 Red, Player 2 Blue) or a specific "glow" effect. This ensures that even if I am playing as a text letter "A" on a page full of text, I can clearly see where I am.

* **2. "Draw-to-Create" Customization:**
* **Issue:** Sometimes a screenshot is boring or lacks platforms (e.g., a blank page).
* **Suggestion:** Before the match starts, allow players to use a "Pen Tool" to draw lines on the screenshot. The AI then treats these drawn lines as solid beams or platforms. This gives players agency to fix "bad" maps before playing.

* **3. The "Ghost" Mechanic:**
* **Issue:** In smash-style games, getting knocked out early is boring.
* **Suggestion:** When a player is eliminated, let them control the "Mouse Cursor" of the computer. They can click on map elements to trigger small hazards (like deleting a word in the Google Doc to make a pitfall) to mess with remaining players. This keeps eliminated players engaged.

* **4. Preset "Game Modes":**
* 
**Issue:** The design mentions voting on many settings. This can take too long.

* **Suggestion:** Create "Card Presets" for rules.
* *Heavyweight:* Gravity 200%, Knockback 50%.
* *Moon Mode:* Gravity 10%, Speed 200%.
* *Insta-Gib:* 1 Hit Kills.
This makes starting a game much faster than voting on individual sliders.
