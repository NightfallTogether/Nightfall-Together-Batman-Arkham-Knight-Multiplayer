<img width="1899" height="1056" alt="NT_1" src="https://github.com/user-attachments/assets/9db06757-cb90-4ce8-9e34-84eba29f47b7" />

<h1 align="center">Nightfall Together</h1>

<p align="center">
  <strong>Online co-op for <em>Batman: Arkham Knight</em> on Steam PC, powered by Nightfall Network</strong>
</p>

<p align="center">
  Two to four players. One Gotham. One shared campaign.
</p>

<p align="center">
  <a href="#what-it-does-today">Features</a> •
  <a href="#modes">Modes</a> •
  <a href="#goal">Goal</a> •
  <a href="#completion-checklist">Completion Checklist</a> •
  <a href="#requirements-testers">Requirements</a> •
  <a href="#legal">Legal</a>
</p>

---

> **Development Status — Active development, playable with testers**
>
> Most systems are built and many have been verified across two PCs.  
> The full campaign is **not yet playable from beginning to end in co-op.** Crashing still occurs often at certain times due to active development.
>
> See the [completion checklist](#completion-checklist) for current progress.

**Nightfall Together** is a multiplayer project that lets two to four players share the same Gotham — the same enemies, fights, world state, missions and story — while each player controls the character they choose.

This repository documents the project. **The source code is private and no project files are distributed here.** Each player must own their own copy of *Batman: Arkham Knight* and any DLC they want to use.

---

<img width="1834" height="999" alt="NT_2" src="https://github.com/user-attachments/assets/c851fcad-908e-4aa4-a71f-60d462446321" />

## What it does today

### Playing together

- **Steam lobbies and invites** — Host from the in-game menu and invite friends, or join a friend's lobby.
- **Late joining** — Players joining an existing session catch up to the current world state using a rebuilt baseline plus the events that have occurred since.
- **Up to four players** in the same open-world Gotham, each controlling their own character.
- **Join Teammate** — A pause-menu option moves you beside a teammate, or into their current area if they are elsewhere.
- **Team HUD** — Displays each player's character, health and status, including downed, paused, AFK and vehicle states.
- **World markers** — Teammate name tags, compass markers, city-map markers and player pings, each in that character's colour.
- **Proximity voice chat.**
- **Collective pause** — The world stops only when everyone is paused. Paused or AFK players are protected.
- **Lobby settings** controlled by the host, including enemy-count scaling from **1x to 3x**.

<img width="1882" height="1058" alt="NT_5" src="https://github.com/user-attachments/assets/ef7194c5-7ffe-44e0-8a40-58e6498fe5ab" />

### Characters

**Current playable roster:**

Batman · Robin · Nightwing · Catwoman · Azrael · Batgirl · Red Hood · Harley Quinn · Joker · Deathstroke

**Stand-in villains** — their own look, on a compatible playable body:

Scarecrow (Nightwing) · Two-Face (Azrael) · Professor Pyg (Harley Quinn) · Penguin (Batgirl) · Riddler (Catwoman)

**Community roles:**

- **Militia Grunt** — Red Hood's guns and movement, in the militia uniform. You play in first person; everyone else sees the grunt in third person. This is a character, not a game mode. It needs the Red Hood story pack.
- **GCPD Officer** — the game's first-person officer. Allied with Batman and the Bat-family, and hostile to militia. No glide and no grapple.
- **Invader** — Deathstroke's appearance on Nightwing's movement. Choosing Invader starts an invasion. See [Modes](#modes).

- Switch characters at any time using the in-game character chooser.
- Other players see your selected character's appearance, movement and colour.
- Each character is being brought toward **Batman gameplay parity** where possible:
  - Glide or equivalent traversal
  - Grapple
  - Counters
  - Takedowns
  - Gadgets
  - Detective Mode
- The GCPD officer is the exception on traversal: that body is first person and has no glide or grapple.
- Players who do not own a character's required DLC see a stand-in rather than a broken or missing character.
<img width="2494" height="1394" alt="NT_6" src="https://github.com/user-attachments/assets/94728100-8dbc-4381-8f54-2929ad16f5ad" />

### Modes

Co-op campaign is the default. These two modes are separate from it, and from each other. Picking the militia grunt in an ordinary session does not start either one.

- **Manhunt** — a host session setting. The party travels into one interior, chosen at random from GCPD, Panessa Studios and Ace Chemicals, then back to the city when the round ends. Militia play at a locked 65° field of view with extra health. They win by reaching the extraction. Batman wins by thinning them out before the countdown ends. The round does not write the campaign save. Open-world manhunt is not in this build.
- **Invasion** — starts when a player is the Invader, and ends when that player leaves the role. The invader wins by taking every defender down or reaching the objective. The defenders win by finishing the encounter first. Invasion does not use manhunt's camera, health or travel.

Not in this build: bounty races, and a director who places enemies.

### Combat and stealth

- **Shared enemies** — The party fights the same enemies in the same locations.
- The host manages the primary enemy population, while a player who owns a district can simulate and publish its enemies for the rest of the session.
- Punches, counters, takedowns, beatdowns and knockouts resolve against the same enemy on every screen.
- **Dual Play team takedowns** are supported.
- **Synchronized gadgets**, including:
  - Batarangs
  - Explosive Gel
  - Batclaw
  - REC
  - Freeze Blast
  - Smoke
  - Line Launcher
  - And more
- Shared enemy types and encounters include gunmen, brutes, medics, shields, ninjas, drones, tanks and APCs.
- **Predator rooms** — Guards can see and hear every player; takedowns, alarms and fear states are shared.
- **Downed and revive system** — A downed player can be revived by a teammate, while enemies stop targeting the downed player.
- **Bosses** use shared health and synchronized finishes.

### World and traversal

Remote player movement uses interpolation and prediction, including:

- Running and standard movement
- Gliding
- Grappling
- Diving
- Vents
- Ladders
- Ledges
- Cover
- Cape presentation
- Head look

World interactions stay synchronized between players, including:

- Doors
- Switches
- Cages
- Winchable walls
- Destructible objects
- Lifts
- Puzzles

**Batmobile**

- Every player can have their own Batmobile.
- Driving and battle mode are replicated to other players.
- Winch interactions, weapons and vehicle damage are synchronized.
- Traffic and enemy vehicles are shared.

**Fall recovery**

If a player falls through unloaded or missing world geometry, the system attempts to return them to valid solid ground.

### Progression and side content

- **Missions** — The host drives story progression while objectives, mission selections and Most Wanted progression are followed by the party.
- **XP and upgrades** are shared by the party.
- **Riddler content** — Trophies, riddles, cages and switches count for the group.
- **AR Challenges** can be played together.
- **New Game Plus and Knightmare** follow the host's selected difficulty.
- **Separate co-op save system** — Your normal single-player save is never overwritten by a co-op session. Party progression is stored in the mod's own save sidecar.

---
<img width="2560" height="1440" alt="NT_4" src="https://github.com/user-attachments/assets/04594b83-557a-48f5-9159-88387325641c" />
## Goal

> **The full shipped single-player game, playable by two to four people simultaneously, with every relevant entity synchronized and every playable character brought as close to Batman gameplay parity as possible.**

For Nightfall Together, **"in sync"** means a system is wired end to end with the networking behavior expected from an actual multiplayer game — including interpolation and prediction where appropriate — rather than merely appearing approximately similar between machines.

### The finish line

1. **Full campaign completion**  
   Two players, followed by three and four players, complete Chapters 1–27 through Knightfall without a blocking desync.

2. **Complete entity synchronization**  
   Every relevant entity visible to a player is synchronized:
   - Enemies
   - Turrets
   - Bosses
   - Friendly NPCs
   - Civilians
   - Traffic
   - World objects
   - Scripted set pieces

3. **Enemy parity**  
   Enemy count, position, animation, target and health match on every player's screen.

4. **Character compatibility**  
   Every supported playable character can reach and complete every required objective.

5. **Full content compatibility**  
   Support for:
   - Main campaign
   - Most Wanted
   - Season of Infamy
   - Story DLC
   - Riddler content
   - AR Challenges
   - New Game Plus
   - Knightmare

6. **Robust multiplayer sessions**
   - Reconnect
   - Host migration
   - Late joining
   - Join at arbitrary campaign points
   - Four-hour continuous-session testing

7. **Release-quality product**
   - Finished menus
   - Installer
   - Privacy handling
   - Release packaging

---
<img width="1877" height="1048" alt="NT_3" src="https://github.com/user-attachments/assets/2e25610d-c8dd-4b20-9231-193e0ce68793" />

## Completion checklist

**Legend**

✅ **Working and verified on two PCs**  
🟨 **Built, awaiting two-PC verification**  
⬜ **Not completed**

This checklist covers completion of the base game and its DLC in co-op. Community roles and modes are listed separately. They are in the current tester build and still awaiting two-PC verification.

### Foundation

- ✅ Steam lobby, invites, join and admission
- ✅ Late join — baseline + event tail
- ✅ Network transport, rate limits and session integrity
- 🟨 Reconnect with every system restored
- ⬜ Host migration when the host leaves
- ⬜ Three-player sessions verified
- ⬜ Four-player sessions verified
- ⬜ Four-hour soak test within performance budget

### Players and characters

- ✅ Player movement, interpolation and traversal on every screen
- 🟨 Head look, capes, glide and grapple presentation
- 🟨 Character switching displayed correctly on every screen
- 🟨 Every character at Batman parity for traversal, combat and gadgets
- 🟨 Stand-in villains — Scarecrow, Two-Face, Pyg, Penguin and Riddler
- 🟨 Militia Grunt, GCPD Officer and Invader in the character chooser
- 🟨 Downed state, revive, death floor and respawn
- ✅ Team HUD, name tags, compass and map markers
- 🟨 Proximity voice chat

### Community modes

- 🟨 Manhunt — interior round in GCPD, Panessa Studios or Ace Chemicals, then back to the city
- 🟨 Invasion — starts when a player is the Invader
- ⬜ Bounty races
- ⬜ Director mode

### Enemies and combat

- ✅ Shared thugs — position, animation and health
- 🟨 Enemy-count parity in every district
- 🟨 Client-owned districts publish their enemies
- 🟨 Every enemy type:
  - Brutes
  - Medics
  - Shields
  - Blades
  - Ninjas
  - Snipers
  - Minigunners
  - Drone operators
- 🟨 Militia tanks, drones and APCs
- 🟨 Turrets and sentries
- 🟨 Every combat move and gadget displayed on every screen
- 🟨 Dual Play team takedowns
- 🟨 Predator rooms — perception, takedowns and alarms
- ⬜ Civilians and friendly NPCs everywhere

### World

- 🟨 Doors, switches, cages, winchables, destructibles and lifts
- 🟨 Puzzles and set pieces
- 🟨 Traffic and parked cars on every screen
- 🟨 Streaming and fall-through protection
- ⬜ Interior and predator-room streaming verified across every chapter

### Batmobile

- 🟨 Each player's own Batmobile
- 🟨 Driving and battle mode
- 🟨 Winch, weapons, damage and ejection on every screen
- ⬜ Mission vehicles and pursuits across every chase and tank section

### Campaign — Chapters 1–27

- 🟨 Mission stages, objectives and story beats followed by every player
- 🟨 Cutscenes held and shared
- 🟨 Checkpoints and party save
- ⬜ Every forced character switch adapted for co-op
- ⬜ Every scripted sequence adapted for co-op
- ⬜ Every boss fight playable together:
  - Firefly
  - Scarecrow
  - Man-Bat
  - Professor Pyg
  - Two-Face
  - Penguin
  - Riddler
  - Hush
  - Azrael
  - Deathstroke
  - Cloudburst
  - Arkham Knight
  - Joker finale
- ⬜ Full campaign playthrough with two players
- ⬜ Full campaign playthrough with four players
- ⬜ Knightfall and 240% completion

### Side content

- 🟨 Most Wanted missions — 14 definitions built, each mission line still to verify
- ⬜ Season of Infamy:
  - Killer Croc
  - Mr. Freeze
  - Ra's al Ghul
  - Mad Hatter
- 🟨 Riddler trophies, riddles, cages and switches
- ⬜ Riddler races and robot fights
- 🟨 AR Challenges — combat, predator and races
- 🟨 New Game Plus and Knightmare
- 🟨 Shared XP, upgrades and WayneTech

### Story DLC episodes

- ⬜ Batgirl: *A Matter of Family*
- ⬜ Harley Quinn Story Pack
- ⬜ Red Hood Story Pack
- ⬜ *Catwoman's Revenge*
- ⬜ *GCPD Lockdown* — Nightwing
- ⬜ *A Flip of a Coin* — Robin

### Product

- 🟨 In-game menus
- 🟨 Character chooser
- 🟨 Lobby settings
- 🟨 Tester package and installer
- ⬜ Ship mode — evidence logging disabled for players
- ⬜ Public release packaging

---

## Requirements (testers)

Each player currently needs:

- ***Batman: Arkham Knight*** on Steam
- Any DLC required for the characters they want to use
- **Arkham Knight Community Patch 4.6**, installed using the latest TFC Installer
- **BmSDK-AK 0.21.0**

Tester builds are distributed privately to invited testers.

---

## Legal

**Nightfall Together is an independent fan project and is not affiliated with or endorsed by Warner Bros., Rocksteady Studios, DC, Epic Games or Valve.**

Players must own a legitimate copy of *Batman: Arkham Knight* and any DLC they use.

**No game assets are distributed by this project.**
