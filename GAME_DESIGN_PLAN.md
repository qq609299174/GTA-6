# Game Design Plan

## Project Codename: Tang Frontier

> Public working title only. This project is not affiliated with Rockstar Games, Grand Theft Auto, or any related IP.

## 1. High Concept

**Tang Frontier** is a 2D / 2.5D cooperative Tang-dynasty fantasy base-defense adventure RPG.

Players begin in a ruined frontier town during a fictionalized Tang dynasty. The empire appears prosperous, but ancient seals beneath the land are weakening. Qin tombs, forgotten battlefields, corrupted waterways, and old military formations begin releasing supernatural threats. The court hides the crisis and quietly sends frontier groups to rebuild defensive settlements along unstable earth-vein boundaries.

The central fantasy is that players are not only improving individual characters. They are rebuilding, operating, defending, and evolving an entire town as a living RPG system.

## 2. Genre Definition

This is not primarily a Celeste-like platformer and not an Unreal-style large 3D game.

The intended genre is:

> **2D / 2.5D cooperative town-defense adventure RPG**

Core influences and roles:

- **Classic Warcraft III RPG defense maps**: town defense, scaling waves, role division, defense pressure, boss waves, long-session progression.
- **Brotato-style horde pressure**: dense enemy waves, build-driven combat, readable chaos, repeated pressure spikes.
- **Town-building and simulation systems**: buildings, workers, marketplace, production, storage, trade, morale, corruption, and town economy.
- **Adventure RPG progression**: quests, regions, bosses, story chapters, dungeon unlocks, equipment, research, and character growth.
- **Selected high-difficulty cooperative platform/action scenarios**: difficult synchronized sections in dungeons or special encounters, not the entire game identity.

## 3. Core Loop

The game uses a day-night structure:

```text
Day: Build, craft, trade, assign workers, gather, research, explore
Dusk: Choose defense plan, assign players, activate preparations
Night: Defend town, repair, manage crisis, complete outside objectives
Aftermath: Recover, upgrade, unlock, handle damage and consequences
```

The loop should feel strategic, stressful, and rewarding. The goal is not only to survive a wave, but to decide how the town develops and how risks are handled over multiple cycles.

## 4. Design Pillars

### 4.1 The Town Is a Living RPG Character

The town should grow like a character. It has health, capabilities, weaknesses, resources, morale, corruption, population, buildings, and long-term progression.

Buildings must not be decorative. Each major building should have:

- Construction cost
- Upgrade path
- Worker assignment
- Resource upkeep
- Production output
- Active function
- Passive benefit
- Failure consequence
- Quest or progression dependency
- Combat impact

### 4.2 Every Player Role Must Matter

Different players should be able to contribute through different styles:

- Fighting and defending
- Repairing and engineering
- Managing resources and logistics
- Operating marketplace and trade systems
- Healing and preparing supplies
- Researching enemies and technologies
- Exploring outside areas
- Completing main and side objectives

The game should avoid making combat the only meaningful activity.

### 4.3 Defense Is More Than Killing Enemies

A strong combat player should not trivialize the entire night by killing everything alone.

Night pressure should include:

- Multiple attack lanes
- Gate and wall damage
- Building-targeting enemies
- Underground breaches
- Ritual disruption
- Civilian panic
- Supply shortages
- Fire or corruption events
- Boss mechanics
- Outside objectives that affect wave strength

### 4.4 Exploration Changes the Defense Game

Leaving town must matter.

Exploration can:

- Destroy enemy sources before night
- Unlock blueprints
- Rescue NPC specialists
- Find rare resources
- Reveal enemy weaknesses
- Open trade routes
- Reduce corruption
- Trigger new threats
- Advance main and side quests

Players can split responsibilities. Some defend while others risk expeditions.

### 4.5 High-Difficulty Cooperation Should Be Earned

The game may include difficult synchronized action scenes, but they should not be simple button puzzles.

Good cooperative challenge design should require:

- Role separation
- Timing
- Mechanical execution
- Combat pressure
- Communication
- Multiple failure states
- Environmental hazards
- Recovery windows
- Meaningful rewards

## 5. Setting Premise

The Tang empire is at its height. Chang'an is wealthy and powerful. Trade flows through the Silk Road. Scholars, merchants, officials, soldiers, monks, Daoists, and travelers move through the empire.

Beneath this prosperity, old dynasties left behind sealed threats:

- Qin military tomb mechanisms
- Terracotta soldier formations
- Han battlefield spirits
- Sui-era underground works
- Corrupted waterways
- Ancient ritual sites
- Forgotten border fortifications
- Failed immortality experiments

A disturbance in the earth veins causes these old systems to awaken. The court suppresses public knowledge and sends selected groups to rebuild defensive towns along unstable regions.

The player's town begins as a ruined frontier outpost. It gradually becomes a strategic settlement holding back supernatural forces.

## 6. Main Gameplay Systems

### 6.1 Town Building

The town includes major functional buildings:

- Town Hall
- Blacksmith
- Workshop
- Marketplace
- Warehouse
- Clinic
- Academy / School
- Daoist Shrine
- Barracks / Martial Hall
- Inn
- Farm / Granary

Each building should remain relevant through active use, upgrades, staffing, damage states, and connections to combat and story progression.

### 6.2 Defense Combat

Night combat uses dense wave pressure.

Enemy waves should include:

- Horde enemies
- Shielded units
- Ranged units
- Siege units
- Infiltrators
- Ritual disruptors
- Elite commanders
- Multi-phase bosses

Players respond with:

- Character builds
- Equipment
- Consumables
- Traps
- Defensive buildings
- NPC guards
- Ritual systems
- Repairs
- Town abilities
- Outside disruption objectives

### 6.3 Economy and Simulation

The economy should not be cosmetic.

Systems include:

- Resources
- Coins
- Stockpiles
- Marketplace inventory
- NPC demand
- Merchant contracts
- Trade routes
- Caravan risk
- Town prosperity
- Morale
- Worker efficiency

A well-run economy should improve survival, upgrades, recruitment, supplies, and access to rare goods.

### 6.4 Research

Research unlocks tactical knowledge and progression.

Research categories:

- Enemy studies
- Engineering
- Ritual studies
- Trade and geography
- Combat doctrine
- Building blueprints
- Dungeon mechanism decoding

Research can reveal attack patterns, unlock counters, improve NPC performance, and enable new areas.

### 6.5 Exploration and Quests

Outside-town activities include:

- Resource expeditions
- Main story missions
- Side quests
- Rescue missions
- Caravan escort
- Dungeon challenges
- Enemy-source disruption
- Night expeditions
- Boss preparation tasks

Exploration should be directly tied to town development and defense strength.

## 7. Building Philosophy

Buildings are the backbone of the game.

A building should not become irrelevant after construction. It should continue to:

- Produce useful output
- Consume resources
- Require staffing
- Offer upgrades
- Affect night defense
- Unlock quests or tech
- Create tradeoffs
- Suffer consequences when damaged

For example:

- The blacksmith crafts weapons, repairs tools, reinforces gates, produces trap parts, and enables armor-piercing counters.
- The marketplace generates coins, satisfies NPC demand, attracts merchants, and provides emergency supplies.
- The academy researches enemy weaknesses, unlocks blueprints, forecasts attacks, and decodes mechanisms.
- The Daoist shrine manages corruption, maintains seals, weakens undead, and protects the town during supernatural events.

## 8. Player Roles

The game should support flexible roles rather than rigid MMO classes.

Possible roles:

### Frontline Defender

Blocks lanes, protects gates, holds enemies back, survives pressure.

### Duelist / Elite Killer

Targets commanders, casters, siege enemies, and boss weak points.

### Archer / Ranged Specialist

Controls walls, rooftops, and long sightlines.

### Engineer

Builds traps, repairs structures, operates machinery, creates temporary platforms.

### Daoist / Ritual Specialist

Maintains seals, controls corruption, weakens spirits, triggers barriers.

### Physician / Support

Prepares medicine, heals players and NPCs, reduces injuries and death penalties.

### Merchant / Logistician

Runs marketplace, manages supplies, prepares consumables, supports upgrades and trade.

### Explorer

Completes outside objectives, finds resources, unlocks routes, advances quests.

## 9. World Regions

Initial region structure:

1. **Ruined Frontier Town**  
   Rebuilding, first defenses, early resources, first night attacks.

2. **Lishan Qin Tomb Perimeter**  
   Terracotta soldiers, Qin mechanisms, ancient production pits, armor-piercing counters.

3. **Ancient Battlefield**  
   Ghost armies, battlefield commanders, cursed weapons, large formation mechanics.

4. **Chang'an Underground Waterways**  
   Corruption under prosperity, water gates, hidden imperial secrets, urban quests.

5. **Silk Road Outpost**  
   Trade routes, caravans, foreign materials, merchant factions, desert threats.

6. **Zhongnan Mountain**  
   Daoist rituals, spiritual systems, mountain beasts, seal truth, late-game purification.

7. **Abandoned Palace / Forbidden Archive**  
   High-level secrets, political cover-ups, late-game bosses, endgame story reveals.

## 10. Chapter Direction

### Chapter 1: Ruined Town

Focus: survival, rebuilding, basic defense, first supernatural reveal.

Key systems:

- Town Hall
- Basic walls and gate
- Blacksmith
- Workshop
- Marketplace
- Resource gathering
- First night waves

### Chapter 2: Lishan Qin Tomb

Focus: Qin tombs, terracotta soldiers, ancient mechanisms.

Key systems:

- Armor-piercing equipment
- Academy research
- Daoist shrine
- Advanced traps
- First major synchronized dungeon

### Chapter 3: Chang'an Underground

Focus: corrupted waterways and imperial secrets.

Key systems:

- Waterway quests
- Urban trade
- Intelligence
- Corruption management

### Chapter 4: Silk Road Crisis

Focus: trade routes, caravans, external economy, rare materials.

Key systems:

- Warehouse expansion
- Trade contracts
- Caravan defense
- Faction reputation

### Chapter 5: Zhongnan Mountain

Focus: Daoist seals, spiritual truth, high-difficulty challenges.

Key systems:

- Advanced ritual mechanics
- Major corruption purification
- Late-game cooperative challenge design

## 11. Prototype Target

The first prototype should not attempt the full game.

It should prove:

> A small town can be built, defended, damaged, repaired, and meaningfully improved through resource, building, combat, and exploration choices.

Prototype content:

- One town map
- One outside resource area
- One enemy route
- One optional side objective
- Basic player combat
- Three enemy types
- One elite enemy
- One mini-boss
- Three night waves
- Blacksmith
- Workshop
- Marketplace
- Town Hall
- Basic wall and gate system
- One building upgrade path
- One outside objective that affects the next night

## 12. Vertical Slice Target

After prototype validation, the vertical slice should be a polished 20-30 minute experience.

Vertical slice content:

- Opening story premise
- 2-3 day-night cycles
- 5-7 buildings
- Worker assignment
- Basic morale
- Basic corruption
- Basic marketplace
- Building damage and repair
- Two outside zones
- Three side quests
- One dungeon challenge
- One boss encounter
- First Qin-related story reveal

## 13. Technical Direction

Recommended engine: **Godot**.

Initial systems:

- Player controller
- Combat and damage system
- Enemy AI
- Wave manager
- Building manager
- Resource inventory
- Town state manager
- Day-night cycle
- Quest manager
- NPC worker assignment
- Save/load
- Interaction system
- Building UI
- Marketplace UI
- Debug tools for balancing waves and building output

## 14. Development Milestones

### Milestone 1: Core Sandbox

- Player movement
- Town map
- Resource nodes
- Inventory
- Basic interaction
- Placeholder UI

### Milestone 2: First Night Defense

- Day-night cycle
- Enemy spawns
- Gate health
- Player combat
- Wave completion
- Rewards

### Milestone 3: Building Systems

- Blacksmith
- Workshop
- Marketplace
- Building damage
- Repairs
- Upgrade costs

### Milestone 4: Exploration Loop

- Outside zone
- Quest objective
- Resource expedition
- Return rewards
- Reward affects town progression

### Milestone 5: Town Management

- NPC workers
- Morale
- Storage
- Basic corruption
- Staffing
- Upgrade dependencies

### Milestone 6: Cooperative Challenge Prototype

- One dungeon challenge
- Split routes
- Timed mechanics
- Combat pressure
- Shared objective
- Reward tied to town progression

### Milestone 7: Vertical Slice

- Polished 20-30 minute demo
- Opening sequence
- Boss encounter
- Core economy
- Building damage and repair
- First story reveal

## 15. Early Content Priorities

Prioritize:

1. Movement and interaction
2. Combat readability
3. Day-night loop
4. Enemy waves
5. Building damage and repair
6. Resource economy
7. Marketplace usefulness
8. Exploration objective
9. Worker assignment
10. Story presentation
11. Advanced synchronized challenges

Avoid early overinvestment in:

- Large world map
- Too many classes
- Too many buildings
- Full procedural generation
- Full story writing
- Advanced networking before the core loop works
- Cosmetic decoration before building gameplay is meaningful

## 16. Summary

Tang Frontier should be designed around the following promise:

> Build the town. Defend the night. Explore the truth beneath the empire.

The project succeeds if the town feels worth protecting, buildings feel alive, players have meaningful roles beyond combat, and exploration meaningfully changes how the next defense plays out.
