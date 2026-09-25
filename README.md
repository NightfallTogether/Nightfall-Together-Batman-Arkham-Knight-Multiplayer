<img width="1899" height="1056" alt="NT_1" src="https://github.com/user-attachments/assets/9db06757-cb90-4ce8-9e34-84eba29f47b7" />
# Nightfall Together #

**Online co-op for *Batman: Arkham Knight* (Steam, PC).** Two to four players
share one Gotham: the same enemies, the same fights, the same world and the
same story, each playing as the character they choose.

> Status: **active development, playable with testers.** Most systems are
> built and many are verified on two PCs; the full campaign is not yet
> playable start to finish together. See the [completion checklist](#completion-checklist).

This page describes the project. The source code is private, and no files are
distributed here. You need your own copy of the game and any DLC you want to
use.

---
<img width="1834" height="999" alt="NT_2" src="https://github.com/user-attachments/assets/c851fcad-908e-4aa4-a71f-60d462446321" />

## What it does today

### Playing together
- **Steam lobbies and invites.** Host from the in-game menu and invite
  friends, or join a friend's lobby. Late joiners catch up to the world as it
  is (world state is rebuilt from a baseline plus the events since).
- **Up to four players** in one open-world Gotham, each on their own body.
- **Join Teammate** on the pause menu moves you next to a teammate (or into
  their area if they are elsewhere).
- **Team HUD:** a roster with each player's character, health and status
  (downed, paused, AFK, in a vehicle), name tags over teammates, compass and
  city-map markers, and pings.
- **Proximity voice chat.**
- **Collective pause:** the world only stops when everyone is paused; a paused
  or AFK player is protected.
- **Host lobby settings,** including enemy count scaling (1x-3x).

### Characters
- **Playable roster:** Batman, Robin, Nightwing, Catwoman, Azrael, Batgirl,
  Red Hood, Harley Quinn, Joker and Deathstroke, plus the stand-in villains
  **Scarecrow, Two-Face, Professor Pyg, Penguin and Riddler** (built on a
  compatible body with borrowed animation sets).
- Switch character from the in-game chooser at any time; every other player
  sees your character's look, moves and colour.
- Every character is kept at Batman parity where possible: glide (or an
  equivalent), grapple, counters, takedowns, gadgets, detective mode.
- Players who lack a character's DLC see a stand-in instead of a broken body.

### Combat and stealth
- **Shared enemies:** the host runs the enemy population; everyone sees the
  same thugs in the same places, animating and fighting the same way. A
  player who owns a district simulates its enemies for everyone.
- Punches, counters, takedowns (including Dual Play team takedowns), beatdowns
  and knockouts land on the same body on every screen.
- **Gadgets** show on every screen: batarangs, explosive gel, batclaw,
  REC, freeze, smoke, line launcher and more.
- Enemy gunfire, brutes, medics, shields, ninjas, drones, tanks and APCs.
- **Predator rooms:** guards see and hear every player; takedowns, alarms and
  fear are shared.
- **Downed and revive:** a downed player can be revived by a teammate;
  enemies leave a downed player alone.
- **Bosses** have shared health and finishes.

### World and traversal
- Every player's movement is interpolated and predicted, including gliding,
  grappling, diving, vents, ladders, ledges and cover, with capes and head
  look shown on other screens.
- Doors, switches, cages, winchable walls, destructibles, lifts and puzzles
  stay in sync.
- **Batmobile:** everyone gets their own car; driving, battle mode, winch,
  weapons and damage are shown on every screen. Traffic and enemy vehicles
  are shared.
- **Fall recovery:** a player who falls through unloaded ground is put back on
  solid ground.

### Progression and side content
- **Missions:** the host drives the story; objectives, mission picks and
  Most Wanted lines are followed by every player.
- **XP and upgrades** are shared by the party.
- **Riddler:** trophies, riddles, cages and switches count for the party.
- **AR challenges** can be played together.
- **New Game Plus and Knightmare** follow the host's difficulty.
- **Your own save is never overwritten** by a co-op session; party progress is
  kept in the mod's own save sidecar.

---

## Goal

**The full shipped single-player game, played by two to four people at once,
with every entity in sync and every playable character at Batman parity.**
"In sync" means fully wired end to end, with interpolation and prediction
wherever a real multiplayer game would use them - not "roughly the same".

The finish line, in order:

1. Two, then three, then four players complete the campaign (chapters 1-27 to
   Knightfall) with no blocking desync.
2. Every entity a player can see is synced: every enemy type, turrets, every
   boss, friendly NPCs, civilians, traffic, world objects and set pieces.
3. Enemy count, position, animation, target and health match on every screen.
4. Every playable character can reach every objective.
5. All Most Wanted, Season of Infamy, story DLC, Riddler, AR, New Game Plus and
   Knightmare content is playable together.
6. Robust sessions: reconnect, host migration, join at any point, 4-hour play.
7. A finished product: menus, installer, privacy and release packaging.

---
<img width="2560" height="1440" alt="NT_4" src="https://github.com/user-attachments/assets/04594b83-557a-48f5-9159-88387325641c" />
## Completion checklist

Legend: ✅ working and verified on two PCs · 🟨 built, awaiting two-PC
verification · ⬜ not done yet.

This list covers finishing the base game and its DLC together. It does not
include new features.

### Foundation
- ✅ Steam lobby, invites, join and admission
- ✅ Late join (baseline + event tail)
- ✅ Network transport, rate limits, session integrity
- 🟨 Reconnect with every system restored
- ⬜ Host migration (host leaves, session continues)
- ⬜ Three- and four-player sessions verified
- ⬜ 4-hour soak test inside budget

### Players and characters
- ✅ Player movement, interpolation and traversal on every screen
- 🟨 Head look, capes, glide and grapple presentation
- 🟨 Every character switch shows correctly on every screen
- 🟨 Every character at Batman parity (traversal, combat, gadgets)
- 🟨 Stand-in villains (Scarecrow, Two-Face, Pyg, Penguin, Riddler) in game
- 🟨 Downed, revive, death floor and respawn
- ✅ Team HUD, name tags, compass and map markers
- 🟨 Proximity voice chat

### Enemies and combat
- ✅ Shared thugs: position, animation, health
- 🟨 Enemy count parity per district on every screen
- 🟨 Client-owned districts publish their enemies
- 🟨 Every enemy type: brutes, medics, shields, blades, ninjas, snipers,
  minigunners, drone operators
- 🟨 Militia tanks, drones and APCs
- 🟨 Turrets and sentries
- 🟨 Every combat move and gadget shown on every screen
- 🟨 Dual Play team takedowns
- 🟨 Predator rooms: perception, takedowns, alarms
- ⬜ Civilians and friendly NPCs everywhere

### World
- 🟨 Doors, switches, cages, winchables, destructibles, lifts
- 🟨 Puzzles and set pieces
- 🟨 Traffic and parked cars on every screen
- 🟨 Streaming and fall-through protection
- ⬜ Interior and predator-room streaming verified across every chapter

### Batmobile
- 🟨 Each player's own Batmobile, driving and battle mode
- 🟨 Winch, weapons, damage and ejection on every screen
- ⬜ Mission vehicles and pursuits (every chase and tank section)

### Campaign (chapters 1-27)
- 🟨 Mission stages, objectives and story beats followed by every player
- 🟨 Cutscenes held and shared
- 🟨 Checkpoints and the party save
- ⬜ Every forced character switch and scripted sequence adapted for co-op
- ⬜ Every boss fight together: Firefly, Scarecrow, Man-Bat, Pyg, Two-Face,
  Penguin, Riddler, Hush, Azrael, Deathstroke, Cloudburst, Arkham Knight,
  Joker finale
- ⬜ Full campaign playthrough with 2 players, then 4
- ⬜ Knightfall and 240% completion

### Side content
- 🟨 Most Wanted missions (14) - definitions built, each line to verify
- ⬜ Season of Infamy (4): Killer Croc, Mr. Freeze, Ra's al Ghul, Mad Hatter
- 🟨 Riddler: trophies, riddles, cages, switches
- ⬜ Riddler races and robot fights
- 🟨 AR challenges (combat, predator, races)
- 🟨 New Game Plus and Knightmare
- 🟨 XP, upgrades and WayneTech shared

### Story DLC episodes (6)
- ⬜ Batgirl: A Matter of Family
- ⬜ Harley Quinn Story Pack
- ⬜ Red Hood Story Pack
- ⬜ Catwoman's Revenge
- ⬜ GCPD Lockdown (Nightwing)
- ⬜ A Flip of a Coin (Robin)

### Product
- 🟨 In-game menus, character chooser and lobby settings
- 🟨 Tester package and installer
- ⬜ Ship mode (evidence logging off for players)
- ⬜ Public release packaging

<img width="1877" height="1048" alt="NT_3" src="https://github.com/user-attachments/assets/2e25610d-c8dd-4b20-9231-193e0ce68793" />

---

## Requirements (testers)

Each player needs:

- *Batman: Arkham Knight* on Steam (and any DLC characters they want to use)
- **Arkham Knight Community Patch 4.6**, installed with the latest TFC Installer
- **BmSDK-AK 0.21.0**

Tester builds are shared privately with invited testers.

## Legal

This project is unaffiliated with Warner Bros., Rocksteady, Epic Games, Valve
or DC. Players must own a legitimate copy of the game and any DLC they use. No
game assets are distributed.
