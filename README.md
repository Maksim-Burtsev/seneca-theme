<p align="center"><img src="assets/hero.png" alt="merl in seneca-light and seneca" width="860"></p>

# seneca

Quiet themes for reading code: text in one grey, comments in a darker one, nothing else coloured.
Three of them:

- `seneca-light`: grey on paper.
- `seneca`: grey on #212121.
- `lucerna`: `seneca` with brighter keywords and definition names in bronze, for when you want a
  little structure back. There's no light version: bronze fades on paper.

<table>
<tr>
<td align="center"><img src="assets/shot-seneca-light.png" alt="seneca-light" width="420"><br><code>seneca-light</code></td>
<td align="center"><img src="assets/shot-seneca.png" alt="seneca" width="420"><br><code>seneca</code></td>
</tr>
<tr>
<td align="center" colspan="2"><img src="assets/shot-lucerna.png" alt="lucerna" width="420"><br><code>lucerna</code></td>
</tr>
</table>

## Files

| App | File |
|---|---|
| [merl](https://github.com/Maksim-Burtsev/merl), bat, Sublime Text, anything that reads TextMate themes | `tmtheme/*.tmTheme` |
| Ghostty, [agterm](https://github.com/umputun/agterm) | `ghostty/seneca`, `ghostty/seneca-light` |

A terminal has no syntax to colour, so `lucerna` in a terminal is just `seneca`.

## Install

**merl.** All three are built in: `merl --theme seneca-light`, or `theme = "seneca-light"` in
`~/.config/merl/config.toml`.

**bat.**

```sh
mkdir -p "$(bat --config-dir)/themes"
cp tmtheme/*.tmTheme "$(bat --config-dir)/themes/"
bat cache --build
bat --theme seneca-light file.py   # or BAT_THEME=seneca-light
```

**Sublime Text.** Copy a `.tmTheme` into `Packages/User/` and pick it under
*UI → Select Color Scheme*.

**Ghostty.** Copy the files into `~/.config/ghostty/themes/` and set `theme = seneca-light`, or
point at the file directly: `theme = /path/to/ghostty/seneca-light`. A pair that follows the
system appearance: `theme = light:seneca-light,dark:seneca`.

**agterm.** It reads Ghostty config. Keep agterm's own theme on the default
(`agtermctl theme set`), or it overrides yours, then set the theme in its Ghostty config as above.
agterm takes selection colours only from its bundled themes, so with a theme loaded by path the
selected sidebar row goes white on white. Repeat the selection colours next to the `theme` line:

```
selection-background = #d5d2c9
selection-foreground = #000000
```

For `seneca`, use `#444444` and `#ffffff`.

**Claude Code.** It draws in your terminal, so set the terminal to seneca first, then pick the
ANSI-only theme in `/theme` (light or dark): Claude Code then paints with seneca's muted ANSI
colours instead of its own. No file needed.

**Claude desktop.** Light, dark or system only; it has no custom themes yet.

## Palette

Everything you need to port the themes to a new app.

<img src="assets/palette-seneca-light.svg" alt="seneca-light palette">
<img src="assets/palette-seneca.svg" alt="seneca palette">
<img src="assets/palette-lucerna.svg" alt="lucerna palette">

The strip under each card is the terminal's red, green, yellow, blue, magenta and cyan.

### Editor

| Role | seneca-light | seneca | lucerna |
|---|---|---|---|
| Background | <img src="assets/swatch/f4f2ec.svg" width="14" height="14"> `#f4f2ec` | <img src="assets/swatch/212121.svg" width="14" height="14"> `#212121` | <img src="assets/swatch/212121.svg" width="14" height="14"> `#212121` |
| Text | <img src="assets/swatch/333333.svg" width="14" height="14"> `#333333` | <img src="assets/swatch/c0c0c0.svg" width="14" height="14"> `#c0c0c0` | <img src="assets/swatch/c0c0c0.svg" width="14" height="14"> `#c0c0c0` |
| Comment | <img src="assets/swatch/8e8c86.svg" width="14" height="14"> `#8e8c86` | <img src="assets/swatch/666666.svg" width="14" height="14"> `#666666` | <img src="assets/swatch/666666.svg" width="14" height="14"> `#666666` |
| Keyword | text | text | <img src="assets/swatch/ececec.svg" width="14" height="14"> `#ececec` |
| Function, class, type name | text | text | <img src="assets/swatch/c4a777.svg" width="14" height="14"> `#c4a777` |
| Operator | text | text | text |
| Cursor | <img src="assets/swatch/333333.svg" width="14" height="14"> `#333333` | <img src="assets/swatch/c0c0c0.svg" width="14" height="14"> `#c0c0c0` | <img src="assets/swatch/c0c0c0.svg" width="14" height="14"> `#c0c0c0` |
| Selection | <img src="assets/swatch/d5d2c9.svg" width="14" height="14"> `#d5d2c9` | <img src="assets/swatch/444444.svg" width="14" height="14"> `#444444` | <img src="assets/swatch/444444.svg" width="14" height="14"> `#444444` |
| Current line | <img src="assets/swatch/e9e6de.svg" width="14" height="14"> `#e9e6de` | <img src="assets/swatch/323232.svg" width="14" height="14"> `#323232` | <img src="assets/swatch/323232.svg" width="14" height="14"> `#323232` |
| Search match (background / text) | <img src="assets/swatch/c9c5ba.svg" width="14" height="14"> `#c9c5ba` / <img src="assets/swatch/000000.svg" width="14" height="14"> `#000000` | <img src="assets/swatch/5a5a5a.svg" width="14" height="14"> `#5a5a5a` / <img src="assets/swatch/ffffff.svg" width="14" height="14"> `#ffffff` | <img src="assets/swatch/5a5a5a.svg" width="14" height="14"> `#5a5a5a` / <img src="assets/swatch/ffffff.svg" width="14" height="14"> `#ffffff` |
| Line numbers | <img src="assets/swatch/b9b6ae.svg" width="14" height="14"> `#b9b6ae` | <img src="assets/swatch/444444.svg" width="14" height="14"> `#444444` | <img src="assets/swatch/444444.svg" width="14" height="14"> `#444444` |

Headings and bold are bold, italics are italic. Strings, numbers and everything else stay text.

### Terminal (ANSI)

| # | Colour | seneca-light | seneca |
|---|---|---|---|
| 0 | black | <img src="assets/swatch/333333.svg" width="14" height="14"> `#333333` | <img src="assets/swatch/323232.svg" width="14" height="14"> `#323232` |
| 1 | red | <img src="assets/swatch/a33a3a.svg" width="14" height="14"> `#a33a3a` | <img src="assets/swatch/c27070.svg" width="14" height="14"> `#c27070` |
| 2 | green | <img src="assets/swatch/4f7a3a.svg" width="14" height="14"> `#4f7a3a` | <img src="assets/swatch/8aab7a.svg" width="14" height="14"> `#8aab7a` |
| 3 | yellow | <img src="assets/swatch/8a6d1f.svg" width="14" height="14"> `#8a6d1f` | <img src="assets/swatch/c2a86a.svg" width="14" height="14"> `#c2a86a` |
| 4 | blue | <img src="assets/swatch/3d5f8a.svg" width="14" height="14"> `#3d5f8a` | <img src="assets/swatch/7a9ac2.svg" width="14" height="14"> `#7a9ac2` |
| 5 | magenta | <img src="assets/swatch/7a4f80.svg" width="14" height="14"> `#7a4f80` | <img src="assets/swatch/a888b8.svg" width="14" height="14"> `#a888b8` |
| 6 | cyan | <img src="assets/swatch/3a7a7a.svg" width="14" height="14"> `#3a7a7a` | <img src="assets/swatch/7ab0b0.svg" width="14" height="14"> `#7ab0b0` |
| 7 | white | <img src="assets/swatch/e9e6de.svg" width="14" height="14"> `#e9e6de` | <img src="assets/swatch/c0c0c0.svg" width="14" height="14"> `#c0c0c0` |
| 8 | bright black | <img src="assets/swatch/8e8c86.svg" width="14" height="14"> `#8e8c86` | <img src="assets/swatch/666666.svg" width="14" height="14"> `#666666` |
| 9 | bright red | <img src="assets/swatch/b84a4a.svg" width="14" height="14"> `#b84a4a` | <img src="assets/swatch/d08080.svg" width="14" height="14"> `#d08080` |
| 10 | bright green | <img src="assets/swatch/5e8a48.svg" width="14" height="14"> `#5e8a48` | <img src="assets/swatch/9abb8a.svg" width="14" height="14"> `#9abb8a` |
| 11 | bright yellow | <img src="assets/swatch/9a7b2a.svg" width="14" height="14"> `#9a7b2a` | <img src="assets/swatch/d0b87a.svg" width="14" height="14"> `#d0b87a` |
| 12 | bright blue | <img src="assets/swatch/4c6f9a.svg" width="14" height="14"> `#4c6f9a` | <img src="assets/swatch/8aaad0.svg" width="14" height="14"> `#8aaad0` |
| 13 | bright magenta | <img src="assets/swatch/8a5f90.svg" width="14" height="14"> `#8a5f90` | <img src="assets/swatch/b898c8.svg" width="14" height="14"> `#b898c8` |
| 14 | bright cyan | <img src="assets/swatch/4a8a8a.svg" width="14" height="14"> `#4a8a8a` | <img src="assets/swatch/8ac0c0.svg" width="14" height="14"> `#8ac0c0` |
| 15 | bright white | <img src="assets/swatch/ffffff.svg" width="14" height="14"> `#ffffff` | <img src="assets/swatch/ffffff.svg" width="14" height="14"> `#ffffff` |

The ANSI colours are muted on purpose, so git diffs, `ls` and errors still read apart without
shouting.

## Credits

The greys follow [huyvohcmc/atlas.vim](https://github.com/huyvohcmc/atlas.vim), a fork of
[jacoborus/tender.vim](https://github.com/jacoborus/tender.vim) (MIT). The themes started in
[merl](https://github.com/Maksim-Burtsev/merl).

MIT licence.
