# Prototype Scope

## Purpose

The first prototype should prove the smallest playable version of Tang Frontier's core identity.

The prototype should not attempt to become the full game. It should answer one question:

> Is the loop of building a town, preparing defenses, surviving a night attack, and using exploration rewards to improve the next defense actually fun?

If this loop is not fun at small scale, adding more regions, story, buildings, classes, or multiplayer complexity will not fix the project.

## Prototype Design Goal

Create a small but complete playable loop:

```text
Gather resources -> Build or upgrade town systems -> Prepare defense -> Survive night attack -> Complete one outside objective -> Unlock one meaningful upgrade
```

The prototype should be playable in roughly 10-15 minutes.

## Prototype Scope Rules

### Keep It Small

Do not build the full world. Do not build all buildings. Do not build all classes. Do not build a large story campaign.

### Make Buildings Matter

At least one building choice must clearly affect night defense.

### Make Night Pressure Real

The night attack should involve more than enemies walking into the player. The gate, building damage, repairs, or side objectives must matter.

### Include One Outside Objective

The prototype must prove that leaving town can change the next defense.

### Use Placeholder Art

Use placeholder sprites, colored blocks, debug UI, and simple effects until the loop works.

## Prototype Content

## 1. Map

One small town map.

Required spaces:

- Town center
- Main gate
- Short wall section
- Blacksmith location
- Workshop location
- Marketplace location
- Storage area
- Outside resource area
- One enemy spawn path
- One optional side path

The map should be small enough that players can understand it quickly but large enough to create movement pressure during night.

## 2. Player

Minimum player capabilities:

- Move
- Attack
- Interact
- Gather resource
- Repair structure
- Use consumable
- Open simple building UI

Optional later capabilities:

- Dash or dodge
- Secondary attack
- Tool use
- Role-specific skill

## 3. Resources

Minimum resource types:

- Wood
- Stone
- Iron
- Food
- Coins

Optional prototype resource:

- Ritual fragments or corruption crystals

## 4. Buildings

The prototype should include only a few buildings, but each should matter.

### Town Hall

Purpose:

- Central state tracker
- Basic construction unlock
- Town health and morale display

Prototype functions:

- Shows town status
- Enables basic building upgrades
- Can trigger one emergency order if implemented

### Gate / Wall

Purpose:

- Main defense object
- If it falls, enemies enter town more easily

Prototype functions:

- Has health
- Can be repaired
- Can be reinforced
- Can be damaged by enemies

### Blacksmith

Purpose:

- Combat and defense upgrade building

Prototype functions:

- Upgrade player damage or weapon quality
- Reinforce gate
- Produce temporary armor-piercing or damage buff

### Workshop

Purpose:

- Repair and trap building

Prototype functions:

- Produce repair kits
- Build one simple trap
- Improve repair speed

### Marketplace

Purpose:

- Economy building

Prototype functions:

- Sell surplus resources for coins
- Generate passive coin if stocked with goods
- Provide emergency supplies if stocked before night

## 5. Enemies

Prototype enemy types:

### Basic Raider / Spirit

- Low health
- Attacks player or gate
- Teaches basic combat

### Shielded Enemy

- More health
- Takes reduced frontal damage or has armor
- Encourages weapon upgrade or flanking

### Siege Enemy

- Slowly moves toward gate or building
- Deals high structure damage
- Must be prioritized

### Elite Enemy

- Appears near final wave
- Higher health
- May buff nearby units or target buildings

### Mini-Boss

- Final enemy of prototype
- Tests whether players understand combat, repairs, and building preparation

## 6. Night Waves

The prototype should contain three waves.

### Wave 1: Introduction

- Basic enemies only
- Attacks main gate
- Teaches fighting and gate defense

### Wave 2: Pressure Split

- Basic enemies plus one shielded or siege enemy
- Player must decide whether to fight or repair

### Wave 3: Mini-Boss

- Mixed enemies
- One mini-boss
- Gate and building damage matter
- Traps or blacksmith upgrade should noticeably help

## 7. Outside Objective

The prototype should include one optional outside objective.

Example:

> Destroy a small enemy altar before night starts or during early night.

Effects:

- Reduces final wave enemy count
- Delays mini-boss spawn
- Provides rare material for Blacksmith upgrade
- Reduces corruption gain

The outside objective proves that exploration affects defense.

## 8. Economy Prototype

The economy should be simple but meaningful.

Minimum system:

- Gather resources
- Store resources
- Sell surplus goods at Marketplace
- Use coins for building upgrades
- Stock Marketplace before night to unlock emergency supply ability

Example:

- Sell food or wood for coins
- Use coins and iron to upgrade Blacksmith
- Blacksmith upgrade improves combat damage
- Combat improvement helps survive final wave

## 9. Building Damage Prototype

At least one building should be damageable.

Minimum implementation:

- Gate has health
- Workshop or Marketplace can be targeted by one enemy type
- Damaged building has reduced function
- Player can repair using wood or repair kit

Example:

- If Workshop is damaged, repair speed decreases.
- If Marketplace is damaged, emergency supply cannot be used.
- If Blacksmith is damaged, weapon buff is unavailable.

## 10. Progression Prototype

The prototype should include one clear progression path.

Example progression:

1. Gather wood and iron.
2. Build Blacksmith.
3. Use Blacksmith to reinforce gate or improve weapon.
4. Survive night more effectively.
5. Defeat mini-boss.
6. Unlock blueprint hint for next system.

## 11. Win and Lose Conditions

### Win Condition

Survive all three waves and defeat the mini-boss.

### Lose Conditions

Potential prototype options:

- Town Hall destroyed
- Gate destroyed and too many enemies enter town
- All players defeated
- Corruption reaches maximum

For the first prototype, keep lose conditions simple.

Recommended first lose condition:

> Town health reaches zero.

## 12. Prototype UI

Minimum UI:

- Player health
- Resource counts
- Town health
- Gate health
- Day/night timer
- Wave indicator
- Building interaction panel
- Simple upgrade button
- Repair prompt

Debug UI should be acceptable during early development.

## 13. Prototype Success Criteria

The prototype is successful if:

- The player understands what to do within 1-2 minutes.
- Building choices affect night defense.
- Combat feels readable enough to continue tuning.
- Repairing and defending feel meaningfully different.
- Marketplace or resource economy has a real purpose.
- The outside objective changes the night outcome.
- The player wants to play another cycle.

## 14. What Not To Build Yet

Do not build these in the first prototype:

- Full multiplayer networking
- Full chapter story
- Large world map
- Many classes
- Complex NPC schedules
- Deep procedural generation
- Advanced pathfinding for dozens of enemy types
- Full inventory UI
- Full building placement system
- Cosmetic decoration
- Final art
- Final music

## 15. Recommended Prototype Development Order

1. Create small town map.
2. Add player movement and attack.
3. Add enemy that walks toward gate.
4. Add gate health and repair.
5. Add day-night timer.
6. Add three enemy waves.
7. Add resource gathering.
8. Add Blacksmith upgrade.
9. Add Workshop repair kit or trap.
10. Add Marketplace coin conversion.
11. Add one outside objective.
12. Add mini-boss.
13. Tune loop until it feels like a complete 10-15 minute experience.

## 16. Prototype Summary

The prototype should prove this promise:

> The town is worth protecting, buildings matter, night defense creates pressure, and exploration changes the next fight.
