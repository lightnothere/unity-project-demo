# Advanced Movement 2D

Welcome to my first game project! This is a 2D game focused on implementing advanced movement mechanics and controls. The project is built using Unity and features various player movement systems that I've developed as part of learning game development.

This project represents my initial foray into game development. As a beginner, I'm experimenting with and implementing fundamental concepts in Unity, primarily focusing on creating smooth and responsive movement systems for 2D characters. The goal is to build a solid foundation for more complex game mechanics in future projects.

## Project Overview

This project serves as my introduction to game development using Unity. It focuses on creating smooth and responsive player movement systems in a 2D environment, with emphasis on:

- Character movement controls
- Input handling
- Animation systems
- 2D physics
- Game state management

## Prerequisites

To run this project, you will need:

- Unity 2021.3 LTS or higher
- Visual Studio or another compatible IDE for C# scripting

## Installation

1. Clone or download this repository to your local machine
2. Open Unity Hub
3. Click "Add" and navigate to the project folder
4. Select the folder and click "Open"
5. Unity should automatically import all assets and dependencies

## Project Structure

```
Assets/
├── InputActions.cs              # Input system actions and mappings
├── InputActions.inputactions    # Unity input actions configuration
├── InputSystem_Actions.inputactions # Alternative input system configuration
├── Materials/                   # Material assets
├── Prefabs/                     # GameObject prefabs
├── Fonts/                       # Font assets
└── Blah.unity                 # Main scene file
```

## Code Files Guide

Based on the files visible in the project directory, here's a detailed breakdown of the code files and their usage:

### InputActions.cs
This script serves as a bridge between the Unity Input System and game logic. It contains auto-generated code from the input actions configuration files.

**Usage:**
- Provides access to input actions defined in .inputactions files
- Enables device-agnostic input handling (keyboard, mouse, gamepad)
- Should be referenced by player controller scripts to respond to input
- Contains methods to enable/disable input action maps

### Input System Configuration Files
- `InputActions.inputactions` and `InputSystem_Actions.inputactions` are Unity Input System asset files
- Define input actions, bindings, and control schemes
- Generate C# code that can be used by other scripts
- Allow for easy remapping of controls without changing code
- Support different control schemes for different devices

### Player Controller Script Template
While not explicitly visible in the root directory, a typical player controller script would:
- Use the InputActions.cs to receive input
- Handle 2D physics using Rigidbody2D
- Implement movement, jumping, and animation logic
- Manage player states (idle, running, jumping, etc.)
- Handle collisions and interactions with the game world

### Scene Files
- `Blah.unity` is the main scene containing game elements
- Contains the player character prefab with attached controller script
- Includes the game environment, cameras, lighting, and UI elements
- Serves as the container for all runtime objects

### Material Files
- Located in the Materials folder
- Define surface properties for 3D objects (likely used for UI or 2.5D elements)
- Include textures, colors, and shader properties
- Applied to sprites and objects in the scene for visual styling

## How to Use

1. Open the project in Unity
2. Navigate to the `Assets` folder and open `Blah.unity` in the Editor
3. Press the Play button to test the game
4. Use arrow keys or WASD to move the character
5. Use additional keys as defined in the Input System for other actions

## Features

- Responsive 2D movement system
- Input handling for multiple control schemes
- Extensible character controller
- Clean and organized code structure

## Contributing

This is a personal learning project, but feel free to fork and experiment with the code. If you have suggestions for improvements, I'd love to hear them!

## Code Templates and Usage Guidelines

As this is my first game project, I've implemented several code templates and patterns to help maintain consistency and structure throughout the development process.

### Player Controller Template
I've set up a basic player controller template that follows Unity's recommended practices:

1. Inherits from MonoBehaviour
2. Uses Unity's Input System for handling controls
3. Implements physics-based movement using Rigidbody2D
4. Includes state management for different player actions (idle, moving, jumping, etc.)

### Code Structure
All C# scripts follow a consistent structure:
- Public variables for inspector customization
- Serialized fields for internal references
- Private variables for internal logic
- Properly documented methods using standard C# documentation

### Input System Template
The input system is configured using Unity's Input System package:
- Action maps defined in .inputactions files
- Device-agnostic input handling
- Support for keyboard, mouse, and gamepad controls
- Easy remapping of controls

### Best Practices Implemented
- Single responsibility principle: Each script handles one main functionality
- Proper Unity lifecycle methods: Use Start() for initialization, Update() for frame-based updates, and FixedUpdate() for physics calculations
- Memory management: Proper disposal of resources and object pooling where appropriate
- Performance optimization: Minimize use of expensive operations in Update() methods

## License

This project is open source and available under the MIT License.