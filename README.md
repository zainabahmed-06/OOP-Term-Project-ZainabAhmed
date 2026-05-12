# Tower Defense Game
A tower defense game written in C++ with SFML graphics, music, and input handling.

## Compiling and Running the Game - 
### Requirements

- Windows OS
- Visual Studio 2022 
- SFML 3.1.0 or later

### Steps
1. Install SFML
2. Create a new project in Visual Studio and configure the project.
   - Go to Project → Properties
   - Under `C/C++ → General → Additional Include Directories`, add the path to SFML's include folder (e.g. `C:\SFML\include`)
   - Under `Linker → General → Additional Library Directories`, add the path to SFML's lib folder (e.g. `C:\SFML\lib`)
   - Under `Linker → Input → Additional Dependencies`, add the following:
     ` sfml-graphics.lib
     sfml-window.lib
     sfml-system.lib
     sfml-audio.lib`
   - For Debug mode, use the `-d` variants (e.g. `sfml-graphics-d.lib`)
3. Copy the SFML DLL files from `SFML/bin` into the folder where your `.exe` is generated (usually `x64/Debug` or `x64/Release`).
4. Copy all asset files (images, fonts, audio files) into the same folder as the .exe:
   - background.png
   - cannontower.png, snipertower.png, machineguntower.png, slowtower.png
   - basicenemy.png, fastenemy.png, tankenemy.png, flyingenemy.png
   - Roboto-Regular.ttf
   - backgroundmusic.ogg, wingame.ogg, lostgame.ogg
5. Build and run the project in Visual Studio

### Installing GUI Library - SFML
1. Go to https://www.sfml-dev.org/download/sfml/3.1.0/
2. Download the version matching your Visual Studio compiler (e.g. Visual C++ 17 (2022) - 64-bit).
3. Extract the downloaded zip to a location on your computer (e.g. `C:\SFM`L).
4. Follow the configuration steps in the Compile and Run section above to link SFML to your Visual Studio project.

### How to Play:
1. Drag a tower from the Towers Shop sidebar on the right and drop it anywhere on the map to place it.
2. Towers will automatically attack enemies that come into their range.
3. Earn gold by killing enemies and spend it on placing more towers.
4. Win the game by surviving all 5 waves.
5. If enemies reach the exit, and you use up all 10 lives, game over.

### Known Issues and Limitations:
1. The game currently has a fixed total of 5 waves with no additional content beyond that.
2. There is no pause button — once the game starts, it cannot be paused.
3. There is no save/load system — progress is lost when the game is closed.
4. Towers cannot be sold or upgraded through the UI once placed.
5. The game window is a fixed resolution of 1224x768 and cannot be resized.
6. All asset files must be placed in the same directory as the executable or they will not load.
