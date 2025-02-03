# Rotating Polygon Physics Animations

A collection of interactive physics-based animations featuring objects bouncing inside a rotating hexagon. The project includes multiple variations:
- Single bouncing ball
- Multiple bouncing balls
- Animated floating letters

## AI Model Testing Documentation

This project was developed to test the capabilities of different AI models (Claude-3.5 Sonnet and O3 Mini) in handling complex physics-based animations and debugging tasks.

### Prompts and Results

1. **Initial Physics Implementation**
   - Prompt: "Write a JS program that shows a ball bouncing inside a spinning hexagon. The ball should be affected by gravity and friction, and it must bounce off the rotating walls realistically"
   - Result: Success on first attempt. Polygon drawn, rotation smooth, one bouncing ball added with natural physics.

2. **Multiple Object Physics**
   - Prompt: "@index.html add another 20 balls"
   - Result: Success. First Attempt. Several balls added.

3. **Object Interaction**
   - Prompt: "Now make it so that the balls should also collide against each other and affect each other"
   - Result: Fail. Several balls seem to build a revolting clump that brings itself outside of the boundaries of polygon
   - Note: Balls got stuck within themselves and pulled each other out of the boundaries

4. **Boundary Constraints**
   - Prompt: "Add limits so balls cannot escape the boundaries of the polygon"
   - Result: Partial success. Balls confined but still exhibited clustering issues
   - Note: Required switching from O3 Mini to Claude for image recognition capabilities

5. **Physics Refinement**
   - Prompt: "Fix balls getting stuck in energetic clusters, make them bounce naturally"
   - Result: Success. First Attempt. Smooth simulation achieved.

## Requirements

- Node.js (v12.0.0 or higher)
- npm (Node Package Manager)

## Installation

1. First, install Node.js and npm from [https://nodejs.org/](https://nodejs.org/)

2. Install http-server globally using npm:
```bash
npm install -g http-server
```

## Running the Examples

1. Open a terminal/command prompt
2. Navigate to the project directory:
```bash
cd path/to/snakeBuilder
```

3. Start the http-server:
```bash
http-server
```

4. Open your web browser and visit:
- http://localhost:8080/examples/rotatingPolygonSingleBall/
- http://localhost:8080/examples/rotatingPolygonMultipleBalls/
- http://localhost:8080/examples/rotatingPolygonLetters/

By default, http-server will run on port 8080. If that port is already in use, it will automatically choose the next available port.

## Troubleshooting

If you get a permission error when installing http-server globally on Unix-based systems (Linux/MacOS), try:
```bash
sudo npm install -g http-server
```

If you prefer not to install http-server globally, you can add it as a project dependency:
1. Initialize a package.json (if you haven't already):
```bash
npm init -y
```

2. Install http-server as a dev dependency:
```bash
npm install --save-dev http-server
```

3. Add a script to package.json:
```json
{
  "scripts": {
    "start": "http-server"
  }
}
```

4. Then run:
```bash
npm start
```