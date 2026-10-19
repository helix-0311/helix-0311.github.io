---
layout: post
title: "The Detection Game"
date: 2026-10-19
---

In MBAT, one of the things you have to balance is where you *think* the enemy is versus where they *actually* are. The Detection Game handles that, complete with Direction Finders, ECMs of different strength, ECCM, False Contact Emitters and other electronic warfare devices that all hope to do one thing: make it very difficult to lock on and isolate the enemy before visual contact is established.

### Seeing Is Hard

The reality on the ground in combat is: things are a lot harder to see than in the movies. Terrain, camouflage and movement (or lack of it) all act together to hide even something as large as a vehicle.

I want to preface this section with: I never operated a radar, hell I never even saw one. So what's here is a best guess of what future warfare might look like and act like.

### Detection States

There are four 'states' of detection, each one ascending in order of 'do-something-about-that'ability.

* **Undetected**: It means what it says on the tin. Surprisingly, you can get awfully close to someone that's unaware without being detected.
* **Suspected**: You know the enemy's general location a little better than 'over yonder', but less than 'they're in that treeline'.
* **Confirmed**: This is the, 'they're in that treeline', but you still have no idea *what* is there. Could be big, could be small, but you know with pretty good certainty where they are.
* **Identified**: You know exactly what they are, exactly where they are and you've either got them on some sensors or have visually identified the target.

### How That Works With a 4 Meter High Power Armor

Power armor (colloquially called 'Frames' in-universe) in MBAT is remarkably mobile, as befits its lineage from Starship Troopers. MBATs can stand, kneel, go prone, dive to cover, and jump based on what equipment they're carrying. Some Frames are also running stealth fields, have silenced equipment, or other such advantages.

Frames also come in different sizes:

An **Ultralight** is a little bigger than a tall person, and is (you probably guessed) more suited to a `Scout` role than anything else. Exceptionally fast, often mounting stealth fields and silenced armor, Ultralights and their slightly-larger cousin, **Light** Frames, have a low `SIGNATURE` and are difficult to detect. As you move up in the Frame classes (Ultralight to Assault), each class has more signature and less stealth available to it.

That's part of it. Movement is another. Most predators' eyes are really good at detecting movement - that's why many animals respond to threats by standing still or hiding. I assumed that was also true of the aliens that Humanity is fighting in MBAT; movement draws attention, both visually and aurally. Prone and crawling is a lot more difficult to detect than sprinting through full view. Prone and only observing is the most difficult to detect of all.

### Future Warriors

I'll talk more about how Frame roles work in later posts, in part because I'm still inventing some, and in part because I plan on covering the core tactical game loop first.

But one Frame role stands out for its effects on the squad you dropped with: the `Command` role. A Command Frame's unique ability is that it lets the entire squad access each other's sensor and weapons data. Meaning that what your Ultralight scout Frames see, your Heavy and Assault `Combat` Frames *also* see.

The Command Frame is a bit of a jack-of-all-trades. It's the only Frame that can mount the `Command Uplink`, which lets the squad share its targeting data, and it *also* has limited ability to mount an ECM, advanced shields and armor, and heavy weapons.

Command Frames are what make the Detection Game so important; without them, you're in a continuously escalating loop of getting more and bigger Frames because you've got to survive contact with the enemy to shoot back. With them, you're able to specialize. You **need** Scout Frames because they give you the ability to engage beyond visual range, whether with `Artillery` Frames or with non-line-of-sight weaponry (like missiles).

### What That Means for Gameplay

Gameplay-wise, it means several things.

* Ghost contacts show up every round, and you can't tell a ghost contact from a real one until you try to lock it or fire on it.
* It means that attempting to ping or use Active ECM helps you - but it also raises your Signature and makes *you* easier to detect in return.
* When you Suspect a contact, it might **actually** be there, just... not exactly where you think it is. That means that some contacts will **seem** like ghost contacts, but aren't.
* Firing your weapons (unless they're silenced, somehow) is a *very* large giveaway for your position.
* Some Drones have the ability to register as different things - for instance, a high-priority Command Frame - which would draw the enemy toward it. Command Frames are the highest-priority target that the enemy AI has, after all. So there's a deception angle to the Detection Game, also.
* Making yourself harder to detect has numerous bonuses, and breaking line of sight/moving through heavy cover actually does something for you. It can break enemy locks, as well.

Lastly, I'll wrap up on a piece of gameplay philosophy. The enemy AI gets no information it hasn't earned. There's no 'cheating' so that it always knows where your forces are; it follows up on ghost contacts just like a real player does. Its units, though, have capabilities yours don't. One of their infiltration units carries short-range electroreceptors that see right through your stealth.

I'll talk more about the enemy you face in MBAT in a later post, but to summarize them: they are an electronics-heavy force, with additional, special EWAR capabilities that the player doesn't have. In return, the player gets other, different advantages (like survivability).

### Closing Thoughts

In the military, we have a thing called an OODA loop. Observe-Orient-Decide-Act. One way to outmaneuver an enemy is to break their OODA loop before they can break yours. The Detection Game focuses on the first and second parts of the OODA loop - literally either hiding or deceiving the enemy so that you can position your forces to get the most damaging strike. So far, it's one of the things that I think are fairly unique to MBAT in how it's implemented, but it still needs another pass of polish or two before it really shines.