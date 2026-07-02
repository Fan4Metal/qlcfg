# Quake Live config

A Visual Studio Code extension that provides syntax highlighting for [Quake Live](https://store.steampowered.com/app/282440/Quake_Live/) configuration files (`.cfg`).

## Features

- Syntax highlighting for `.cfg` files, including:
  - **Console commands** (`bind`, `set`, `exec`, `map`, `kick`, `qlx`, `pyrestart`, …)
  - **Server, client, game and engine cvars** (`sv_hostname`, `g_gametype`, `cg_fov`, `r_picmip`, …)
  - **minqlx plugin cvars** (`qlx_*`, e.g. `qlx_commandPrefix`, `qlx_balanceAuto`, `qlx_redisAddress`)
  - **Key names** for `bind`/`unbind` (`SPACE`, `MOUSE1`, `F1`–`F12`, `KP_ENTER`, …)
  - **Numeric constants** and **quoted strings**
- Line comments (`//`) and block comments (`/* */`)
- Automatic closing of quotes

## Installation

The extension sources live in the [`qlcfg/`](qlcfg/) folder.

1. Package the extension with [`vsce`](https://github.com/microsoft/vscode-vsce) from that folder:
   ```sh
   npm install -g @vscode/vsce
   cd qlcfg
   vsce package
   ```
2. In VS Code, open the Extensions view, choose **Install from VSIX…**, and select the generated `.vsix` file.

### Manual

Copy the [`qlcfg/`](qlcfg/) folder into your VS Code extensions directory (`~/.vscode/extensions` on Linux/macOS, `%USERPROFILE%\.vscode\extensions` on Windows) and reload the editor.

## Usage

Open any file with the `.cfg` extension and the highlighting is applied automatically. If VS Code does not detect the language, select **Quake Live config** from the language mode picker in the bottom-right status bar.

## Project structure

| Path | Description |
| --- | --- |
| `qlcfg/package.json` | Extension manifest (language and grammar contributions) |
| `qlcfg/syntaxes/qlcfg.plist` | TextMate grammar with the highlighting rules |
| `qlcfg/language-configuration.json` | Comments and auto-closing pairs |
| `qlcfg/images/logo.png` | Extension icon |

## Grammar

The grammar (`qlcfg/syntaxes/qlcfg.plist`) was generated with [Iro](https://eeyo.io/iro/). The command and cvar lists are kept in sync with an authoritative dump of Quake Live / minqlx cvars, so newly discovered variables can be appended to the corresponding alternation in the grammar.

## License

No license has been specified for this project yet.
