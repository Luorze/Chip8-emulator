# CHIP-8 Emulator

A CHIP-8 emulator built with **C++ and SDL2**.

This project is a learning-focused implementation of the CHIP-8 virtual machine. It explores how a simple CPU fetches, decodes, and executes instructions, manages memory and registers, handles input, and renders graphics.

## ✨ Features

- CHIP-8 CPU state, registers, memory, stack, and program counter
- Instruction fetching, decoding, and execution using opcode dispatch tables
- CHIP-8 font data loaded into memory
- ROM loading
- 64 × 32 monochrome display
- Keyboard input mapped to the CHIP-8 hexadecimal keypad
- SDL2-based window and rendering
- Opcode testing with an external CHIP-8 test ROM

## 🛠️ Built With

- **C++** — emulator implementation
- **SDL2** — window, rendering, and keyboard input
- **VS Code** — development and debugging

## 📁 Project Structure

```text
chip-8-emulator/
├── .vscode/       # Build and debugging configuration
├── roms/
│   └── README.md  # Instructions for obtaining ROMs
├── src/
│   ├── chip8.cpp
│   ├── chip8.hpp
│   ├── main.cpp
│   └── platform.hpp
├── .gitignore
└── README.md
```

## 🚀 Getting Started

### Requirements

- A C++ compiler supporting C++17
- SDL2 development libraries
- Git (optional, for cloning the project)
- A CHIP-8 ROM file

The included VS Code build configuration is designed for **Windows with MSYS2 UCRT64 and SDL2**. Other platforms may require different compiler and linker settings.

### Build on Windows with VS Code

1. Install a C++ compiler and SDL2 through MSYS2 UCRT64.
2. Open this project folder in VS Code.
3. Ensure the compiler and SDL2 include/library paths in `.vscode/tasks.json` match your installation.
4. Build using **Ctrl + Shift + B**.

The build task produces `chip8.exe` in the project root.

### Run the Emulator

The emulator accepts three command-line arguments:

```text
chip8.exe <Scale> <Delay> <ROM>
```

- `Scale` — integer multiplier for the display size.
- `Delay` — cycle delay in milliseconds.
- `ROM` — path to the CHIP-8 ROM file.

Example in PowerShell:

```powershell
.\chip8.exe 10 3 ".\roms\test_opcode.ch8"
```

The example assumes you've placed `test_opcode.ch8` at that path. ROM files are not included in this repository; see the testing section below.

## 🎮 Keyboard Mapping

The CHIP-8 hexadecimal keypad is mapped to the keyboard as follows:

| CHIP-8 | Keyboard |
|---|---|
| `1 2 3 C` | `1 2 3 4` |
| `4 5 6 D` | `Q W E R` |
| `7 8 9 E` | `A S D F` |
| `A 0 B F` | `Z X C V` |

Press **Escape** to quit the emulator.

## 🧪 Testing

### Opcode Test ROM

The emulator was initially tested with the CHIP-8 test ROM by corax89:

- [corax89/chip8-test-rom](https://github.com/corax89/chip8-test-rom)

This ROM helps check whether CHIP-8 instructions behave as expected. Visual output alone does not guarantee that every instruction passes.

### Additional ROMs

For more programs and games to try, see:

- [dmatlack/chip8 — ROMs and games](https://github.com/dmatlack/chip8/tree/master/roms/games)

ROM compatibility may vary depending on instruction behavior, timing, and implementation details.

**Note:** ROM files are kept out of this repository. Obtain them from their original sources and follow their respective licensing and distribution terms.

## 📚 References & Learning Resources

These resources helped guide the implementation and testing of this project:

1. **Emulator implementation tutorial** — [Building a CHIP-8 Emulator in C++](https://austinmorlan.com/posts/chip8_emulator/) by Austin Morlan.
2. **Instruction set and technical reference** — [Cowgod's CHIP-8 Technical Reference](http://devernay.free.fr/hacks/chip8/C8TECH10.HTM).
3. **Initial opcode testing** — [corax89/chip8-test-rom](https://github.com/corax89/chip8-test-rom).
4. **Additional ROMs and games** — [dmatlack/chip8 games directory](https://github.com/dmatlack/chip8/tree/master/roms/games).

## 🗺️ Future Improvements

- Verify instruction behavior against a broader test suite
- Improve CPU and timer scheduling
- Test compatibility with more CHIP-8 programs
- Add screenshots and gameplay demonstrations
- Improve build portability across operating systems

## 🎯 Project Goal

The goal of this project was to learn the fundamentals of emulation, bitwise operations, instruction decoding, memory management, and low-level graphics through a small but practical C++ project. This project was very fun and I hope to make more complex emulators next.

---

Soham :)
