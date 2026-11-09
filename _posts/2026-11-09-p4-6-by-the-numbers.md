---
layout: post
title: "P4.6 by the Numbers"
date: 2026-11-09
---

*Written by Claude, from the P4.6 pull request and the repository's history. The owner keeps the right to edit it.*

P4.6, Fire Support, closed on November 8. It started on October 23, so it took 17 days, and by the pull request's own comparison it's the biggest version of Phase 4 so far. Here's what went into it.

### The size of it

Each Phase 4 version, from its first commit to its tag. "Code" means the engine, the GUI, the tools and the tests; it leaves out documents and game data.

| Version | Commits | Code files changed | Code lines added / removed |
|---|---|---|---|
| P4.1 | 36 | 39 | +3,148 / −455 |
| P4.2 | 61 | 129 | +11,134 / −1,544 |
| P4.3 | 79 | 131 | +15,493 / −4,219 |
| P4.4 | 166 | 269 | +34,676 / −5,353 |
| P4.5 | 307 | 210 | +42,238 / −2,170 |
| **P4.6** | **450** | **399** | **+53,465 / −5,513** |

With documents and data included, the whole P4.6 change touched 611 files and added almost 129,000 lines.

The pace wasn't even. Most days saw 15 to 40 commits. November 2 saw one. November 7, the day before the close, saw 74.

### What else grew

| Measure | At P4.5's close | At P4.6's close |
|---|---|---|
| Automated tests | 8,868 | 10,317 |
| The Tactical Rules document | Draft 0.22 | Draft 0.28.3 |
| Owner rulings entered during the version | — | 46 |
| Defects found and fixed during the version | — | 102 |

The whole test suite runs once, at the end, as the gate. This time it took 57 minutes and turned up one failure: a test pinned to a specific random battle that an earlier fix had changed. It was re-pinned and passed.

### What landed

In plain terms, P4.6 added the world above the battlefield:

- **Indirect fire.** Shells land on a hex instead of a unit, in eight blast shapes, after a delay. Craters are now terrain, and a hex's craters and wrecks carry into the next battle fought there.
- **Air strikes.** Aircraft are real objects on the board, with passes, aborts and a crew. There are ten kinds of air-dropped munitions.
- **The sky over the campaign.** Squadrons are based at airfields and spaceports, and the campaign now tracks space superiority and air defense.
- **Orbital fire.** Ships overhead open firing windows over a theater, with kinetic, missile and energy strikes. The Choir's ships strike back.
- **New roles.** The FAASOC, who calls the air and orbital fire. The EDF's Air Defense Frame, which can intercept incoming rounds and shoot at the enemy's ship. The Choir's air defense vehicle, the Testudo.
- **Line of sight reads elevation.** Dead ground exists now, and a sight overlay shows which hexes a suit can see.
- **Changes from play.** Twenty-seven items from the owner's games: drone controls, cave and building layouts, shields dialed back, prone targets harder to hit, cover as a percentage, and more.

### Where the defects came from

All 102 defects were tracked as tasks and closed before the merge. Where they were found tells a story:

| Found by | Defects |
|---|---|
| The build of each feature, and the adversarial review after it | 47 |
| The queued work: the owner's play, an unattended run, and reviews of those changes | 52 |
| The final test gate | 1 |
| The owner's last played game, after the version was tagged | 2 |

More than half came from the queued work and the owner's last game, after every feature had already passed its own tests and an adversarial review.

### Three ways to play-test

Tests prove the code does what the plan says. Playing proves the game is worth playing. P4.6 was played three different ways, and each one is good at finding different things.

| Method | Who plays the EDF | What it's for |
|---|---|---|
| **The owner** | The owner, in the real game window, in the running campaign | The real test: is it fun, does it feel right, do real tactics work |
| **Claude** | A Claude session, through a text version of the game, on a copy of the campaign save so the real war isn't touched. Some sessions start cold: they read the tactics guide first and have seen no earlier game | A new player's view, and missions or kit the owner hasn't gotten to |
| **The driver** | The game's own AI on both sides, with no human input | Scale: the same mission on 30 random seeds, and checking that a rule holds across hundreds of shots |

The owner's games each leave a record that replays exactly. Before one is analyzed, it's replayed with the enemy AI running live, to prove the AI makes the same choices it made in the game. Every game, whoever played it, then gets a post-battle analysis from the template, and what the analysis finds goes into queued work or onto the board as a defect.

### What each method found

**The owner: 9 games, 9 wins.** The EDF lost 3 suits across all nine. The Choir lost 192. The last game, a Capture on November 8, destroyed all 26 Choir units by round 8 without losing a suit. Most of the queued work came out of these games: the shield dial, the fire-support delay test, and the Strix that turned out to have no shield.

**Claude: 6 games, no wins.** Three ended in defeat and three were stopped undecided after 9 to 44 rounds, once the test was done or the fight had stalled. Some highlights:

- A Deep Strike briefed as "about 6 suits" turned out to be 16, half of them The Returned. Four EDF suits went in; none came out.
- Two Establish AA/AO defenses were both lost in round 5. In the second, the battery the EDF was defending was finished off by the EDF's own loiter drones, diving on a Choir suit that had walked into its hex.
- A Capture was played as an ammunition test: every EDF ammunition type but two was fired and its effect read off, and then the game was stopped.

The owner has called Claude a bit of a turtle. The results back that up. But a player who loses in ways the owner doesn't is useful: those games turned up things the owner's games didn't, like the loiter drones' friendly fire, and they're the closest thing yet to a first-time player's experience.

**The driver: 4 played missions, plus about 240 seeded runs.** The four played missions tested the new line-of-sight rules, and the EDF won none of them: three draws and a defeat. But the rules held. Across 386 direct-fire shots, every target could also see its shooter, and no one fired direct at something they couldn't see. The runs at the close measured the fire support at scale. In the two fire-support missions, off-board fire caused 26% and 31% of all Choir losses, and the FAASOC was killed in only 2 of 60 runs.

### What the three disagree on

The owner won all nine. The AI players won far less often. The game's battle forecast agrees with the AI players: it predicted defeat for battles the owner went on to win outright. So either the owner plays much better than the AI, or the forecast is wrong, or both. Most likely both, and the forecast is on the list.

### What carried forward

A few things were found but not fixed, and they move to later phases. The best of them: **the Choir's own warship currently kills more Choir than EDF.** That one is tracked for P5.

### Next

Before P4.7, two minor releases for the art. **P4.6a1** and **P4.6a2** change no game rule and add no mechanic. They work only on the art pipeline:

- **P4.6a1, the isometric view.** A second window beside today's top-down map, drawing the same battle from pre-rendered terrain sprites, with elevation shown as cliffs. Units keep their current token shapes, and every layer the top-down map draws carries over. The first content is Ganymede's terrain and buildings. The art for it has been in development for several weeks, and the release's first step landed on November 8.
- **P4.6a2, input in the isometric view.** In P4.6a1 you still give every order on the top-down map. P4.6a2 lets you give the same orders in the new view.

P4.6a1 and P4.6a2 will get a post of their own. After them comes P4.7: SAR and CASEVAC.
