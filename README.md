EnemySpawner
Overview
EnemySpawner is a Unity script that spawns various types of enemies within a specified area at the start of the game. Each type of enemy can be assigned a unique tag, and the spawning positions are validated to ensure they don't overlap with objects that implement the IEnvironment interface.

Features
Spawn multiple types of enemies with configurable counts.
Assign unique tags to different enemy types.
Ensure enemies spawn within a designated area, avoiding overlaps with environmental objects.
Match enemy spawn height with the player's height.
Usage
Inspector Setup
Enemy Types:

Add elements to the Enemy Types list.
For each element, specify the Enemy Prefab, Count, and Tag.
Spawn Area:

Assign the Spawn Area GameObject which defines the area within which enemies will spawn.
Player:

Assign the Player GameObject to match the spawn height with the player's height.
Spawn Margin:

Set the Spawn Margin, which is the minimum distance from the spawn area's edges.
Environment Layer:

Set the Environment Layer to define objects implementing the IEnvironment interface.
Example Inspector Configuration
