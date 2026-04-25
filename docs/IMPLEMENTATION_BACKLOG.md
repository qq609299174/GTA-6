# Implementation Backlog

## Purpose

This backlog breaks the design plan into executable implementation tasks.

The immediate goal is not to build the full game. The first goal is to create a small playable prototype that proves the core loop:

```text
Gather -> Build -> Prepare -> Defend -> Repair -> Explore -> Upgrade
```

## Backlog Priority Levels

### P0: Required for First Playable Prototype

These tasks are required before the project can be considered playable.

### P1: Required for Strong Prototype

These tasks make the prototype feel like the intended game instead of a raw combat test.

### P2: Vertical Slice Expansion

These tasks should wait until the core loop works.

---

# P0: First Playable Prototype

## 1. Godot Project Setup

### Goal

Create a clean Godot project foundation.

### Tasks

- Create Godot project.
- Add basic folder structure.
- Add main scene.
- Add placeholder town map.
- Add player scene.
- Add simple camera follow.
- Add collision layers and masks.
- Add debug input actions.

### Done When

The player can move around a small town map with collision.

---

## 2. Player Movement and Interaction

### Goal

Implement a basic controllable player.

### Tasks

- Move in 2D / 2.5D space.
- Add basic attack.
- Add interact button.
- Add simple gathering action.
- Add repair action.
- Add health.
- Add damage feedback.

### Done When

The player can move, attack enemies, interact with buildings, gather a resource, and repair a structure.

---

## 3. Health and Damage System

### Goal

Create reusable health and damage components.

### Tasks

- Implement `HealthComponent`.
- Implement damage events.
- Support player damage.
- Support enemy damage.
- Support building/gate damage.
- Add death / disabled events.

### Done When

Players, enemies, and buildings can all take damage through the same basic system.

---

## 4. Gate Defense System

### Goal

Create the first meaningful defense object.

### Tasks

- Add gate scene.
- Add gate health.
- Add gate damage UI.
- Allow enemies to target gate.
- Allow player to repair gate using wood.
- Add gate destroyed state.

### Done When

Enemies can attack the gate, the player can repair it, and losing the gate creates a clear danger.

---

## 5. Enemy Foundation

### Goal

Create simple enemies for prototype waves.

### Tasks

- Implement `EnemyBase`.
- Add basic pathing toward target.
- Add attack behavior.
- Add death behavior.
- Add drops or reward hook.
- Create Basic Enemy.
- Create Siege Enemy.
- Create Shield Enemy.

### Done When

Enemies spawn, move toward targets, attack, die, and affect the defense.

---

## 6. Day-Night Cycle

### Goal

Implement the main phase structure.

### Tasks

- Add Day phase.
- Add Dusk phase.
- Add Night phase.
- Add Aftermath phase.
- Add timer UI.
- Lock or unlock actions by phase.

### Done When

The game can transition from day preparation into night defense and then into aftermath.

---

## 7. Wave Manager

### Goal

Spawn enemy waves during night.

### Tasks

- Create `WaveManager`.
- Define three waves.
- Spawn enemies from spawn points.
- Track active enemies.
- Trigger next wave.
- End night when all waves are complete.

### Done When

A full night attack can start, progress through three waves, and end correctly.

---

## 8. Resource System

### Goal

Add simple resources needed for building and repair.

### Tasks

- Implement `ResourceManager`.
- Add wood.
- Add stone.
- Add iron.
- Add food.
- Add coins.
- Add resource UI.
- Add simple resource nodes.
- Allow resource spending.

### Done When

The player can gather resources and spend them on repairs or upgrades.

---

## 9. Basic Building System

### Goal

Create reusable building infrastructure.

### Tasks

- Implement `BuildingBase`.
- Add building health.
- Add building levels.
- Add repair behavior.
- Add upgrade cost.
- Add interaction panel.
- Add operational / damaged / disabled states.

### Done When

A building can be interacted with, damaged, repaired, and upgraded.

---

## 10. Blacksmith Prototype

### Goal

Make the first combat-impacting building.

### Tasks

- Create Blacksmith scene.
- Add upgrade option.
- Add weapon damage buff.
- Add gate reinforcement option.
- Add simple resource cost.

### Done When

Using the Blacksmith clearly makes night defense easier.

---

## 11. Workshop Prototype

### Goal

Make the first repair / engineering building.

### Tasks

- Create Workshop scene.
- Add repair kit generation.
- Add one basic trap or barricade.
- Add repair speed bonus.
- Add damaged state consequences.

### Done When

The Workshop helps the player survive through repairs, traps, or emergency structure support.

---

## 12. Marketplace Prototype

### Goal

Make economy matter in the prototype.

### Tasks

- Create Marketplace scene.
- Allow selling surplus resources for coins.
- Add simple stock system.
- Add emergency supply active ability.
- Add coin spending for upgrades.

### Done When

The Marketplace gives the player a reason to manage resources beyond direct crafting.

---

## 13. Outside Objective

### Goal

Prove that exploration affects defense.

### Tasks

- Add small outside area.
- Add enemy altar objective.
- Add objective tracker.
- Allow player to destroy altar.
- If altar is destroyed, reduce final wave pressure.

### Done When

Completing the outside objective changes the night outcome.

---

## 14. Mini-Boss

### Goal

End the prototype with a meaningful pressure test.

### Tasks

- Add mini-boss enemy.
- Give mini-boss structure damage or special attack.
- Spawn mini-boss in final wave.
- Add defeat reward.
- Add victory condition.

### Done When

The prototype has a clear final challenge and win condition.

---

# P1: Strong Prototype

## 15. Building Damage Consequences

### Goal

Make building damage matter beyond visuals.

### Tasks

- Blacksmith damaged: weapon buff disabled.
- Workshop damaged: repairs slower.
- Marketplace damaged: emergency supplies unavailable.
- Gate destroyed: enemies enter town faster or town health drops.

### Done When

Players care about protecting buildings during night.

---

## 16. Town Health and Morale Lite

### Goal

Add a simple town-level failure pressure.

### Tasks

- Add town health.
- Reduce town health when enemies breach.
- Add simple morale value.
- Increase morale after successful defense.
- Reduce morale after heavy damage.

### Done When

The town has a visible strategic state beyond individual building health.

---

## 17. Simple NPC Worker System

### Goal

Make buildings feel operated rather than static.

### Tasks

- Add worker count per building.
- Allow assigning workers.
- Worker improves production or repair speed.
- Add simple worker UI.

### Done When

Assigning workers changes building output.

---

## 18. Basic Corruption System

### Goal

Introduce supernatural long-term pressure.

### Tasks

- Add corruption meter.
- Increase corruption if enemies breach or altar survives.
- Corruption increases enemy strength or wave count.
- Add simple purification reward.

### Done When

Ignoring supernatural objectives makes later nights harder.

---

## 19. Quest System

### Goal

Support repeatable objective logic.

### Tasks

- Create `QuestManager`.
- Add objective types: destroy, gather, survive, repair.
- Add quest UI.
- Add rewards.

### Done When

The outside altar objective is driven by a reusable quest/objective system.

---

## 20. Better Combat Feedback

### Goal

Make combat readable.

### Tasks

- Add hit flash.
- Add damage numbers or simple feedback.
- Add enemy attack telegraph.
- Add structure damage effect.
- Add death effect.

### Done When

Players can clearly read hits, danger, enemy death, and structure damage.

---

# P2: Vertical Slice Expansion

## 21. First Qin Enemy Set

### Goal

Introduce the first major thematic enemy group.

### Tasks

- Terracotta infantry.
- Qin crossbow enemy.
- Armored terracotta guard.
- Qin formation commander.
- Qin visual placeholders.

---

## 22. Academy Research System

### Goal

Add knowledge progression.

### Tasks

- Create Academy building.
- Add research UI.
- Add enemy weakness research.
- Add blueprint unlock.
- Add night forecast ability.

---

## 23. Daoist Shrine and Corruption Control

### Goal

Make supernatural defense a real town system.

### Tasks

- Create Daoist Shrine.
- Add town barrier ability.
- Add corruption reduction.
- Add spirit suppression effect.
- Add breach sealing objective.

---

## 24. High-Difficulty Cooperative Dungeon Prototype

### Goal

Prototype one difficult synchronized challenge.

### Tasks

- Create Qin tomb production pit map.
- Add split routes.
- Add timed platform/mechanism sequence.
- Add enemy pressure.
- Add shared objective health.
- Add reward tied to town defense.

---

## 25. Vertical Slice Boss

### Goal

Create the first major boss encounter.

### Tasks

- Create Awakened Terracotta Commander.
- Add multi-phase behavior.
- Add structure-targeting attack.
- Add player-targeting attack.
- Add town system counterplay.

---

# Suggested First Codex Task

Use this prompt for the first implementation pass:

```text
Build the first playable Godot prototype foundation for this repo.

Follow docs/TECHNICAL_PLAN.md and docs/PROTOTYPE_SCOPE.md.

Do not expand the game scope. Focus only on P0 tasks 1-4 from docs/IMPLEMENTATION_BACKLOG.md:
- Godot project setup
- player movement and interaction
- reusable health/damage system
- gate defense system

Use placeholder art and simple debug UI. The result should let the player move around a small town map, interact with a gate, and repair the gate after it takes damage.

Do not implement multiplayer, full story, advanced buildings, or large maps yet.
```

## Backlog Management Rule

Do not start P2 tasks until the P0 loop is playable and understandable.

The project should stay prototype-driven:

1. Make the loop playable.
2. Make the loop fun.
3. Then add content.
