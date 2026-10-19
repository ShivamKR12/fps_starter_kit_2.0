# Godot 4 FPS Starter Kit 2.0

A modular, state-chart-driven 3D First-Person Shooter starter kit built with **Godot Engine 4.4** (Forward+ Renderer).

It provides an extensible foundation for modern 3D first-person games, featuring clean GDScript architecture, decoupled state management, smooth camera controls, and a dynamic reticle.

## 🎮 Features

- **State-Chart Movement Controller**: Decoupled movement states managed with hierarchical state charts:
  - *Standing / Crouching*
  - *Idle / Moving / Walking / Sprinting*
  - *Grounded / Airborne (Jumping & Falling)*
- **First-Person Camera**:
  - Smooth mouse look with configurable sensitivity.
  - Clamped vertical pitch angles.
  - Sprint FOV transitions.
- **Dynamic Crosshair / Reticle**:
  - Procedural reticle drawing reacting dynamically to player movement speed and airborne state.
- **Modular Components**:
  - `mouse_capture.gd`: Handles cursor locking and capture toggling on click/escape.
  - `interaction_raycast.gd`: Forward raycasting for interactive objects.
  - `game_manager.gd`: Global session management.
- **Integrated Plugins**:
  - Pre-installed [Godot State Charts](https://github.com/derkork/godot-state-charts) addon (`res://addons/godot_state_charts/`) for visual state machine design and live in-game state debugging.
- **Prototype Playground Level**:
  - Included `prototype_level.tscn` equipped with ramps, pillars, elevation tests, and physics collision bodies.

## 🕹️ Controls

- **W / A / S / D**: Move Forward / Left / Backward / Right
- **Mouse**: Look around / Aim
- **Shift (Hold)**: Sprint
- **C / Ctrl**: Crouch
- **Space**: Jump
- **Escape**: Release / Capture mouse cursor

## 🚀 Getting Started

### Prerequisites

- Download and install [Godot Engine 4.4+](https://godotengine.org/download/).

### How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/ShivamKR12/fps_starter_kit_2.0.git
   cd fps_starter_kit_2.0
   ```

2. Open Godot Engine and click **Import**.
3. Select `project.godot` inside the cloned directory.
4. Press **F5** (or click the Play icon in the top right) to launch the prototype level.

## 🛠️ Project Structure

```
fps_starter_kit_2.0/
├── addons/
│   └── godot_state_charts/     # Hierarchical State Machine addon
├── assets/
│   └── scripts/
│       ├── player/             # Player & camera controllers, states, components
│       ├── system/             # Game manager
│       └── ui/                 # Dynamic reticle drawing
├── levels/
│   └── prototype_level.tscn    # 3D test arena with collisions
├── scenes/
│   ├── environment/            # Lighting & skybox
│   ├── player/                 # Assembled player controller prefab
│   ├── system/                 # Main scene & user interface wrapper
│   └── ui/                     # UI overlays & reticle
└── project.godot               # Godot 4.4 project configuration
```

## 📜 Credits & License

- Built with [Godot Engine](https://godotengine.org/).
- Includes the `godot_state_charts` addon by derkork (MIT License).
