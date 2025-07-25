My zmk config for my keyboards from keebart.com


![](my_keymap.png)


https://keymap-drawer.streamlit.app


# Piantor Pro BT Combo Reference

This is a reference list of all key combinations (combos) defined for the Piantor Pro BT keyboard using ZMK firmware with the QWERTY base layer and Swedish locale (`locale/keys_sv.h`). Each combo is triggered by pressing two keys simultaneously on the base layer (`layer 0`) with a 50ms timeout. These combos are designed for ergonomic use (horizontal adjacent fingers or thumb + finger, no same-finger verticals) and output symbols relevant for Java, Python, and Bash development.

| Symbol | Keys to Press | Key Positions | Description |
|--------|---------------|---------------|-------------|
| `(`    | `D + F`       | `<15 16>`     | Left parenthesis |
| `)`    | `J + K`       | `<19 20>`     | Right parenthesis |
| `{`    | `A + S`       | `<13 14>`     | Left curly brace |
| `}`    | `L + Ö`       | `<21 22>`     | Right curly brace |
| `[`    | `S + D`       | `<14 15>`     | Left square bracket |
| `]`    | `K + L`       | `<20 21>`     | Right square bracket |
| `<`    | `Z + X`       | `<25 26>`     | Less-than sign |
| `>`    | `. + -`       | `<33 34>`     | Greater-than sign |
| `/`    | `W + E`       | `<2 3>`       | Forward slash |
| `\`    | `I + O`       | `<8 9>`       | Backslash |
| `'`    | `Q + W`       | `<1 2>`       | Single quote |
| `"`    | `U + I`       | `<7 8>`       | Double quote |
| ```    | `T + Y`       | `<5 6>`       | Grave accent |
| `~`    | `O + P`       | `<9 10>`      | Tilde |
| `\|`   | `X + C`       | `<26 27>`     | Pipe |
| `&`    | `, + .`       | `<32 33>`     | Ampersand |
| `+`    | `W + P`       | `<2 10>`      | Plus sign |
| `*`    | `E + O`       | `<3 9>`       | Asterisk |
| `%`    | `R + I`       | `<4 8>`       | Percent sign |
| `^`    | `R + U`       | `<4 7>`       | Caret |
| `=`    | `Q + P`       | `<1 10>`      | Equals sign |
| `!`    | `S + K`       | `<14 20>`     | Exclamation mark |
| `?`    | `D + J`       | `<15 19>`     | Question mark |
| `#`    | `Z + .`       | `<25 33>`     | Hash sign |
| `$`    | `X + .`       | `<26 33>`     | Dollar sign |
| `@`    | `C + ,`       | `<27 32>`     | At sign |



## Notes
- **Key Positions**: Refer to the `default_map` in `piantor_pro_bt-layouts.dtsi` for the physical key layout.
- **Swedish Locale**: Uses macros like `SV_SQT`, `SV_DQT`, `SV_EXCL`, etc., from `locale/keys_sv.h` to ensure correct symbol output on a Swedish keyboard layout.
- **Ergonomics**: Combos are designed for horizontal adjacent fingers (e.g., `J + K`) or thumb + finger (e.g., `V + SPC`) to avoid same-finger vertical presses.
- **Testing**: Use a text editor or keyboard tester to verify outputs. Ensure your system is set to a Swedish keyboard layout for correct symbol rendering.
- **Home-Row Mods**: Combos like `S + D` and `A + S` involve home-row mod keys. The 50ms timeout helps distinguish them from hold-tap behaviors, but adjust `timeout-ms` if needed.

## QWERTY Base Layer with Combos

# Corne Pro BT Combo Reference

| Symbol | Keys to Press | Key Positions | Description |
|--------|---------------|---------------|-------------|
| `(`    | `D + F`       | `<17 18>`     | Left parenthesis |
| `)`    | `J + K`       | `<23 24>`     | Right parenthesis |
| `{`    | `A + S`       | `<15 16>`     | Left curly brace |
| `}`    | `L + Ö`       | `<25 26>`     | Right curly brace |
| `[`    | `S + D`       | `<16 17>`     | Left square bracket |
| `]`    | `K + L`       | `<24 25>`     | Right square bracket |
| `<`    | `Z + X`       | `<29 30>`     | Less-than sign |
| `>`    | `. + -`       | `<37 38>`     | Greater-than sign |
| `/`    | `W + E`       | `<2 3>`       | Forward slash |
| `\`    | `I + O`       | `<10 11>`     | Backslash |
| `'`    | `Q + W`       | `<1 2>`       | Single quote |
| `"`    | `U + I`       | `<9 10>`      | Double quote |
| ```    | `Q + W`       | `<1 2>`       | Grave accent |
| `~`    | `U + I`       | `<9 10>`      | Tilde |
| `\|`   | `X + C`       | `<30 31>`     | Pipe |
| `&`    | `, + .`       | `<36 37>`     | Ampersand |
| `+`    | `W + P`       | `<2 12>`      | Plus sign |
| `*`    | `E + O`       | `<3 11>`      | Asterisk |
| `%`    | `R + I`       | `<4 10>`      | Percent sign |
| `^`    | `R + I`       | `<4 10>`      | Caret |
| `=`    | `Q + P`       | `<1 12>`      | Equals sign |
| `!`    | `S + K`       | `<16 24>`     | Exclamation mark |
| `?`    | `D + J`       | `<17 23>`     | Question mark |
| `#`    | `Z + /`       | `<29 38>`     | Hash sign |
| `$`    | `X + .`       | `<30 37>`     | Dollar sign |
| `@`    | `C + ,`       | `<31 36>`     | At sign |