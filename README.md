# Plants vs Zombies - C# Unity Game

A complete Plants vs Zombies tower defense game built in C# with Unity.

## Game Overview

Defend your garden from incoming zombies by strategically planting various plants that can attack or produce resources. Manage your sun resource carefully to place plants and survive the waves of zombies.

## Features

### Plants
- **Sunflower** (50 Sun) - Generates additional sun over time
- **Peashooter** (100 Sun) - Shoots peas at zombies in its row
- **Walnut** (150 Sun) - Tank plant that absorbs damage
- **Cherrybomb** (150 Sun) - Explodes when zombies are nearby, dealing massive damage
- **Torchwood** (175 Sun) - Burns zombies and modifies pea attacks

### Zombies
- **Normal Zombie** - Standard zombie with basic stats
- **Conehead Zombie** - More durable than normal zombies
- **Bucket Zombie** - Heavily armored zombie with high health
- **Flag Zombie** - Fast and aggressive

### Game Mechanics
- **Sun Resource System** - Earn sun by placing sunflowers or naturally over time
- **Grid-Based Board** - 9x5 grid for strategic plant placement
- **Wave System** - Zombies spawn in waves with increasing difficulty
- **Win Condition** - Defeat all 50 zombies to win
- **Lose Condition** - Zombies reaching the left side (player's house) results in defeat

## Core Systems

### GameManager.cs
Central game manager handling:
- Sun resource management
- Game state (active, won, lost)
- Win/lose conditions
- Zombie defeat tracking

### GridSystem.cs
Manages the game board:
- 9x5 grid layout
- Plant placement and tracking
- Zombie movement constraints
- Position validation

### Plant.cs
Base plant class with:
- Different plant types with unique behaviors
- Attack system for offensive plants
- Sun generation for sunflowers
- Explosion mechanics for cherrybombs
- Health and damage system

### Zombie.cs
Base zombie class with:
- Different zombie types with varied stats
- Pathfinding and movement
- Plant targeting system
- Attack mechanics
- Health tracking

### PlantSystem.cs
Manages plant selection and placement:
- Plant type selection
- Cost validation
- Grid placement
- Plant instantiation

### ZombieSpawner.cs
Handles zombie spawning:
- Wave-based spawning system
- Random zombie type selection
- Spawn interval management
- Total zombie tracking

### UIManager.cs
User interface management:
- Sun display
- Game state indicators
- Button state management
- Resource cost display

## How to Play

1. **Start the Game** - Zombies begin spawning from the right side
2. **Earn Sun** - Sunflowers generate sun passively; earn 25 sun every 2 seconds
3. **Place Plants** - Click plant buttons and click on the grid to place them
4. **Defend** - Peashooters and other plants automatically attack nearby zombies
5. **Manage Resources** - Use sun wisely to defend against all waves
6. **Win Condition** - Survive and defeat all 50 zombies

## Game Controls

- **Left Click** - Place selected plant on grid
- **Plant Buttons** - Select which plant to place
- **ESC** - Cancel plant placement

## Installation & Setup

1. Create a new Unity project (2020.3 LTS or later)
2. Clone this repository
3. Copy all .cs scripts to your Assets folder
4. Create the following GameObjects in your scene:
   - Main Canvas (for UI)
   - GameManager (attach GameManager.cs)
   - GridSystem (attach GridSystem.cs)
   - ZombieSpawner (attach ZombieSpawner.cs)
   - UIManager (attach UIManager.cs)

5. Create prefabs:
   - Plant prefab with Plant.cs component
   - Zombie prefab with Zombie.cs component

6. Assign all references in the Inspector
7. Run the game!

## Game Balance

- **Sun Generation**: 25 sun every 2 seconds
- **Starting Sun**: 100
- **Max Sun**: 500
- **Total Zombies**: 50 per game
- **Spawn Interval**: 3 seconds between waves

## Future Enhancements

- Additional plant types with unique abilities
- Multiple difficulty levels
- Sound effects and music
- Particle effects for attacks
- Achievement system
- High score tracking

## License

Free to use and modify.

---

Enjoy defending your garden from the zombie apocalypse!
