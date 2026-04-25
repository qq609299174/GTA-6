# Building System

## Purpose

The building system is one of the central pillars of Tang Frontier.

Buildings must not be passive decorations or one-time unlocks. They should form the operational backbone of the town. A building should produce, consume, upgrade, fail, recover, and interact with combat, economy, research, quests, NPCs, and town survival.

The town should feel like a machine made of interconnected buildings. If one part fails, the rest of the town should feel the consequence.

## Core Building Design Rules

Every major building should include the following design elements:

1. **Construction Cost**  
   The resources required to build the structure.

2. **Upgrade Path**  
   Multiple levels or specialization branches.

3. **Staffing Requirement**  
   NPCs or players can operate the building for better output.

4. **Production Output**  
   Items, resources, services, research, money, defensive tools, or town benefits.

5. **Active Ability**  
   A player-triggered or condition-triggered function that matters during gameplay.

6. **Passive Benefit**  
   Background effect that improves town function.

7. **Resource Upkeep**  
   Important buildings may consume fuel, food, coins, paper talismans, medicine, metal, or other inputs.

8. **Damage State**  
   Buildings can be damaged, disabled, corrupted, burned, raided, or understaffed.

9. **Failure Consequence**  
   If the building fails, gameplay becomes harder in a specific way.

10. **Progression Link**  
   Buildings unlock quests, regions, research, equipment, NPCs, or story paths.

## Building State Model

Each building can have several states:

### Unbuilt

The building is not yet available or has not been constructed.

### Under Construction

Resources have been committed. The building requires time or labor to finish.

### Operational

The building is active and can perform its normal functions.

### Understaffed

The building works at reduced efficiency due to insufficient workers.

### Damaged

The building still exists but has reduced output and may lose active abilities.

### Disabled

The building cannot function until repaired.

### Corrupted

The building is affected by supernatural pressure. It may produce negative side effects until purified.

### Upgrading

The building is being improved and may be partially unavailable during the process.

## Building Categories

### Core Governance

- Town Hall
- Notice Board
- Tax / administration systems

### Production

- Blacksmith
- Workshop
- Farm
- Granary
- Lumber Yard
- Quarry
- Furnace

### Economy

- Marketplace
- Warehouse
- Caravan Office
- Inn
- Trade stall upgrades

### Defense

- Walls
- Gates
- Watchtowers
- Barracks
- Trap control systems
- Siege tool platforms

### Research and Spiritual Systems

- Academy
- Archive
- Daoist Shrine
- Ritual Platform
- Seal Tower

### Support

- Clinic
- Kitchen
- Housing
- Public well
- Emergency shelter

## Major Buildings

## 1. Town Hall

### Role

The central command structure of the town.

### Core Functions

- Unlocks town management UI
- Tracks population, morale, corruption, and prosperity
- Enables building placement and upgrades
- Stores key town records
- Issues major town decisions

### Upgrade Path

#### Level 1: Ruined Hall Restored

- Enables basic construction
- Unlocks basic worker assignment
- Tracks town health

#### Level 2: Frontier Office

- Unlocks town policies
- Improves NPC assignment
- Enables basic tax income

#### Level 3: Regional Command Hall

- Unlocks advanced defense planning
- Enables multi-district town management
- Improves reputation gain

### Active Abilities

- **Emergency Order**: temporarily increases worker speed or repair speed.
- **Rally Town**: reduces panic and stabilizes morale during night.
- **Evacuation Command**: moves civilians away from threatened districts.

### Failure Consequence

If the Town Hall is disabled:

- Worker reassignment becomes unavailable
- Town morale drops sharply
- Building upgrades pause
- Certain emergency commands cannot be used

## 2. Blacksmith

### Role

Weapons, armor, metal components, repairs, and defensive reinforcement.

### Core Functions

- Craft melee and ranged weapons
- Repair damaged weapons and armor
- Produce metal components for traps and buildings
- Reinforce gates and walls
- Produce armor-piercing tools against heavy enemies
- Support engineers with parts

### Inputs

- Iron ore
- Coal or fuel
- Wood
- Coins
- Worker time

### Outputs

- Weapons
- Armor
- Nails
- Spikes
- Reinforcement plates
- Trap blades
- Gate braces

### Upgrade Branches

#### Weapon Forge

Focuses on player equipment and offensive output.

#### Defense Forge

Focuses on gates, walls, traps, and siege tools.

#### Precision Smithy

Focuses on elite counters, special arrows, armor-piercing tools, and boss preparations.

### Active Abilities

- **Emergency Repair Kit**: instantly repairs a selected gate, wall, or defense device.
- **Night Tempering**: gives players a temporary weapon damage bonus for one night.
- **Armor Break Batch**: produces temporary armor-piercing ammunition.

### Combat Impact

- Stronger player weapons
- Faster repair capability
- Better gate durability
- Access to counters against armored enemies
- Better traps and siege devices

### Failure Consequence

If damaged or disabled:

- Weapon repairs stop
- Gate reinforcement is unavailable
- Trap component production slows
- Armored enemies become harder to counter

## 3. Workshop / Carpentry Yard

### Role

Construction, repairs, platforms, traps, and town infrastructure.

### Core Functions

- Build wooden defenses
- Repair buildings
- Produce traps
- Build ladders, bridges, lifts, barricades, and platforms
- Support 2D / 2.5D traversal routes
- Enable rapid defensive layout changes

### Inputs

- Wood
- Stone
- Rope
- Iron components
- Worker time

### Outputs

- Barricades
- Spike traps
- Rolling logs
- Roof walkways
- Ladders
- Emergency platforms
- Repair kits
- Watchtower components

### Upgrade Branches

#### Defensive Carpentry

Focuses on walls, barricades, platforms, and gate support.

#### Trap Workshop

Focuses on traps, mechanical devices, and lane control.

#### Infrastructure Workshop

Focuses on bridges, lifts, roof routes, town mobility, and exploration tools.

### Active Abilities

- **Rapid Construction**: builds a temporary barricade or platform during night.
- **Emergency Patch**: prevents a damaged building from becoming disabled.
- **Trap Reset**: instantly rearms nearby traps.

### Failure Consequence

If disabled:

- Repairs become slower
- Temporary structures cannot be built
- Trap reset is unavailable
- Movement routes may become harder to maintain

## 4. Marketplace

### Role

Town economy, civilian demand, trade, supply, and money generation.

The marketplace is the ancient equivalent of a town shop or supermarket system. It should not use modern supermarket language in-world. It should be presented as a market district, shopfront, stall network, or city market.

### Core Functions

- Sell goods to residents
- Sell goods to merchants
- Generate coins
- Track supply and demand
- Increase prosperity
- Attract visitors and trade NPCs
- Convert surplus resources into money
- Provide emergency supplies during defense

### Inventory Types

- Food
- Medicine
- Tools
- Weapons
- Clothing
- Building materials
- Luxury goods
- Ritual items
- Rare artifacts

### Economy Systems

- Stock level
- Demand level
- Price setting
- Civilian satisfaction
- Merchant reputation
- Town prosperity
- Supply shortage penalties
- Special orders

### Active Abilities

- **Emergency Supply Release**: consumes stored goods to recover morale, health, or repair capacity.
- **Merchant Contract**: attracts a merchant with specific goods after a delay.
- **Price Adjustment**: changes profit and satisfaction balance.

### Combat Impact

- Generates coins for upgrades
- Supplies food and medicine
- Improves morale
- Attracts useful merchants
- Provides rare materials through trade
- Enables pre-night supply buffs

### Failure Consequence

If mismanaged or damaged:

- Morale decreases
- Coin income drops
- Merchant traffic slows
- Shortages appear
- Civilian satisfaction drops
- Upgrades slow due to lack of money

## 5. Warehouse

### Role

Storage, logistics, caravans, and bulk supply movement.

### Core Functions

- Store large quantities of resources
- Manage caravan goods
- Fulfill regional contracts
- Reduce waste
- Prepare expedition supplies
- Support long defense nights

### Systems

- Storage capacity
- Item categories
- Spoilage for certain goods
- Caravan scheduling
- Trade route risk
- Contract deadlines
- Emergency reserve rules

### Active Abilities

- **Emergency Stockpile**: sends stored resources to a selected building.
- **Caravan Request**: calls a caravan with delayed arrival.
- **Contract Fulfillment**: trades bulk goods for rare resources or reputation.

### Failure Consequence

If damaged:

- Stored goods may be lost
- Trade is interrupted
- Repair materials become harder to access
- Expedition preparation slows

## 6. Academy / School / Archive

### Role

Research, knowledge, blueprints, enemy analysis, skill development, and mechanism decoding.

### Core Functions

- Research enemy weaknesses
- Unlock building blueprints
- Improve NPC worker efficiency
- Reveal map clues
- Decode dungeon mechanisms
- Improve attack forecasts
- Unlock advanced skills or tactical doctrines

### Research Categories

1. **Enemy Studies**  
   Weaknesses, resistances, wave behavior, elite counters.

2. **Engineering Studies**  
   Better traps, walls, mechanisms, repair tools.

3. **Ritual Studies**  
   Seals, barriers, anti-undead systems, corruption control.

4. **Trade and Geography**  
   Routes, regional goods, hidden areas, caravan opportunities.

5. **Combat Doctrine**  
   NPC guard behavior, player tactical upgrades, formation bonuses.

### Active Abilities

- **Night Forecast**: reveals part of tonight's attack pattern.
- **Weakness Report**: marks elite enemy vulnerabilities.
- **Tactical Briefing**: grants a temporary team buff.

### Failure Consequence

If damaged:

- Research pauses
- Enemy previews are lost
- Blueprint unlocks slow
- Certain dungeon mechanisms remain unreadable

## 7. Clinic / Medicine Hall

### Role

Healing, recovery, medicine production, injury treatment, poison and curse cleansing.

### Core Functions

- Produce healing items
- Treat injured NPCs
- Reduce death penalties
- Cure poison, corruption, and curses
- Improve recovery after battle
- Prepare expedition medical kits

### Active Abilities

- **Emergency Treatment**: heals nearby players and NPCs.
- **Revival Talisman**: revives one fallen player under limited conditions.
- **Cleanse Mist**: removes poison, corruption, or curse effects in an area.

### Failure Consequence

If damaged:

- Injuries last longer
- NPCs become unavailable for longer
- Player recovery weakens
- Curse and poison effects become more dangerous

## 8. Daoist Shrine / Ritual Office

### Role

Spiritual defense, seals, barriers, corruption control, and anti-undead systems.

### Core Functions

- Maintain town barrier
- Seal underground breaches
- Reduce corruption
- Study supernatural threats
- Unlock ritual abilities
- Protect buildings from ghost attacks

### Systems

- Corruption meter
- Seal durability
- Ritual resource supply
- Barrier coverage
- Spiritual threat forecast

### Active Abilities

- **Town Barrier**: reduces building damage for a short time.
- **Spirit Suppression**: weakens undead and ghost enemies.
- **Seal Pulse**: knocks back enemies near breach points.
- **Purification Ritual**: reduces corruption after successful defense.

### Failure Consequence

If damaged:

- Corruption rises faster
- Ghost enemies become stronger
- Breach events increase
- Certain boss attacks become harder to survive

## 9. Barracks / Martial Hall

### Role

NPC guards, militia training, combat doctrine, patrols, and town defense.

### Core Functions

- Train guards
- Assign patrol routes
- Improve gate defense
- Unlock combat-related upgrades
- Prepare militia units
- Detect infiltrators

### Active Abilities

- **Rally Militia**: summons trained guards to a selected location.
- **Defensive Formation**: improves nearby player and NPC defense.
- **Counterattack Order**: sends guards outside the wall briefly.

### Failure Consequence

If damaged:

- Guard strength decreases
- Patrol coverage weakens
- Infiltrators become more dangerous
- Players must cover more lanes manually

## 10. Inn

### Role

Recruitment, quests, travelers, rumors, and town reputation.

### Core Functions

- Attract travelers
- Generate side quests
- Recruit specialists
- Improve town reputation
- Provide rumors about regions and hidden threats
- House temporary merchants or quest NPCs

### Active Abilities

- **Recruit Specialist**: spend reputation to attract a selected NPC type.
- **Gather Rumors**: reveal hidden side quests or resource locations.
- **Feast**: improves morale before a dangerous night.

### Failure Consequence

If damaged:

- Fewer travelers arrive
- Side quest generation slows
- Recruitment weakens
- Reputation growth slows

## 11. Farm / Granary

### Role

Food supply, morale, population support, expedition preparation, and siege endurance.

### Core Functions

- Produce food
- Store grain
- Support civilians and workers
- Provide cooking ingredients
- Prepare expedition rations
- Reduce marketplace shortages

### Active Abilities

- **Emergency Rationing**: prevents morale collapse during shortages.
- **War Meal**: provides a temporary team buff.
- **Supply Pack**: prepares food for expeditions.

### Failure Consequence

If damaged:

- Food shortages begin
- Morale decreases
- Worker efficiency drops
- Civilians may leave

## Inter-Building Dependencies

Buildings should depend on each other to form a living town system.

Examples:

- Blacksmith needs Warehouse storage for bulk ore.
- Workshop needs Blacksmith components for advanced traps.
- Marketplace needs Farm and Workshop goods to stay stocked.
- Academy needs recovered artifacts from exploration.
- Daoist Shrine needs Academy research to improve rituals.
- Clinic needs herbs from expeditions and containers from Workshop.
- Barracks needs Blacksmith weapons and Farm food supply.
- Inn improves recruitment, which improves staffing across all buildings.

## Building Damage and Repair

Night attacks can damage buildings.

Damage levels:

1. **Light Damage**: reduced efficiency.
2. **Heavy Damage**: active ability disabled.
3. **Disabled**: production stops.
4. **Critical**: risk of resource loss, NPC injury, or corruption.

Repair sources:

- Workshop repair kits
- Player repair action
- Assigned workers
- Blacksmith reinforcement
- Emergency Town Hall order

## Design Success Criteria

The building system succeeds if:

- Players care when buildings are damaged.
- Buildings affect combat, economy, and exploration.
- Upgrades create meaningful choices.
- Staffing matters.
- Economy and logistics are not optional decoration.
- Each building creates both power and vulnerability.
- The town feels like a system rather than a collection of menus.
