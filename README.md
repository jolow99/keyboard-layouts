# Keyboard layouts

My layouts for three keyboards:

| Keyboard | Firmware | Files |
|---|---|---|
| **Corne LP** (split, wireless, nice!nano v2) | [ZMK](https://zmk.dev) | [`config/corne.keymap`](config/corne.keymap), [`config/corne.conf`](config/corne.conf) |
| **Planck rev6** (Drop/Massdrop, wired) | [QMK](https://qmk.fm) | [`planck/keymap.c`](planck/keymap.c), [`planck/keymap.json`](planck/keymap.json) |
| **Geonix Rev 2.5** (40%, wireless, 2u spacebar) | [Vial](https://get.vial.today) | [`geonix/colemak-dh.vil`](geonix/colemak-dh.vil) (mine), [`geonix/default.vil`](geonix/default.vil) (factory) |

All three boards share the same idea: a **Colemak-DH** letter layout, a **Lower** layer for arrows and symbols, a **Raise** layer for numbers, and an **Adjust** layer you reach by holding Lower and Raise together.

**How to read the diagrams**

- **Cmd** is the GUI key (Cmd on macOS, Windows key on Windows). **Opt** is Alt/Option.
- **LOWER**, **RAISE** and **ADJUST** are hold keys: the layer stays on while you hold them.
- **(held)** marks the key you are holding to be on that layer.
- A blank key does nothing on the Planck. On the Corne and the Geonix it falls through to the base layer, so it types the same thing as on the base layer.

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

## Geonix Rev 2.5 (Vial)

The Geonix is configured live in the [Vial](https://get.vial.today) app, with no flashing needed. To load a layout, open Vial, then choose *File → Load saved layout* and pick a `.vil` file from [`geonix/`](geonix/). Neither file uses tap dance, combos, macros or key overrides. Everything is in the layers below.

The bottom row has a **2u spacebar** and one less key than the rows above it.

### My layout: Colemak-DH ([`geonix/colemak-dh.vil`](geonix/colemak-dh.vil))

This is my main layout. It's built around using the mouse less:

- **LOWER is for navigation and editing.** Your left hand gets the commands and modifiers, your right hand gets the arrows.
- **RAISE is for numbers, F-keys and the wireless settings.**

The previous version, which copied the Corne's Lower and Raise layers, is kept in [`geonix/colemak-dh-v1.vil`](geonix/colemak-dh-v1.vil). Load that file in Vial to switch back.

#### Base (layer 0)

```
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┐
│  Tab  │   Q   │   W   │   F   │   P   │   B   │   J   │   L   │   U   │   Y   │   ;   │  Bksp │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│Esc/Ctl│   A   │   R   │   S   │   T   │   G   │   M   │   N   │   E   │   I   │   O   │   '   │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│ Shift │   Z   │   X   │   C   │   D   │   V   │   K   │   H   │   ,   │   .   │   /   │ Enter │
├───────┼───────┼───────┼───────┼───────┼───────┴───────┼───────┼───────┼───────┼───────┼───────┤
│  Esc  │  Ctrl │  Opt  │  Cmd  │ LOWER │     Space     │ RAISE │  RCmd │  ROpt │  Esc  │  Del  │
└───────┴───────┴───────┴───────┴───────┴───────────────┴───────┴───────┴───────┴───────┴───────┘
```

- **Esc/Ctl** is a dual-purpose key: tap it for Esc, hold it for Ctrl.
- Layer 1 must stay an exact copy of layer 0. The Geonix firmware switches layer 1 on by itself at startup when the board is in Mac mode, so anything different there would replace your base keys. That also leaves no free layer for a Lower + Raise "Adjust" layer: the board only has 4.

#### Lower: navigation and editing (hold LOWER, layer 2)

```
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┐
│       │       │ Tab ← │ Tab → │       │  PgUp │       │       │   ↑   │       │       │       │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│       │  Ctrl │  Opt  │  Cmd  │ Shift │  PgDn │       │   ←   │   ↓   │   →   │  Bksp │  Del  │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│       │  Undo │  Cut  │  Copy │ Paste │       │       │  Mute │  Vol- │  Vol+ │  Play │  Next │
├───────┼───────┼───────┼───────┼───────┼───────┴───────┼───────┼───────┼───────┼───────┼───────┤
│       │       │       │       │ (held)│               │       │       │       │       │       │
└───────┴───────┴───────┴───────┴───────┴───────────────┴───────┴───────┴───────┴───────┴───────┘
```

**Left hand** (works one-handed while the right hand is on the mouse):
- **Tab ← / Tab →** go to the previous and next tab (Cmd+Shift+[ and Cmd+Shift+]). This works in browsers, VS Code, Finder and Terminal.
- **Undo / Cut / Copy / Paste** are Cmd+Z / X / C / V.
- **PgUp / PgDn** scroll one screen up or down.
- **Ctrl / Opt / Cmd / Shift** are on the home row, so you can hold them while the right hand uses the arrows.

**Right hand:**
- **Arrows** are in an inverted T, plus **Bksp** and **Del**.
- **Media keys** are on the bottom row: Mute, Vol-, Vol+, Play/Pause, Next.

**How to move and edit without the mouse.** The modifier decides how far a key goes, and the rule is the same for moving, selecting and deleting:

| | Arrow keys | Bksp |
|---|---|---|
| no modifier | one character | delete a character |
| **Opt** (left ring) | one **word** | delete a **word** |
| **Cmd** (left middle) | to the start/end of the **line**, or ↑/↓ to the top/bottom of the document | delete to the start of the **line** |
| add **Shift** (left index) | select instead of move | |

For example, hold LOWER, then Opt + Shift with your left hand, and tap → twice: that selects the next two words.

> Ctrl+Backspace is the **Windows** shortcut for deleting a word. On a Mac it only deletes one character.

#### Raise: numbers, F-keys and wireless (hold RAISE, layer 3)

```
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┐
│  BT 1 │   F1  │   F2  │   F3  │   F4  │  USB  │   `   │   7   │   8   │   9   │   -   │   =   │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│  BT 2 │   F5  │   F6  │   F7  │   F8  │  2.4G │       │   4   │   5   │   6   │   [   │   ]   │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│  BT 3 │   F9  │  F10  │  F11  │  F12  │Battery│       │   1   │   2   │   3   │   0   │   \   │
├───────┼───────┼───────┼───────┼───────┼───────┴───────┼───────┼───────┼───────┼───────┼───────┤
│  LEDs │       │       │       │       │               │ (held)│ Enter │   .   │       │       │
└───────┴───────┴───────┴───────┴───────┴───────────────┴───────┴───────┴───────┴───────┴───────┘
```

- **The right hand is a number pad** (7-8-9 on top, 0 at the bottom right), with `` ` `` `-` `=` `[` `]` `\` around it. **Enter** and **.** are under the thumb.
- **Symbols are the shifted numbers**, so hold Shift (left pinky) while on Raise: Shift+7 = `&`, Shift+4 = `$`, Shift+1 = `!`, and so on.
- **F1–F12** are on the left in a 4×3 block.
- **BT 1–3 / 2.4G / USB** pick the connection. **Battery** shows the charge on the LEDs.
- **LEDs** turns all the backlighting on or off, and the board remembers the setting. The light that shows when you hold LOWER or RAISE is built into the Geonix firmware and can't be turned off from Vial.

### Factory default: QWERTY ([`geonix/default.vil`](geonix/default.vil))

This is the layout the board shipped with. It's kept for reference and as a reset point.

#### Base: Windows mode (layer 0)

```
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┐
│  Tab  │   Q   │   W   │   E   │   R   │   T   │   Y   │   U   │   I   │   O   │   P   │  Bksp │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│  Esc  │   A   │   S   │   D   │   F   │   G   │   H   │   J   │   K   │   L   │   ;   │   '   │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│ Shift │   Z   │   X   │   C   │   V   │   B   │   N   │   M   │   ,   │   .   │   ↑   │ Enter │
├───────┼───────┼───────┼───────┼───────┼───────┴───────┼───────┼───────┼───────┼───────┼───────┤
│   Fn  │  Del  │  Ctrl │  Opt  │  Cmd  │     Space     │  RCmd │   /   │   ←   │   ↓   │   →   │
└───────┴───────┴───────┴───────┴───────┴───────────────┴───────┴───────┴───────┴───────┴───────┘
```

Layer 1 is the **Mac mode** copy of this layer, with **Opt** and **Cmd** swapped. **Fn → →Mac / →Win** switches between the two modes.

#### Fn layer (hold Fn, layers 2 and 3)

```
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┐
│  USB  │  BT 1 │  BT 2 │  BT 3 │  2.4G │LEDmode│  →Mac │  →Win │   [   │   ]   │   \   │  LEDs │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│   `   │   1   │   2   │   3   │   4   │   5   │   6   │   7   │   8   │   9   │   0   │   -   │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│ Shift │  Ins  │  Del  │  Home │  End  │  PgUp │  PgDn │   M   │   ,   │   .   │  LED+ │  Logo │
├───────┼───────┼───────┼───────┼───────┼───────┴───────┼───────┼───────┼───────┼───────┼───────┤
│ (held)│ Debnce│Battery│ Sleep │  Cmd  │     Reset     │  RCmd │   =   │LEDspd-│  LED- │LEDspd+│
└───────┴───────┴───────┴───────┴───────┴───────────────┴───────┴───────┴───────┴───────┴───────┘
```

- The number row is on the home row, with `` ` `` and `-` at the ends. Brackets, `\` and `=` sit at the top right and bottom right.
- Editing keys (Ins, Del, Home, End, PgUp, PgDn) are on the bottom-left letter row.
- **USB / BT 1–3 / 2.4G** pick the connection. **→Mac / →Win** pick the OS mode.
- The bottom row has board settings: **Debnce** (debounce), **Battery**, **Sleep** and **Reset**. Space becomes **Reset**, which probably restores the factory settings, so be careful with Fn + Space.
- Layer 3 is the same as layer 2, except the key next to the spacebar is Opt instead of Cmd (the Mac-mode version).

> The `Debnce`, `Sleep`, `Reset` and `Logo` keys are custom Geonix firmware keys, shown in Vial as `USER05`, `USER11` and so on. Their meanings come from the keyboard's Vial definition in the manufacturer's QMK source, so a couple of them may behave slightly differently on your board.

### Notes for improving the layout

Done in the current version: arrows and modifiers on Lower, dedicated tab-switching keys, F1–F12, and Cmd-based Undo/Cut/Copy/Paste.

Still open:

- **Esc appears three times**: the Esc/Ctl home-row key, bottom left, and bottom right next to Del. Two of those spots could hold something more useful.
- **The Corne and Planck still use the old setup** (arrows on the left, symbols on Lower). Updating them to match would make switching boards easier.
- **The thumb keys differ between boards.** On the Corne the inner thumbs are Lower / Space and Esc / Raise. On the Geonix it's Lower / Space / Raise, with Cmd and Opt next to them.

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
