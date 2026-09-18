# Universo

A dark, cinematic theme inspired by SpaceX, xAI, and GrokNight.
Void black canvas, neutral gray ramp, TokyoNight accents — engineered
restraint with color reserved for content semantics.
Designed for omarchy.org with a focus on clarity, depth, and minimal distraction.

Theme created with aether https://github.com/bjarneo/aether <br>
Palette strongly inspired by GrokNight (grok-build `xai-grok-pager-render`).

# Installation

Local (this machine):

```bash
omarchy theme set universo
```

From a git repo (after publishing):

```bash
omarchy theme install https://github.com/jltrench/omarchy-universo-theme.git
```

> Note: a theme installed from a repo cannot ship Lua, terminal configs, or
> `vscode.json` (Omarchy drops them and generates from `colors.toml`
> instead). The hand-tuned `zed.json` and `vscode-extension/` in this repo
> apply to local installs; on repo installs, editors fall back to the
> generated `Omarchy` theme until imported manually (see below).

# Screenshots

![Universo preview](preview.png)
![Universo boot preview](preview-unlock.png)

Backgrounds live in `backgrounds/` (`universo-1..6`), each with a black
gradient baked into the top so the transparent bar keeps labels readable.

# What is themed

- Terminals (ghostty, alacritty, kitty, foot), tmux, btop — generated from `colors.toml`
- Neovim (aether), Helix, Obsidian — generated from `colors.toml`
- Shell/bar, Hyprland, Mako, Walker, Chromium — generated from `colors.toml`
- Lock screen — follows the current background automatically (Quickshell)
- Boot splash (Plymouth) — `unlock.png` + `colors.toml` via:
  `omarchy plymouth set-by-theme universo` (needs sudo)
- Cursor / VS Code — packaged `local.theme-universo` extension (`vscode.json` + `vscode-extension/`)
- Zed — `zed.json`, copy once to `~/.config/zed/themes/universo.json`
- Icons — `Yaru-blue`

Login screen (SDDM) stays the Omarchy default by design — same for every
theme. Boot and lock are the theme-driven surfaces.

# Editor setup (manual steps)

Zed does not auto-apply `zed.json` on `theme set`:

```bash
mkdir -p ~/.config/zed/themes
cp ~/.config/omarchy/themes/universo/zed.json ~/.config/zed/themes/universo.json
```

VS Code family uses the packaged `Universo` theme (`local.theme-universo`).
Install the local extension once, then:

```bash
omarchy-theme-set-vscode
```

# Palette (v2, GrokNight-inspired)

| Role | Hex | Source |
| ---- | --- | ------ |
| Terminal canvas | `#0a0a0a` | GrokNight `BG` |
| Darkest | `#0c0c0c` | GrokNight `BG_DARK` |
| Void | `#000000` | SpaceX canvas |
| Elevated | `#242424` | GrokNight `BG_HIGHLIGHT` |
| Editor canvas | `#0e0e0e` | `grok-night.tmTheme` |
| Primary text | `#e1e1e1` | GrokNight `FG` |
| Secondary text | `#c8c8c8` | GrokNight `FG_DARK` |
| Muted | `#6c6c6c` | GrokNight `COMMENT` |
| Selection | `#363636` | GrokNight `bg_visual` |
| Borders | `#323237` / `#3c3c41` / `#505058` | GrokNight chrome |
| Blue / functions | `#7aa2f7` | TokyoNight |
| Cyan / links | `#7dcfff` | GrokNight `CYAN` |
| Green / strings | `#9ece6a` | TokyoNight |
| Mint / keys | `#73daca` | GrokNight `GREEN1` |
| Magenta / keywords | `#bb9af7` | TokyoNight |
| Orange / numbers | `#ff9e64` | TokyoNight |
| Yellow / types | `#e0af68` | TokyoNight |
| Golden highlight | `#ffdb8d` | GrokNight `accent_plan` |
| Teal / headings | `#1abc9c` | GrokNight `TEAL` |
| Comment (code) | `#51597d` italic | `grok-night.tmTheme` |
| Operator | `#89ddff` | `grok-night.tmTheme` |
| Abort red | `#f7768e` | TokyoNight |

#### Recommendations for 3rd-Party App Theming

Using Bypass Theme-Hook script for GTK, Vesktop, Steam, Spotify etc:
https://github.com/imbypass/omarchy-theme-hook

### License

MIT — see [LICENSE](LICENSE).
