# Dodgy Cube (MARS) — MIPS Assembly Game

A small **MIPS assembly** arcade game made for **MARS** using the **Bitmap Display** tool.

You control a cube and must **dodge falling obstacles** to avoid losing health, while **collecting coins/points** to increase your score and win.

## Gameplay

- **Player:** A cube you move around the screen.
- **Hazards:** Falling objects (spikes) that reduce your health on contact.
- **Collectibles:** Coins that increase your score.
- **Goal:** Survive and collect enough points to win.

## Health & Score

- You start with **3 health**.
- Getting hit by a falling hazard reduces health.
- Collecting coins increases score.

## Requirements

- **MARS MIPS Simulator** (recommended version used in most courses)
- MARS **Tools → Bitmap Display**

## How to Run (MARS)

1. Open MARS.
2. Open the game `.asm` file.
3. Assemble: **Run → Assemble**.
4. Configure the bitmap:
   - Open **Tools → Bitmap Display**
   - Set:
     - **Unit Width:** `2`
     - **Unit Height:** `2`
     - **Display Width (pixels):** `512`
     - **Display Height (pixels):** `512`
     - **Base address:** `0x10010000`
   - Click **Connect to MIPS**
5. Run: **Run → Go**.

### Important

The game expects the Bitmap Display base address to match the value in the code:

- `display_address: .word 0x10010000`

If the Bitmap Display base address does not match, you’ll typically see a blank/garbled screen.

## Controls

To play the game after oppening the display in MARS you should also Open the Keyboard pannel and connect both of them to MIPS

## Project Notes (from the code)

Some core values used by the game:

- Bitmap base: `0x10010000`
- Colors:
  - Cube: blue (`0x00006DCC`)
  - Spikes: red (`0x00FF0000`)
  - Coins: yellow (`0x00F7F72A`)
- Starting health: `3`

## Troubleshooting

- **Blank screen:** Ensure Bitmap Display is connected and base address is `0x10010000`.
- **Wrong scale/positioning:** Ensure unit size is `2x2` and display is `512x512`.
- **Assemble errors:** Make sure you’re running in **MARS** (not QtSPIM), and paste the exact error message to debug quickly.

## Credits

Made in MIPS assembly for MARS as a simple dodge-and-collect arcade game.
