# aw-web Backend

The aw-web backend is responsible for managing the core game logic, state updates, player data, and
AI dialogue system for the virtual world project. Built on [Convex](https://www.convex.dev), this
backend ensures efficient, real-time processing of interactions between human players and AI agents
while maintaining the stability of the game world.

## Key Features

### Real-time Multiplayer Interaction

- Utilizes a high-frequency tick model to update the global state.
- Ensures real-time synchronization among multiple players and AI agents.
- Processes state updates sequentially in a single-threaded environment to avoid concurrency issues.

### AI Agents and Dialogue System

- Implements built-in AI agents with rule-based behaviors and large language model integration.
- Supports initiating conversations, remembering historical interactions, and performing various
  asynchronous tasks.
- Enhances user experience by simulating natural human-AI interaction.

### Server-side Game Logic

- Handles the receipt and processing of inputs from players and agents.
- Manages and updates the virtual world state.
- Persists game data and tracks historical changes using Convex's query and mutation interfaces.

### Game Engine

- Simulates the overall state of the virtual world.
- Implements high-frequency tick updates, batching input processing, and supports historical
  playback.
- Provides a robust foundation for smooth state transitions and animations.

## Directory Structure

The backend code is primarily located within the `convex/` directory, which includes:

- **aiTown**: Manages game logic and interaction between players and agents.
- **engine**: Handles state simulation, tick-based updates, input batching, and data persistence.
- **agent**: Defines the behavior, dialogue strategies, and memory management for AI agents.

## How to Run the Backend

### Prerequisites

- Node.js (LTS version recommended)
- npm or yarn

### Install Dependencies

From the project root directory, run:

```bash
npm install
```

or, if using yarn:

```bash
yarn install
```

### Start the Backend Development Environment

Run the following command in your terminal to launch the Convex backend development server and
monitor the backend logs:

```bash
npm run dev:backend
```

### Initialize World Data

After starting the backend, initialize the default world by running:

```bash
npx convex run init
```

This command loads the initial map data and starts the game engine.

## Deployment Guide

### Build the Project

Compile the TypeScript code and generate static assets for the backend:

```bash
npm run build
```

### Deploying the Convex Backend

Deploy the built backend code to your target environment, ensuring that the database, scheduler, and
function services are configured properly.

### Initialize Deployment Data

After deployment, execute the initialization script to create the default world and associated data:

```bash
npx convex run init
```

## Contribution and Support

We welcome contributions to the aw-web backend project. To contribute:

1. Fork the repository and create a new branch.
2. Ensure your changes pass all relevant tests.
3. Submit a Pull Request for review.

For any issues or feature suggestions, please submit an Issue on GitHub or contact the project
maintainers directly.

## License

This project is licensed under the MIT License. For more details, please refer to the
[LICENSE](LICENSE) file.

## Contact

If you have any questions or suggestions, feel free to open an Issue on GitHub or email the project
maintainers.

Happy coding, and enjoy building dynamic virtual worlds!
