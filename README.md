# Multiplayer Bomberman Game

## Overview
This project is a multiplayer version of the classic Bomberman game, where 2-4 players battle until only one player is left standing. The game features dynamic gameplay, power-ups, and a built-in chat system for player communication. The game is developed using a custom framework created in a previous project.

## Table of Contents
- [Features](#features)
- [Game Mechanics](#game-mechanics)
  - [Players](#players)
  - [Map](#map)
  - [Power-ups](#power-ups)
- [Multiplayer and Chat](#multiplayer-and-chat)
- [Performance Requirements](#performance-requirements)
- [Setup Instructions](#setup-instructions)
- [Future Enhancements](#future-enhancements)
- [Directory Structure](#directory-structure)

## Features
- Multiplayer support for 2-4 players.
- Real-time chat using WebSockets.
- Various power-ups to enhance gameplay.
- Fixed map layout with destructible and indestructible blocks.
- Customizable player nicknames.
- Responsive design to ensure a smooth gaming experience.

## Game Mechanics

### Players
- Number of players: 2-4.
- Each player starts with 3 lives.
- Players are placed in the corners of the map at the start of the game.

### Map
- The map is fixed and fully visible to all players.
- Two types of blocks: destructible blocks and indestructible walls.
- Destructible blocks are randomly generated at the start of each game.
- Players' starting positions are free of destructible blocks to ensure they can avoid bomb explosions.

### Power-ups
Random power-ups may appear when a block is destroyed:
- **Bombs**: Increases the number of bombs a player can drop at a time by 1.
- **Flames**: Increases the bomb explosion range by 1 block in four directions.
- **Speed**: Increases the player's movement speed.

## Multiplayer and Chat
- Players enter a nickname before joining a game.
- A waiting page displays the player count, starting the game once 2-4 players are ready.
- If the player count reaches 4 before 20 seconds, a 10-second timer starts. If not, the timer starts when the count reaches 2.
- In-game chat allows players to communicate using WebSockets.

## Performance Requirements
- The game must run at 60fps at all times with no frame drops.
- Proper use of `requestAnimationFrame` for smooth animations.
- Performance measurements are taken to ensure optimal game speed.

## Setup Instructions
1. **Clone the Repository:**
    ```bash
    git clone https://github.com/yourusername/multiplayer-bomberman.git
    cd multiplayer-bomberman
    ```

2. **Install Dependencies:**
    ```bash
    npm install
    ```

3. **Run the Game:**
    ```bash
    npm start
    ```

4. **Access the Game:**
    Open your browser and go to `http://localhost:3000` to start playing.

## Future Enhancements
- **Solo + Co-Op Mode**: Develop AI opponents and allow co-op gameplay.
- **Additional Power-ups**:
  - Bomb Push: Ability to throw placed bombs.
  - Bomb Pass: Pass through bombs.
  - Block Pass: Pass through blocks.
  - Detonator: Choose when a bomb will explode.
  - 1 Up: Extra life.
- **Release Power-ups After Death**: Drop power-ups upon player death.
- **Team Mode**: 2v2 team battles.
- **After Death Interaction**: Ghost mode allowing players to revive teammates or die permanently.

## Conclusion
This project demonstrates the creation of a multiplayer Bomberman game with real-time chat and various gameplay enhancements. It focuses on performance optimization, real-time communication, and a smooth user experience.
