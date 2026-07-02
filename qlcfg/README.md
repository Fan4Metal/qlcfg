# Quake Live config

Syntax highlighting for [Quake Live](https://store.steampowered.com/app/282440/Quake_Live/) configuration files (`.cfg`).

## Features

- Highlighting for `.cfg` files, including:
  - **Console commands** (`bind`, `set`, `exec`, `map`, `kick`, `qlx`, `pyrestart`, …)
  - **Server, client, game and engine cvars** (`sv_hostname`, `g_gametype`, `cg_fov`, `r_picmip`, …)
  - **minqlx plugin cvars** (`qlx_*`, e.g. `qlx_commandPrefix`, `qlx_balanceAuto`, `qlx_redisAddress`)
  - **Key names** for `bind`/`unbind` (`SPACE`, `MOUSE1`, `F1`–`F12`, `KP_ENTER`, …)
  - **Numeric constants** and **quoted strings**
- Line comments (`//`) and block comments (`/* */`)
- Automatic closing of quotes

## Usage

Open any file with the `.cfg` extension and the highlighting is applied automatically. If VS Code does not detect the language, select **Quake Live config** from the language mode picker in the bottom-right status bar.
