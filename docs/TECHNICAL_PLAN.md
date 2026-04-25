# Technical Plan

## Purpose

This document defines the initial technical direction for building a playable prototype of Tang Frontier.

The technical goal is not to build every long-term system immediately. The first priority is to create a small, testable foundation that proves the core loop:

```text
Town preparation -> Night defense -> Damage and recovery -> Outside objective -> Upgrade
```

## Recommended Engine

### Godot

Godot is recommended for the first prototype because the project is primarily 2D / 2.5D and benefits from fast iteration.

Reasons:

- Strong 2D workflow
- TileMap support
- Lightweight project structure
- Good for small-team iteration
- Easy scripting with GDScript
- Suitable for UI-heavy simulation systems
- Suitable for action combat prototypes
- Easier to keep scope controlled than a large 3D engine workflow

## Initial Technical Philosophy

### Build Systems Before Content

The project should first implement reusable systems rather than hardcoding one-off scenes.

Examples:

- A generic building component is better than one hardcoded Blacksmith scene.
- A generic wave manager is better than one scripted enemy spawn sequence.
- A reusable resource inventory is better than separate counters in each building.

### Keep the Prototype Data-Driven

Whenever practical, prototype data should be stored in simple resource files or dictionaries so values can be tuned quickly.

Examples:

- Enemy health
- Wave composition
- Building cost
- Upgrade cost
- Repair cost
- Resource output
- Night duration
- Damage values

### Use Placeholder Art

Do not block progress on final art.

Acceptable early visuals:

- Colored rectangles
- Simple sprite placeholders
- Debug icons
- Temporary UI panels
- Basic tiles
- Simple effects

The first milestone is fun and clarity, not visual polish.

## Recommended Project Structure

```text
project/
├── scenes/
│   ├── main/
│   │   └── Main.tscn
│   ├── player/
│   │   └── Player.tscn
│   ├── enemies/
│   │   ├── BasicEnemy.tscn
│   │   ├── ShieldEnemy.tscn
│   │   ├── SiegeEnemy.tscn
│   │   └── MiniBoss.tscn
│   ├── buildings/
│   │   ├── BuildingBase.tscn
│   │   ├── TownHall.tscn
│   │   ├── Gate.tscn
│   │   ├── Blacksmith.tscn
│   │   ├── Workshop.tscn
│   │   └── Marketplace.tscn
│   ├── world/
│   │   ├── TownMap.tscn
│   │   └── OutsideArea.tscn
│   └── ui/
│       ├── HUD.tscn
│       ├── BuildingPanel.tscn
│       └── ResourcePanel.tscn
├── scripts/
│   ├── core/
│   │   ├── GameState.gd
│   │   ├── DayNightManager.gd
│   │   ├── ResourceManager.gd
│   │   ├── TownState.gd
│   │   └── SaveManager.gd
│   ├── combat/
│   │   ├── HealthComponent.gd
│   │   ├── Hitbox.gd
│   │   ├── Hurtbox.gd
│   │   └── DamageTypes.gd
│   ├── player/
│   │   └── PlayerController.gd
│   ├── enemies/
│   │   ├── EnemyBase.gd
│   │   ├── EnemyAI.gd
│   │   └── WaveManager.gd
│   ├── buildings/
│   │   ├── BuildingBase.gd
│   │   ├── BuildingManager.gd
│   │   ├── Gate.gd
│   │   ├── Blacksmith.gd
│   │   ├── Workshop.gd
│   │   └── Marketplace.gd
│   ├── quests/
│   │   ├── QuestManager.gd
│   │   └── Objective.gd
│   └── ui/
│       ├── HUD.gd
│       └── BuildingPanel.gd
├── data/
│   ├── buildings/
│   ├── enemies/
│   ├── waves/
│   ├── resources/
│   └── upgrades/
└── docs/
```

## Core Systems

## 1. Game State Manager

### Purpose

Controls the current phase of the game.

Possible states:

- Boot
- Main Menu
- Day
- Dusk
- Night
- Aftermath
- Game Over

### Responsibilities

- Track current phase
- Notify systems when phase changes
- Control transition timing
- Enable or disable actions by phase
- Coordinate save points

## 2. Day-Night Manager

### Purpose

Controls the cycle between preparation and defense.

### Responsibilities

- Track day timer
- Track dusk preparation timer
- Start night waves
- End night when waves are cleared
- Trigger aftermath processing
- Increase day count

### Prototype Values

- Day length: 3-5 minutes
- Dusk length: 30-60 seconds
- Night length: wave-driven
- Prototype total run: 10-15 minutes

## 3. Resource Manager

### Purpose

Tracks town-wide resources.

### Initial Resources

- Wood
- Stone
- Iron
- Food
- Coins

### Responsibilities

- Add resources
- Spend resources
- Validate upgrade costs
- Update UI
- Support building production and consumption

## 4. Town State

### Purpose

Tracks overall town health and strategic state.

### Initial Properties

- Town health
- Gate health
- Morale
- Corruption
- Population
- Day count
- Current threat level

### Prototype Simplification

The first prototype can start with:

- Town health
- Gate health
- Day count
- Threat level

Morale and corruption can be added after the base loop works.

## 5. Player Controller

### Minimum Features

- Movement
- Attack
- Interact
- Gather
- Repair
- Use item

### Later Features

- Dash or dodge
- Skill system
- Class-specific actions
- Tool system
- Build-specific modifiers

## 6. Combat System

### Components

- HealthComponent
- Hitbox
- Hurtbox
- Damage data
- Knockback
- Enemy targeting
- Structure damage

### Damage Targets

- Players
- Enemies
- Buildings
- Gates
- NPCs later

### Damage Types

Initial prototype:

- Physical
- Structure

Later:

- Fire
- Poison
- Spirit
- Armor-piercing
- Ritual
- Corruption

## 7. Enemy AI

### Basic Enemy Behavior

- Spawn at defined point
- Move toward target
- Attack player if nearby
- Attack gate or building if assigned
- Die and drop reward

### Initial Enemy Types

1. Basic Enemy
2. Shield Enemy
3. Siege Enemy
4. Elite Enemy
5. Mini-Boss

### Targeting Modes

- Player-seeking
- Gate-seeking
- Building-seeking
- Ritual-point-seeking later

## 8. Wave Manager

### Purpose

Controls night enemy attacks.

### Responsibilities

- Read wave data
- Spawn enemies
- Track active enemies
- Trigger next wave
- End night when complete
- Trigger special events

### Prototype Wave Data Example

```text
Wave 1:
- 8 Basic Enemies

Wave 2:
- 10 Basic Enemies
- 2 Shield Enemies
- 1 Siege Enemy

Wave 3:
- 12 Basic Enemies
- 2 Shield Enemies
- 1 Elite Enemy
- 1 Mini-Boss
```

## 9. Building System

### BuildingBase Responsibilities

- Building ID
- Display name
- Health
- Max health
- State
- Level
- Staff count later
- Resource cost
- Upgrade data
- Active ability
- Damage behavior

### Initial Building States

- Operational
- Damaged
- Disabled
- Upgrading

### Required Prototype Buildings

- Town Hall
- Gate
- Blacksmith
- Workshop
- Marketplace

## 10. Building Manager

### Purpose

Tracks all town buildings.

### Responsibilities

- Register buildings
- Query building states
- Apply global building effects
- Handle repairs and upgrades
- Notify UI of changes
- Handle night damage consequences

## 11. Building UI

### Required UI Functions

- Show building name
- Show health
- Show level
- Show upgrade cost
- Show active ability
- Show repair option
- Show production or stock status

Prototype UI can be simple but must support fast iteration.

## 12. Quest and Objective System

### Prototype Need

The first prototype needs one outside objective.

Example:

- Destroy enemy altar
- Reward: reduce final wave count or delay mini-boss

### Objective Types

- Kill target
- Destroy object
- Gather item
- Escort NPC later
- Repair object
- Survive timer
- Activate mechanism

## 13. Save / Load

Save/load is not mandatory for the first 10-minute prototype.

However, design should prepare for it by keeping state centralized:

- Resources in ResourceManager
- Buildings in BuildingManager
- Town values in TownState
- Quests in QuestManager
- Phase in GameState

## Data Design

## Building Data Example

```json
{
  "id": "blacksmith",
  "name": "Blacksmith",
  "max_health": 100,
  "build_cost": {
    "wood": 20,
    "stone": 10,
    "iron": 5
  },
  "upgrade_cost": {
    "wood": 30,
    "iron": 15,
    "coins": 20
  },
  "active_ability": "weapon_tempering",
  "passive_effect": "player_damage_bonus"
}
```

## Enemy Data Example

```json
{
  "id": "siege_enemy",
  "name": "Siege Enemy",
  "health": 80,
  "speed": 45,
  "damage": 12,
  "structure_damage": 25,
  "target_priority": "gate"
}
```

## Wave Data Example

```json
{
  "wave_id": 1,
  "spawns": [
    { "enemy": "basic_enemy", "count": 8, "interval": 1.0 }
  ]
}
```

## Development Order

## Phase 1: Empty Playable Map

- Create Godot project
- Create town map
- Add player
- Add camera
- Add collision
- Add simple interaction prompt

## Phase 2: Combat Foundation

- Add attack
- Add enemy
- Add health component
- Add damage
- Add enemy death

## Phase 3: Gate Defense

- Add gate
- Add gate health
- Enemy targets gate
- Player repairs gate
- Gate damage shows in UI

## Phase 4: Wave Manager

- Add night state
- Spawn Wave 1
- Spawn Wave 2
- Spawn Wave 3
- End night after enemies defeated

## Phase 5: Resource Loop

- Add resource nodes
- Add gathering
- Add resource UI
- Add spend validation

## Phase 6: Buildings

- Add Blacksmith
- Add Workshop
- Add Marketplace
- Add building interaction UI
- Add one upgrade per building

## Phase 7: Outside Objective

- Add outside area
- Add enemy altar
- Add objective tracker
- Destroying altar affects Wave 3

## Phase 8: Mini-Boss and Tuning

- Add mini-boss
- Tune enemy counts
- Tune repairs
- Tune resource cost
- Tune day-night pacing

## Phase 9: Prototype Polish

- Add simple title screen
- Add restart flow
- Add clearer UI
- Add basic sound placeholders
- Add simple visual feedback

## Debug Tools

The project should include debug tools early.

Useful debug actions:

- Add resources
- Start night immediately
- End night immediately
- Spawn enemy type
- Damage gate
- Repair all buildings
- Toggle outside objective complete
- Increase or decrease threat level

Debug tools make balancing much faster.

## Multiplayer Note

Do not implement full online multiplayer before the single-machine prototype loop works.

Early cooperative design can be tested with:

- Local simulation
- AI stand-ins
- Controller support later
- Debug role switching
- Simplified split objectives

Full networking should be postponed until the core loop proves fun.

## Immediate Implementation Backlog

1. Create Godot project.
2. Build small town map.
3. Implement player movement and attack.
4. Implement health and damage components.
5. Implement one enemy that attacks the gate.
6. Implement gate health and repair.
7. Implement day-night manager.
8. Implement wave manager.
9. Implement resource gathering.
10. Implement Blacksmith upgrade.
11. Implement Workshop repair kit.
12. Implement Marketplace coin conversion.
13. Implement outside altar objective.
14. Implement mini-boss wave.
15. Tune the 10-15 minute prototype.

## Technical Success Criteria

The technical prototype succeeds if:

- A player can complete a full day-night cycle.
- Buildings can be interacted with and upgraded.
- Enemies can damage town structures.
- The player can repair structures.
- Resources are gathered and spent.
- One outside objective affects night combat.
- The code structure can support adding more buildings and enemies without rewriting the entire project.
