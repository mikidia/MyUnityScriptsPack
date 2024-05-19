# FirstPersonControllerScript

## Overview

`FirstPersonControllerScript` is a Unity script that provides a basic implementation of a first-person character controller. It handles player movement, jumping, and mouse-based camera control with smooth rotation.

## Features

- **Frame Rate Control:** Set the target frame rate for the application.
- **Movement:** Basic WASD movement with adjustable speed.
- **Jumping:** Ability to jump with adjustable jump speed.
- **Gravity:** Adjustable gravity for realistic falling.
- **Mouse Look:** Smooth and responsive mouse look with adjustable sensitivity and smoothing.

## Getting Started

### Prerequisites

- Unity 2019.4 or higher

### Installation

1. Download or clone the repository.
2. Add the `FirstPersonControllerScript` to a GameObject with a `CharacterController` component in your Unity project.

### Usage

1. **Attach Script:**
   - Attach the `FirstPersonControllerScript` to a GameObject in your scene that has a `CharacterController` component.

2. **Configure in Inspector:**
   - **FPS:** Set the target frames per second (default is 120).
   - **Speed:** Set the movement speed (default is 6.0).
   - **Jump Speed:** Set the jump speed (default is 8.0).
   - **Gravity:** Set the gravity force (default is 20.0).
   - **Look Sensitivity:** Adjust the mouse look sensitivity (default is 2).
   - **Look Smoothness:** Adjust the smoothness of the mouse look (default is 0.1).

### Example Inspector Configuration

```plaintext
FPS: 120
Speed: 6.0
Jump Speed: 8.0
Gravity: 20.0
Look Sensitivity: 2.0
Look Smoothness: 0.1

```

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
