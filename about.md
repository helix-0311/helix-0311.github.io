---
layout: page
title: About
permalink: /about/
---

MBAT (Mobile Battlesuit All-Terrain) is a single-player tactical wargame
I'm building in my spare time. You command a squadron of battlesuits:
10 to 15 feet tall, large power armor rather than mechs. You fight on a
hex grid with d100 roll-under resolution and alternating activation.
Above the battles sits a campaign layer: a war fought across the solar system, one planet, one theater, one battle at a time.

## How We Got Here

I spent 4 years as a USMC Rifleman (0311), and then got into systems and software engineering about 20 years ago. I created this project originally as an extended systems test for another game I am in the process of making, but as many projects do it outgrew its scope and became its own thing.

Part of this is inspired by my experiences in the Marines; how you fight, what you see, the roles an MBAT uses are modeled after real Marine Corps military occupational specialties. The other part is inspiration and thinking about what the potential future of warfare could hold, plus a long-time love of Battletech and other strategy wargames, with a healthy dose of Heinlein and Starship Troopers.

## How It's Built

- Python, as a desktop app (wxPython for the interface)
- SQLite for saves
- All game content (suits, weapons, missions, the campaign) is JSON
  data, not code
- Built with an AI coding assistant (Claude Code). I write the initial design spec, we turn it into a brief, then iterate until we have a solid design plan. Then it goes to engineering planning, implementation, then multiple reviews.
- Everything you see here is my ideation and experience, extracted and put onto a hex grid. Claude writes code, I review it; I use this tech stack because I've used it for 20 years. Claude just makes me faster.

## This Blog

This is where I think out loud: why a rule works the way it does, what
play testing changed, what got cut, and a bit about the setting.
Nothing here is a promise. Every number in the game is provisional
until play says otherwise.
