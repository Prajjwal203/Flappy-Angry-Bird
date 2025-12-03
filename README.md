Flappy Angry Bird

A simple, fun Flappy Bird-style game built with .NET — flap your way through pipes while an angry bird carries the hopes of your high score.
(Note: the project currently uses an angry-bird-style image for the player sprite — see Assets & Licensing below.)
Demo / Screenshots to check: (Assets\Screenshots)
    Screenshot-gamestart.png => Game start
    Screenshot-gameplay.png — In-game (mid-flap)
    Screenshot-gameover.png — Game over / score screen 
    Gameplay Recording (.mp4) 

Table of contents

About

Demo / Screenshots

Features

Requirements

Installation & Running

Controls

How it works (brief)

Configuration

Troubleshooting

Contributing

Assets & Licensing

License

Credits

About

Flappy Angry Bird is a lightweight Flappy Bird clone implemented in .NET. The gameplay follows the classic tap-to-flap mechanic: keep the bird airborne, avoid pipes, and chase the high score. The project is ideal as a small portfolio game, demonstration of simple game loops in .NET, or a learning exercise for 2D collision and basic physics.

Demo / Screenshots

Screenshot-gamestart.png => Game start

Screenshot-gameplay.png — In-game (mid-flap)

Screenshot-gameover.png — Game over / score screen

Gameplay Recording (.mp4) => in the same (Assets\Screenshots) folder

Features

Classic flap-to-fly mechanics (gravity and upward impulse).

Randomized pipe gaps and procedural pipe scrolling.

Score tracking and simple high-score memory (local).

Smooth frame-based movement using a game loop.

Keyboard and mouse control support.

Easy-to-read, modular .NET code (suitable for extension).

Requirements 

.NET SDK 6.0 or later recommended (works with .NET 7+).

Windows / macOS / Linux (if using cross-platform UI/back-end you included).

Optional: Visual Studio, Visual Studio Code, or JetBrains Rider for development.

If your project uses a specific UI framework (e.g., WinForms, WPF, MonoGame, SDL2#, Avalonia), make sure the appropriate runtime/framework is installed. Add here whichever framework your repo uses.

Installation & Running

Clone repository

git clone https://github.com/Prajjwal203/Flappy-Angry-Bird.git
cd Flappy-Angry-Bird


Restore and run

dotnet restore
dotnet run --project src/FlappyAngryBird/FlappyAngryBird.csproj


Build

dotnet build



Controls

Spacebar — Flap (give the bird an upward impulse)

Left Mouse Click — Flap

Escape — Pause / Quit to menu

Tip: Adjust input mapping in InputManager (or equivalent class).

How it works (brief)

A continuous game loop updates physics (gravity + velocity), moves obstacles left, and checks collisions each frame.

Pipes are spawned at regular intervals with randomized vertical offsets to create variety.

When the bird collides with a pipe or the ground, the game ends and the final score is shown.

The score increments as the bird successfully passes between pipes.

Configuration

You can tweak gameplay parameters (in GameSettings.cs or config.json) such as:

Gravity — downward acceleration.

FlapStrength — upward velocity applied on flap.

PipeSpawnInterval — time between pipes.

PipeSpeed — horizontal speed of pipes.

GapSize — vertical gap between top and bottom pipe.

Troubleshooting

Game doesn’t start — ensure the correct .NET SDK is installed; run dotnet --info.

Missing assets (images/sounds) — ensure assets folder is copied to output directory or embedded resources are configured.

Low framerate / stuttering — confirm you use a time-based update (delta time) rather than frame-based movement, and limit expensive per-frame allocations.

Contributing

Contributions are welcome! Suggested workflow:

Fork the repository.

Create a feature branch: feature/your-feature.

Make changes, include tests where reasonable.

Open a Pull Request with a clear description.

Please follow the code style used in the repository and keep changes focused and small.

Assets & Licensing

Important: The repository includes an angry-bird-style sprite for the player. That artwork is visually similar to a trademarked character. If you plan to distribute or publicize this project, consider:

Replacing the sprite with an original or openly licensed image (Creative Commons / public domain / your own art).

Confirming asset rights — do not use trademarked images in commercial or widely distributed projects without permission.

If you'd like, I can:

Suggest free sprite resources, or

Generate a small original sprite concept for use in the game.

License

This repository is released under the MIT License. You are free to use, modify, and distribute the code — see LICENSE for details.

If you include third-party assets (images/sounds), ensure their licenses are compatible with your distribution. Add a THIRD-PARTY-LICENSES.md if necessary.

Credits

Game code: Prajjwal.

Player sprite: angry-bird-style image (replace/credit appropriately).

Inspirations: Flappy Bird and classic 2D endless runner mechanics.
