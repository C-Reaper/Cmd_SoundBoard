# Project README

## Overview
This project is a C application that demonstrates the use of a soundboard library across multiple platforms: Linux, Windows, Wine (Windows compatibility on Linux), and WebAssembly. The application initializes a soundboard with specified parameters, starts it in a separate thread, sets a buffer of random values to play, and then joins the thread before cleaning up.

## Features
- Cross-platform support: Linux, Windows, Wine, and WebAssembly.
- Initialization of a soundboard with configurable parameters (channels, bits per sample, sample rate).
- Playback of a simple buffer in a separate thread.

## Project Structure

### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed:
  - Linux: ALSA for audio handling.
  - Windows & Wine: No specific libraries required as the project is cross-platform compatible.
  - WebAssembly: No external libraries are required.

## Build & Run

### Linux
To build and run on Linux:

```bash
cd <Project>
make -f Makefile.linux all       # build output
make -f Makefile.linux do        # build + exe output
make -f Makefile.linux clean      # Remove build artifacts
make -f Makefile.linux exe        # Execute it with make
```

### Windows
To build and run on Windows:

```bash
cd <Project>
make -f Makefile.windows all       # build output
make -f Makefile.windows do        # build + exe output
make -f Makefile.windows clean      # Remove build artifacts
make -f Makefile.windows exe        # Execute it with make
```

### Wine (Windows Compatibility on Linux)
To build and run on Linux using Wine:

```bash
cd <Project>
make -f Makefile.wine all         # build output
make -f Makefile.wine do          # build + exe output
make -f Makefile.wine clean        # Remove build artifacts
make -f Makefile.wine exe          # Execute it with make
```

### WebAssembly (Emscripten)
To build and run on the web using Emscripten:

```bash
cd <Project>
make -f Makefile.web all           # build output
make -f Makefile.web do            # build + exe output
make -f Makefile.web clean          # Remove build artifacts
make -f Makefile.web exe            # Execute it with make (requires wasmtime)
```

These commands will help you build and execute the project on the specified platforms.