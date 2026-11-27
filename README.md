# Keyboard layouts

My layouts for two keyboards:

| Keyboard | Firmware | Files |
|---|---|---|
| **Corne LP** (split, wireless, nice!nano v2) | [ZMK](https://zmk.dev) | [`config/corne.keymap`](config/corne.keymap), [`config/corne.conf`](config/corne.conf) |
| **Planck rev6** (Drop/Massdrop, wired) | [QMK](https://qmk.fm) | [`planck/keymap.c`](planck/keymap.c), [`planck/keymap.json`](planck/keymap.json) |

Both boards share the same idea: a **Colemak-DH** letter layout, a **Lower** layer for arrows and symbols, a **Raise** layer for numbers, and an **Adjust** layer you reach by holding Lower and Raise together.

**How to read the diagrams**

- **Cmd** is the GUI key (Cmd on macOS, Windows key on Windows). **Opt** is Alt/Option.
- **LOWER**, **RAISE** and **ADJUST** are hold keys: the layer stays on while you hold them.
- **(held)** marks the key you are holding to be on that layer.
- A blank key does nothing on the Planck. On the Corne it falls through to the base layer, so it types the same thing as on the base layer.

---

## Corne LP (ZMK)

Holding **LOWER + RAISE** together opens Adjust. The order you press them in doesn't matter.

### Base: Colemak-DH

```
┌───────┬───────┬───────┬───────┬───────┬───────┐   ┌───────┬───────┬───────┬───────┬───────┬───────┐
│  Tab  │   Q   │   W   │   F   │   P   │   B   │   │   J   │   L   │   U   │   Y   │   ;   │  Bksp │
├───────┼───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┼───────┤
│  Ctrl │   A   │   R   │   S   │   T   │   G   │   │   M   │   N   │   E   │   I   │   O   │   '   │
├───────┼───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┼───────┤
│ Shift │   Z   │   X   │   C   │   D   │   V   │   │   K   │   H   │   ,   │   .   │   /   │ Enter │
└───────┴───────┴───────┴───────┴───────┴───────┘   └───────┴───────┴───────┴───────┴───────┴───────┘
                        ┌───────┬───────┬───────┐   ┌───────┬───────┬───────┐
                        │  Cmd  │ LOWER │ Space │   │  Esc  │ RAISE │  Opt  │
                        └───────┴───────┴───────┘   └───────┴───────┴───────┘
```

Ctrl is on the home row where Caps Lock usually is, and Esc is the right inner thumb.

### Lower: arrows and symbols (hold LOWER)

```
┌───────┬───────┬───────┬───────┬───────┬───────┐   ┌───────┬───────┬───────┬───────┬───────┬───────┐
│  Tab  │       │       │   ↑   │       │       │   │       │   &   │   *   │   (   │   0   │  Bksp │
├───────┼───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┼───────┤
│  Ctrl │       │   ←   │   ↓   │   →   │       │   │       │   $   │   %   │   ^   │       │       │
├───────┼───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┼───────┤
│ Shift │       │       │       │       │       │   │       │   !   │   @   │   #   │   )   │       │
└───────┴───────┴───────┴───────┴───────┴───────┘   └───────┴───────┴───────┴───────┴───────┴───────┘
                        ┌───────┬───────┬───────┐   ┌───────┬───────┬───────┐
                        │  Cmd  │ (held)│ Space │   │ Enter │ ADJUST│  Opt  │
                        └───────┴───────┴───────┘   └───────┴───────┴───────┘
```

- Arrow keys are under the left hand, in an inverted T on W/R/S/T.
- The right hand has the shifted-number symbols `! @ #`, `$ % ^`, `& * (` and `)`, roughly where they sit above the numbers on the Raise layer.
- The right inner thumb becomes **Enter**.

### Raise: numbers and brackets (hold RAISE)

```
┌───────┬───────┬───────┬───────┬───────┬───────┐   ┌───────┬───────┬───────┬───────┬───────┬───────┐
│  Tab  │   `   │       │       │       │       │   │       │   7   │   8   │   9   │   -   │   =   │
├───────┼───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┼───────┤
│  Ctrl │       │       │       │       │       │   │       │   4   │   5   │   6   │   [   │   ]   │
├───────┼───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┼───────┤
│ Shift │       │       │       │       │       │   │       │   1   │   2   │   3   │   0   │   \   │
└───────┴───────┴───────┴───────┴───────┴───────┘   └───────┴───────┴───────┴───────┴───────┴───────┘
                        ┌───────┬───────┬───────┐   ┌───────┬───────┬───────┐
                        │  Cmd  │ ADJUST│ Space │   │ Enter │ (held)│  Opt  │
                        └───────┴───────┴───────┘   └───────┴───────┴───────┘
```

- The right hand is a number pad (7-8-9 on top, 0 at the bottom right).
- `-` `=` `[` `]` `\` and `` ` `` live here too.
- The right inner thumb becomes **Enter**.

### Adjust: Bluetooth and media (hold LOWER + RAISE)

```
┌───────┬───────┬───────┬───────┬───────┬───────┐   ┌───────┬───────┬───────┬───────┬───────┬───────┐
│       │       │       │       │       │       │   │  Vol+ │       │       │       │       │       │
├───────┼───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┼───────┤
│ BT Clr│  BT 1 │  BT 2 │  BT 3 │  BT 4 │  BT 5 │   │  Vol- │       │       │       │       │       │
├───────┼───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┼───────┤
│       │ BT out│       │       │       │       │   │  Play │       │       │       │       │       │
└───────┴───────┴───────┴───────┴───────┴───────┘   └───────┴───────┴───────┴───────┴───────┴───────┘
                        ┌───────┬───────┬───────┐   ┌───────┬───────┬───────┐
                        │       │ (held)│       │   │       │ (held)│       │
                        └───────┴───────┴───────┘   └───────┴───────┴───────┘
```

- **BT 1–5** switch between the five paired devices. **BT Clr** forgets the pairing on the current profile.
- **BT out** sends keystrokes over Bluetooth even when USB is plugged in.
- **Vol+ / Vol- / Play** are media keys.

### Building and flashing

Every push runs GitHub Actions ([`.github/workflows/build.yml`](.github/workflows/build.yml), with the targets in [`build.yaml`](build.yaml)). The build produces `corne_left` and `corne_right` firmware for the nice!nano v2. Download the artifact from the Actions run, double-tap reset on each half, and drag the matching `.uf2` onto the drive that appears.

---

## Planck rev6 (QMK)

On the Planck, holding **LOWER + RAISE** together opens Adjust.

### Layer 0: QWERTY (default)

```
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┐
│  Tab  │   Q   │   W   │   E   │   R   │   T   │   Y   │   U   │   I   │   O   │   P   │  Bksp │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│  Esc  │   A   │   S   │   D   │   F   │   G   │   H   │   J   │   K   │   L   │   ;   │   '   │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│ Shift │   Z   │   X   │   C   │   V   │   B   │   N   │   M   │   ,   │   .   │   /   │ Enter │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│  Ctrl │       │  Cmd  │  Opt  │ LOWER │       │ Space │ RAISE │       │   -   │   =   │   \   │
└───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┘
```

### Layer 1: Colemak-DH

```
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┐
│  Tab  │   Q   │   W   │   F   │   P   │   B   │   J   │   L   │   U   │   Y   │   ;   │  Bksp │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│  Esc  │   A   │   R   │   S   │   T   │   G   │   M   │   N   │   E   │   I   │   O   │   '   │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│ Shift │   Z   │   X   │   C   │   D   │   V   │   K   │   H   │   ,   │   .   │   /   │ Enter │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│  Ctrl │       │  Cmd  │  Opt  │ LOWER │       │ Space │ RAISE │ RShift│   -   │   =   │   \   │
└───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┘
```

Switch between QWERTY and Colemak-DH on the Adjust layer. The board remembers your choice until it is unplugged.

> The bottom row is drawn as a plain 12-key grid. On a 2u spacebar the space key covers the blank spot to its left.

### Layer 2: Lower (hold LOWER)

```
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┐
│   `   │       │  Copy │   ↑   │ Paste │       │       │   &   │   *   │   (   │       │  Del  │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│       │  Undo │   ←   │   ↓   │   →   │  Cut  │       │   $   │   %   │   ^   │       │  PgUp │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│ Shift │       │       │       │       │       │       │   !   │   @   │   #   │   )   │  PgDn │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│  Ctrl │       │       │       │ (held)│       │ Space │ ADJUST│       │       │       │       │
└───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┘
```

- Arrow keys are under the left hand, in an inverted T on W/S/D/F (QWERTY positions).
- **Undo / Cut / Copy / Paste** are around the arrows. These send the dedicated HID editing keys, which work on Linux but are ignored by macOS and most Windows apps.
- The right hand has the shifted-number symbols `! @ #`, `$ % ^`, `& * (` and `)`.
- **Del**, **PgUp** and **PgDn** are on the right edge.

### Layer 3: Raise (hold RAISE)

```
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┐
│   `   │       │       │       │       │       │       │   7   │   8   │   9   │       │  Bksp │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│       │   F1  │   F2  │   F3  │   F4  │   F5  │   F6  │   4   │   5   │   6   │   [   │   ]   │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│ Shift │   F7  │   F8  │   F9  │  F10  │  F11  │  F12  │   1   │   2   │   3   │   0   │ Enter │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│  Prev │  Vol- │  Vol+ │  Next │ ADJUST│       │  Play │ (held)│       │       │       │       │
└───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┘
```

- The right hand is a number pad (7-8-9 on top, 0 at the bottom right), with `[` `]` next to it.
- **F1–F12** run across the left and middle of the board.
- Media keys are on the bottom row: previous, volume down, volume up, next, play/pause.

### Layer 4: Adjust (hold LOWER + RAISE)

```
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┐
│       │  BOOT │ QWERTY│Colemak│       │       │       │Click L│ Mouse↑│Click R│       │       │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│       │       │MusMode│ AudOff│ AudOn │       │       │ Mouse←│ Mouse↓│ Mouse→│       │       │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│       │ Voice-│ Voice+│ MusOn │ MusOff│       │       │       │       │       │       │       │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│       │       │       │       │ (held)│       │       │ (held)│       │       │       │       │
└───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┘
```

- **BOOT** puts the Planck into bootloader mode so you can flash new firmware. It does the same as the reset button on the bottom.
- **QWERTY / Colemak** sets the default letter layer.
- The right hand has mouse keys: move the cursor, plus left and right click.
- The audio keys are on the left: audio on/off, music mode on/off, music mode cycle, and voice +/-.

### Files

- [`planck/keymap.c`](planck/keymap.c) is the QMK keymap. Copy it to `keyboards/planck/keymaps/<name>/keymap.c` in a [qmk_firmware](https://github.com/qmk/qmk_firmware) checkout and build it with `qmk compile -kb planck/rev6 -km <name>`.
- [`planck/keymap.json`](planck/keymap.json) is the same layout for the [QMK Configurator](https://config.qmk.fm) web app (use *Import*).
- [`planck/planck_rev6_firmware_backup.bin`](planck/planck_rev6_firmware_backup.bin) is the exact firmware that was on the board when this keymap was recovered (Nov 2026). To restore it, put the board in bootloader mode and run:

  ```sh
  dfu-util -a 0 -d 0483:df11 -s 0x08000000:leave -D planck/planck_rev6_firmware_backup.bin
  ```

> The keymap was recovered by reading it out of that firmware, because the original source was lost. `keymap.c` uses current QMK key names but has not been compiled yet. The Colemak layer has a Right Shift in the bottom row where QWERTY has nothing. That is how it is on the board.
