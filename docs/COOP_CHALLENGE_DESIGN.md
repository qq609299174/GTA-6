# Cooperative Challenge Design

## Purpose

Tang Frontier includes selected high-difficulty cooperative challenge scenarios. These scenarios are not the main genre of the game, but they create memorable difficulty spikes inside dungeons, story missions, boss encounters, and late-game objectives.

The goal is not to copy simple co-op puzzle design. The goal is to create difficult, high-pressure, synchronized team scenarios where every player has an active job.

These challenges should feel closer to raid mechanics adapted into a 2D / 2.5D action RPG than basic platforming puzzles.

## What This System Is Not

The cooperative challenge system is not:

- A simple button puzzle
- A slow lever sequence
- A stand-on-pressure-plates mechanic
- A section where one player acts and everyone else waits
- A pure platformer mode
- A casual minigame unrelated to the main loop

Avoid scenarios like:

```text
Three players stand on three buttons and a door opens.
```

That is not enough for this game.

## Design Goal

A good cooperative challenge should create this feeling:

> Every player is under pressure, every route matters, timing matters, combat matters, and the team succeeds only if everyone executes their role while communicating.

## Core Rules

A strong challenge should include most of the following:

1. **Role Separation**  
   Players handle different routes, tasks, or threats.

2. **Timing Windows**  
   Actions must happen within strict windows.

3. **Mechanical Execution**  
   Movement, dodging, fighting, carrying, repairing, or interacting must be performed well.

4. **Combat Pressure**  
   Enemies interrupt, chase, defend objectives, or punish delays.

5. **Environmental Hazards**  
   Traps, water levels, collapsing platforms, rotating mechanisms, darkness, fire, poison, corruption, or moving walls.

6. **Shared Failure Conditions**  
   One route failing can affect the whole team, but failure should feel understandable rather than random.

7. **Recovery Windows**  
   Teams should sometimes recover from mistakes through skill, resource use, or sacrifice.

8. **Meaningful Reward**  
   The reward should affect town progression, defense strength, story, research, or region access.

## Challenge Components

### Split Routes

Players may be separated into different lanes or chambers.

Examples:

- Upper mechanism route
- Lower combat route
- Ritual carrier route
- Defense holdout route
- Control room route
- Rescue route

Split routes should interact. One player's success should open, stabilize, or change another player's route.

### Timed Synchronization

Synchronization should not mean pressing the same button at the same time. It should mean completing different tasks inside a shared timing structure.

Examples:

- One player opens a 6-second route window while another crosses a hazard.
- One player lowers water while another pushes a seal stone.
- One player disables arrows while another carries a fragile ritual item.
- One player kills a commander before a ritual channel collapses.

### Pressure Layers

A challenge becomes interesting when multiple pressures stack.

Possible pressure layers:

- Combat pressure
- Time pressure
- Escort pressure
- Resource pressure
- Corruption pressure
- Environmental cycles
- Enemy reinforcements
- Route instability
- Shared objective health

### Role-Specific Tasks

Each route can require different strengths.

Examples:

- High mobility route: dodging traps and making precise jumps
- Combat route: surviving enemy waves and elite units
- Engineering route: repairing or operating machinery
- Ritual route: protecting a fragile object or maintaining a seal
- Logistics route: carrying supplies, keys, or materials under pressure

## Difficulty Principles

### Difficulty Should Be Readable

Players should understand why they failed.

Bad failure:

- Random instant death
- Unclear trigger
- Invisible timer
- Too many hidden rules

Good failure:

- The seal stone reset because enemies reached it.
- The flame went out because the carrier entered the wind zone too early.
- The upper platform collapsed because the control lever was missed.
- The water level changed before the lower route crossed.

### Difficulty Should Escalate

A challenge can have phases:

1. Learn the mechanic
2. Combine mechanic with enemies
3. Add time pressure
4. Add route interaction
5. Add final synchronized execution

### Difficulty Should Reward Mastery

A good team should improve through:

- Better communication
- Better role assignment
- Better timing
- Better route knowledge
- Better use of builds and equipment
- Better preparation from town systems

## Example Challenge 1: Qin Tomb Production Pit

### Setting

A hidden Qin tomb chamber is reactivating terracotta soldiers. The chamber functions like an ancient military production system.

### Objective

Disable the production mechanism before it sends a large terracotta army toward the town.

### Team Roles

#### Upper Route Player

- Crosses collapsing platforms
- Dodges mechanical crossbows
- Disables arrow traps
- Opens short windows for the lower route

#### Lower Route Player

- Pushes heavy seal stones
- Fights terracotta soldiers
- Activates floor mechanisms
- Prevents stone resets

#### Ritual Carrier

- Carries a fragile ritual flame
- Moves slower while carrying
- Must avoid wind vents and enemy attacks
- Needs route windows created by other players

#### Defense Player

- Holds the entry point
- Stops reinforcements
- Protects the retreat route
- May need to leave position temporarily for emergency saves

### Interaction Design

- Upper route disables arrows that would kill the ritual carrier.
- Lower route moving the seal stone changes upper platforms.
- Ritual flame opens the final chamber only if kept lit.
- Defense failure increases enemies inside all routes.

### Failure Conditions

- Ritual flame extinguished
- Production meter reaches full
- Seal stone resets too many times
- Entry route collapses
- All players downed

### Rewards

- Qin enemy weakness research
- Armor-piercing blueprint
- Reduced terracotta raids for several nights
- Unlock next Qin tomb mission

## Example Challenge 2: Chang'an Waterway Seal

### Setting

A corrupted waterway beneath the city is channeling dark energy toward the town.

### Objective

Close three water gates and purify the central channel.

### Mechanics

- Water level cycles between low, medium, and high.
- High water opens swim routes but strengthens water spirits.
- Low water opens ground routes but activates floor traps.
- Medium water allows seal movement but narrows safe zones.

### Roles

#### Gate Controller

- Operates sluice gates
- Cannot fight while controlling machinery
- Must time water level changes for teammates

#### Traversal Player

- Crosses high-risk timing routes
- Dodges traps, currents, and enemies
- Reaches remote switches

#### Ritual Defender

- Protects purification stones
- Prevents water spirits from corrupting the ritual

#### Cleaner / Fighter

- Clears enemy clusters
- Interrupts stronger spirits
- Protects the controller during pressure spikes

### Failure Conditions

- Pollution meter reaches maximum
- Ritual stone destroyed
- Water gate sequence missed
- Controller interrupted during key timing
- Central chamber flooded with corrupted water

### Rewards

- Reduced town corruption rate
- New medicine ingredients
- Waterway trade route
- City questline unlock

## Example Challenge 3: Frontier Beacon Chain

### Setting

A group of old beacon towers must be activated before a large enemy force arrives.

### Objective

Light three beacons in a strict sequence and defend them until reinforcements respond.

### Mechanics

Each beacon has a different task:

1. **Fire Beacon**  
   A player carries flame through enemies and wind hazards.

2. **Mechanism Beacon**  
   A player repairs gears, ladders, and pulleys under attack.

3. **Guardian Beacon**  
   A player defeats a tower guardian and holds the roof.

Once lit, each beacon becomes a defense point. Enemies attempt to extinguish active beacons.

### Difficulty Features

- Timed sequence
- Split routes
- Enemy escalation after each beacon
- Shared reinforcement timer
- Need for route planning before activation

### Rewards

- Temporary allied troops
- Regional map reveal
- Military support system unlock
- Town reputation gain

## Example Challenge 4: Ancient Battlefield Formation Break

### Setting

A ghost army formation is reforming on an old battlefield. If not disrupted, it will march on the town.

### Objective

Break four formation nodes within the same timing window.

### Mechanics

- Each node regenerates if left alone too long.
- Nodes have different mechanics.
- Players must split, weaken nodes, then coordinate final destruction.

### Node Types

#### Drum Node

Summons continuous enemies until interrupted.

#### Banner Node

Buffs all nearby ghost units.

#### Cavalry Node

Creates periodic charge attacks across the battlefield.

#### Commander Node

Protected by elite guards and requires burst damage.

### Failure Conditions

- Any node fully regenerates after the final phase begins
- Formation morale meter reaches maximum
- Too many ghost charges hit the town-bound path
- Players fail to destroy nodes inside the final timing window

### Rewards

- Reduced ghost army raids
- Militia morale upgrade
- Battlefield artifact
- New martial doctrine research

## Integration With Town Systems

Cooperative challenges should interact with the town.

Examples:

- Blacksmith provides armor-piercing tools for Qin tomb challenges.
- Workshop provides repair kits for mechanism challenges.
- Clinic provides antidotes or injury protection.
- Daoist Shrine provides ritual tools and corruption resistance.
- Academy reveals mechanics or weak points.
- Marketplace and Warehouse provide consumables and expedition supplies.
- Barracks can send NPC support for holdout sections.

This keeps challenges connected to preparation, not isolated from the rest of the game.

## Scaling for Player Count

### Solo

- Fewer simultaneous routes
- NPC assistants may hold simple positions
- Longer timing windows
- Lower enemy pressure

### Two Players

- Two major roles at once
- Some route tasks can be sequential instead of simultaneous
- Moderate enemy pressure

### Three to Four Players

- Full split-route design
- More simultaneous responsibilities
- Higher enemy pressure
- Shorter recovery windows

## Design Success Criteria

A cooperative challenge succeeds if:

- Every player has an active responsibility.
- The team understands why success or failure happened.
- The challenge feels hard but fair.
- Preparation from town systems matters.
- Communication improves performance.
- The reward affects town, story, or future defense.
- The encounter is memorable enough that players talk about it afterward.
