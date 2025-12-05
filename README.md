# Roll The RPG

A Unity package for the Roll The RPG game jam project by Tiny Walnut Games.

## Installation

Add this package to your Unity project via the Package Manager using the Git URL:

```url
https://github.com/Tiny-Walnut-Games/rolltherpg.git
```

## Development

This package contains the core game logic and assets for Roll The RPG.

## 🎲 Dice RPG Jam – TDD Task List

Using **Synty Studios Fantasy RPG Tiles** + **Mini Fantasy Characters**  
Theme: *Creation* | Limitation: *Roll the Dice*

---

### 1. Core Dice Mechanics

- [ ] **Test:** `test_roll_returns_valid_values` → Dice roll returns values within die range (d4, d6, d8, d10).
- [ ] **Implement:** Dice roll function.
- [ ] **Test:** `test_class_maps_to_correct_dice` → Warrior/Mage/Rogue classes map to correct dice sets.
- [ ] **Implement:** Class factory with dice mapping.

---

### 2. Tile Creation

- [ ] **Test:** `test_tile_roll_places_correct_number` → Tile roll places N tiles adjacent to frontier.
- [ ] **Implement:** Tile placement system.
- [ ] **Test:** `test_tile_has_valid_terrain_type` → Terrain type assigned correctly (forest, mountain, plains, water).
- [ ] **Implement:** Terrain generator using Synty tile assets.

---

### 3. Movement & Fog of War

- [ ] **Test:** `test_move_roll_allows_steps` → Move roll allows correct number of steps.
- [ ] **Implement:** Movement system with tile traversal.
- [ ] **Test:** `test_fow_reveal_radius` → Normal terrain exposes 2 tiles, rough terrain exposes 1.
- [ ] **Implement:** FoW reveal logic.
- [ ] **Test:** `test_move_five_tiles_exposes_eleven` → Moving 5 tiles in open terrain exposes 11 tiles.
- [ ] **Implement:** Exposure calculation.

---

### 4. Encounters

- [ ] **Test:** `test_encounter_chance_per_tile` → Each exposed tile rolls for encounter chance.
- [ ] **Implement:** Encounter generator.
- [ ] **Test:** `test_enemy_spawns_on_tile` → Enemy spawns at correct position.
- [ ] **Implement:** Enemy placement system using Synty mini characters.
- [ ] **Test:** `test_enemy_alert_range` → Enemies within 2 tiles become alerted.
- [ ] **Implement:** Alert logic.

---

### 5. Enemy Movement

- [ ] **Test:** `test_enemy_moves_every_other_turn` → Alerted enemies move every other turn.
- [ ] **Implement:** Enemy AI rhythm.
- [ ] **Test:** `test_enemy_move_speed_cap` → Movement capped by enemy Move Speed.
- [ ] **Implement:** Speed-based movement system.
- [ ] **Test:** `test_enemy_terrain_penalty` → Rough terrain slows enemy movement.
- [ ] **Implement:** Terrain penalty integration.

---

### 6. Chase & Give-Up Logic

- [ ] **Test:** `test_chase_decay_formula` → Distance increases chance to abandon chase.
- [ ] **Implement:** Chase decay formula (distance/max range).
- [ ] **Test:** `test_chase_terrain_modifier` → Forest/mountain terrain increases give-up chance.
- [ ] **Implement:** Terrain modifier in chase roll.
- [ ] **Test:** `test_auto_abandon_at_max_range` → At max range, enemy always gives up.
- [ ] **Implement:** Auto-abandon rule.

---

### 7. Combat Resolution

- [ ] **Test:** `test_player_rolls_life_def_atk` → Player rolls Life, Def, Atk in fixed order.
- [ ] **Implement:** Combat loop.
- [ ] **Test:** `test_healing_capped_at_max_hp` → Healing capped at max HP.
- [ ] **Implement:** HP cap logic.
- [ ] **Test:** `test_def_roll_applies_shield` → Def roll applies temporary shield until next turn.
- [ ] **Implement:** Shield mechanic.
- [ ] **Test:** `test_atk_roll_applies_damage` → Atk roll applies damage to enemy.
- [ ] **Implement:** Damage resolution.

---

### 8. Story Test Integration

- [ ] **Test:** Phantom props eliminated (no unused tiles, dice, or methods).
- [ ] **Test:** Cold methods removed (all combat/encounter logic exercised).
- [ ] **Test:** Hollow enums avoided (CorridorLength replaced with meaningful values).
- [ ] **Test:** No premature celebration (success logged only after readiness).
- [ ] **Implement:** Refactor until Story Test passes clean.

---

### ⚡ Jam Milestones

- **Day 1:** Dice mechanics + tile creation + movement/FoW.  
- **Day 2:** Encounters + enemy movement + chase logic.  
- **Day 3:** Combat loop + polish + Story Test cleanup.

---

### Assets

- **Tiles:** Synty Studios Fantasy RPG World Pack (hex/square).  
- **Characters:** Synty Studios Mini Fantasy Heroes.  
- **Integration:** Use tiles for terrain generation, minis for enemy/player representation.
