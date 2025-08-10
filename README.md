My zmk config for my keyboards from keebart.com



# The corne layout
![](my_keymap.png)


# My piantor layout
![](piantor.svg)

https://keymap-drawer.streamlit.app

# My ZMK Config for Keyboards from Keebart.com

[Keymap Drawer](https://keymap-drawer.streamlit.app)

This repository contains my custom ZMK firmware configurations for ergonomic split keyboards like the Piantor Pro BT and Corne Pro BT (or similar variants like Corne 4.1). The keymaps are optimized for QWERTY with Swedish locale support (`locale/keys_sv.h`), focusing on programming symbols for Java, Python, and Bash development. I've recently updated the combos to a new chorded system for better ergonomics and efficiency.

## New Combo System

I've developed a new combo system using chorded key presses (pressing two keys simultaneously within a 50ms timeout). This replaces the previous mappings with a more intuitive, visualization-friendly approach. Combos are divided into single-side (same hand) and dual-side (both hands) for balanced use.

### Design Philosophy
- **Single-Side Combos**: Use keys from the same hand for paired or isolated symbols (e.g., brackets, quotes). Reduces stretching and allows one-handed input.
- **Dual-Side Combos**: Span both hands for operators and punctuation, encouraging deliberate, balanced typing.
- **Key Selection**: Based on adjacent QWERTY pairs (e.g., "qw" for Q+W). Swedish keys like ö are integrated naturally.
- **Unused Slots ("nop")**: Some dual-side combos are left unmapped for now, to avoid accidents or for future use.
- **Ergonomics**: Prioritizes home-row and adjacent fingers; no same-finger verticals. Timeout is 50ms—adjust if needed.
- **Compatibility**: Works on base layer (0). For Swedish macOS users, set input source to U.S. (System Settings > Keyboard > Input Sources) to fix issues like `[` rendering as Å.

### How to Use
1. Press the two keys in the combo nearly simultaneously.
2. No modifiers needed—these are pure combos.
3. Test in a text editor after flashing.
4. Customize in the `.keymap` file's `combos` section.

### Combo Visualization
Tables show key pairs (e.g., "qw") and triggered symbols (e.g., "`"). "split" separates left/right hands.

### Single-Side Combos
| Left Hand        |                |                | Split | Right Hand     |                |                  |
|------------------|----------------|----------------|-------|----------------|----------------|------------------|
| qw<1,2>("nop")   | we<2,3>("/")   | er<3,4>("{")   |       | ui<7,8>("}")   | io<8,9>("\")   | op<9,10>("nop")  |
| as<13,14>("nop") | sd<14,15>("<") | df<15,16>("(") |       | jk<19,20>(")") | kl<20,21>(">") | lö<21,22>("nop") |
| zx<25,26>("nop") | xc<26,27>("^") | cv<27,28>("[") |       | ,.<31,32>("]") | m,<32,33>("$") | .-<33,34>("nop") |

### Dual-Side Combos
| Top Row          |                |                |                   |                |
|------------------|----------------|----------------|-------------------|----------------|
| qp<1,10>("nop")  | wo<2,9>("*")   | ei<3,8>("?")   | ru<4,7>("!")      | ty<5,6>("@")   |
| aö<13,22>("%")   | sl<14,21>("=") | dk<15,20>("'") | fj<16,19>("\"")   | gh<17,18>("&") |
| z-<25,34>("~")   | x.<26,33>("+") | c,<27,32>("`") | vm<28,31>("pipe") | bn<29,30>("#") |



## Piantor Pro BT Combo Reference (Updated)

| Symbol | Keys to Press | Key Positions | Description |
|--------|---------------|---------------|-------------|
| /     | W + E          | <2 3>         | Forward slash |
| {     | E + R          | <3 4>         | Left curly brace |
| }     | U + I          | <7 8>         | Right curly brace |
| \\    | I + O          | <8 9>         | Backslash |
| <     | S + D          | <14 15>       | Less-than sign |
| (     | D + F          | <15 16>       | Left parenthesis |
| )     | J + K          | <19 20>       | Right parenthesis |
| >     | K + L          | <20 21>       | Greater-than sign |
| ^     | X + C          | <26 27>       | Caret |
| [     | C + V          | <27 28>       | Left square bracket |
| ]     | , + .          | <31 32>       | Right square bracket |
| $     | M + ,          | <32 33>       | Dollar sign |
| *     | W + O          | <2 9>         | Asterisk |
| ?     | E + I          | <3 8>         | Question mark |
| !     | R + U          | <4 7>         | Exclamation mark |
| @     | T + Y          | <5 6>         | At sign |
| %     | A + Ö          | <13 22>       | Percent sign |
| =     | S + L          | <14 21>       | Equals sign |
| '     | D + K          | <15 20>       | Single quote |
| "     | F + J          | <16 19>       | Double quote |
| &     | G + H          | <17 18>       | Ampersand |
| ~     | Z + -          | <25 34>       | Tilde |
| +     | X + .          | <26 33>       | Plus sign |
| `     | C + ,          | <27 32>       | Grave accent |
| \|    | V + M          | <28 31>       | Pipe |
| #     | B + N          | <29 30>       | Hash sign |

#### Notes
- **Visualization vs. Implementation:** The single/dual tables above exactly match your org-mode representation with `<pos,pos>` inline; the list here shows the same combos in a searchable form.
- **Swedish Locale:** Combos emit symbols using the Swedish layout (see `locale/keys_sv.h` for keycodes such as `SV_LBKT`, `SV_RBRC`, `SV_DQT`, `SV_PIPE`, etc.).
- **Reserved (nop):** The four mirrored bottom-row combos are intentionally shown as `"nop"` in the table to mark them as reserved; they’re *not* mapped in firmware.

## Notes
- **Key Positions**: Refer to the `default_map` in your keyboard's `.dtsi` file for exact layout.
- **Swedish Locale**: Uses macros like `SV_SQT`, `SV_DQT`, etc., from `locale/keys_sv.h`. Set OS to U.S. input for consistent symbols.
- **Ergonomics**: Horizontal adjacent fingers or thumb + finger; no same-finger verticals.
- **Testing**: Verify in a text editor with Swedish keyboard layout enabled.
- **Home-Row Mods**: Combos like `as` involve mods; 50ms timeout distinguishes from hold-taps—adjust if needed.
- **Changes from Old System**: New mappings are more symmetric and visualization-based; old ones (e.g., D+F for ()) are replaced for better flow.

For full configs, see the `.keymap` files. Contributions or issues welcome!
