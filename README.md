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

This is my current layout. Its Lower and Raise layers copy the Corne's, so the arrow, symbol and number positions match across both boards.

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
- Layer 1 is an exact copy of layer 0 and nothing switches to it, so in practice it isn't used.

#### Lower: arrows and symbols (hold LOWER, layer 2)

```
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┐
│       │       │  Home │   ↑   │  End  │  PgUp │       │   &   │   *   │   (   │   0   │       │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│       │       │   ←   │   ↓   │   →   │  PgDn │       │   $   │   %   │   ^   │       │  Del  │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│       │       │       │       │       │       │       │   !   │   @   │   #   │   )   │       │
├───────┼───────┼───────┼───────┼───────┼───────┴───────┼───────┼───────┼───────┼───────┼───────┤
│       │       │       │       │ (held)│               │       │       │       │       │       │
└───────┴───────┴───────┴───────┴───────┴───────────────┴───────┴───────┴───────┴───────┴───────┘
```

- Arrow keys are in an inverted T on R/S/T and F, with **Home/End** either side of ↑ and **PgUp/PgDn** next to them.
- The symbols on the right hand are the same as on the Corne's Lower layer.

#### Raise: numbers, media, wireless and lighting (hold RAISE, layer 3)

```
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┐
│       │   `   │  BT 1 │  BT 2 │  BT 3 │  2.4G │       │   7   │   8   │   9   │   -   │   =   │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│       │  Mute │  Vol- │  Vol+ │  Play │  Next │       │   4   │   5   │   6   │   [   │   ]   │
├───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┼───────┤
│       │ LED on│LEDmode│  LED- │  LED+ │  Logo │       │   1   │   2   │   3   │   0   │   \   │
├───────┼───────┼───────┼───────┼───────┼───────┴───────┼───────┼───────┼───────┼───────┼───────┤
│       │  USB  │Battery│       │       │               │ (held)│ Enter │   .   │       │       │
└───────┴───────┴───────┴───────┴───────┴───────────────┴───────┴───────┴───────┴───────┴───────┘
```

- The right hand is a number pad (same as the Corne's Raise layer), with **Enter** and **.** under the thumb.
- Media keys are on the left home row. Wireless connection keys are on the left top row: **BT 1–3**, **2.4G** (USB dongle) and **USB** (wired).
- Lighting keys are on the left bottom row. **Battery** shows the charge level on the LEDs.

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
│  USB  │  BT 1 │  BT 2 │  BT 3 │  2.4G │LEDmode│  →Mac │  →Win │   [   │   ]   │   \   │ LED on│
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

Things worth deciding on, comparing my Colemak-DH layout with the other boards:

- **Esc appears three times**: the Esc/Ctl home-row key, bottom left, and bottom right next to Del. Two of those spots could hold something more useful.
- **There are no F1–F12 keys anywhere.** The Planck has them on Raise. The Corne doesn't have them either.
- **There's no Adjust layer.** Holding Lower + Raise does nothing special, so wireless and lighting keys take up the left half of Raise. Moving them to a Lower + Raise layer, as on the Corne, would free that space.
- **Layer 1 is unused** (a duplicate of the base layer). It could become a QWERTY layer for other people, or a gaming layer.
- **The thumb keys differ between boards.** On the Corne the inner thumbs are Lower / Space and Esc / Raise. On the Geonix it's Lower / Space / Raise, with Cmd and Opt next to them. Matching them would make switching boards easier.
- **Ctrl is on the home row on all three boards** (Esc/Ctl here, Ctrl on the Corne), but the bottom-left key differs (Esc here, Ctrl on the Corne and Planck).

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
