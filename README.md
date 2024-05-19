# EnemySpawner

## Overview

`EnemySpawner` is a Unity script designed to spawn various types of enemies within a specified area at the start of the game. Each type of enemy can be assigned a unique tag, and the spawning positions are validated to ensure they don't overlap with objects that implement the `IEnvironment` interface.

## Features

- **Multiple Enemy Types:** Configure and spawn different types of enemies.
- **Unique Tags:** Assign unique tags to each type of enemy.
- **Validated Spawning:** Ensure enemies spawn within a designated area, avoiding overlaps with environmental objects.
- **Height Matching:** Match enemy spawn height with the player's height.

## Getting Started

### Prerequisites

- Unity 2019.4 or higher

### Installation

1. Download or clone the repository.
2. Add the `EnemySpawner` script to a GameObject in your Unity project.

### Usage

1. **Attach Script:**
   - Attach the `EnemySpawner` script to an empty GameObject in your scene.

2. **Configure in Inspector:**
   - **Enemy Types:** Add elements to the `Enemy Types` list. For each element, specify:
     - `Enemy Prefab`: The prefab of the enemy to spawn.
     - `Count`: The number of enemies to spawn.
     - `Tag`: The tag to assign to this type of enemy.
   - **Spawn Area:** Assign the GameObject that defines the spawn area.
   - **Player:** Assign the player GameObject to match the spawn height.
   - **Spawn Margin:** Set the minimum distance from the spawn area's edges.
   - **Environment Layer:** Set the layer mask for objects implementing the `IEnvironment` interface.

### Example Inspector Configuration

```plaintext
Enemy Types:
  - Enemy Prefab: ZombiePrefab
    Count: 5
    Tag: Zombie
  - Enemy Prefab: SkeletonPrefab
    Count: 3
    Tag: Skeleton

Spawn Area: SpawnAreaGameObject
Player: PlayerGameObject
Spawn Margin: 1.0
Environment Layer: EnvironmentLayer
