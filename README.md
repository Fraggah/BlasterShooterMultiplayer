# Blaster Shooter Multiplayer

<img width="3839" height="2159" alt="image" src="https://github.com/user-attachments/assets/bf2ec86d-ecbf-4754-a7ba-361164129924" />

**Genre:** Multiplayer FPS/TPS Shooter  
**Engine:** Unreal Engine 5 (C++ + Blueprints)  
**Platform:** PC (Windows, Steam)

Blaster Shooter Multiplayer is a competitive multiplayer shooter built from the ground up in C++ with Unreal Engine 5, focusing on precise replication and networked gameplay. It integrates the Steam Subsystem via a custom plugin developed to connect through the `AppID 40 (Spacewar)` sandbox, enabling lobbies, matchmaking, and seamless peer connections.

---

## ✨ Key Features

- **Custom Steam Subsystem Plugin**
  - Written in C++ to handle initialization and connection to Steam’s Spacewar AppID (40) for testing.
  - Lobby creation, player invites, and session browsing.
  - Player count, game mode, and map selection from the menu.

- **Advanced Replication Logic**
  - Careful distinction of what to replicate and where:
    - **Server-only:** authoritative gameplay logic, damage calculations, score handling.
    - **Client-only:** prediction, input handling, local effects.
    - **Both:** position, rotation, relevant animation states.
  - Optimized network usage with conditional replication and relevance checks.

- **Character Animation Systems**
  - **FABRIK IK**: Used for precise weapon alignment with hands in any stance.
  - **Animation Blending:** Smooth transitions between idle, walk, run, crouch, and aim poses.
  - **Dynamic Aim Offset:** Real-time blending for aiming up/down/left/right without snapping.
  - Full-body awareness in third-person with synchronized aim direction.

- **Core Shooter Mechanics**
  - Projectile & hitscan weapons.
  - Reload, ammo management, and recoil systems.
  - Headshot multipliers and damage types.

- **Multiplayer Architecture**
  - Dedicated server and listen server modes.
  - Proper ownership checks for authority-side actions.
  - Lag compensation for fair hit registration.
