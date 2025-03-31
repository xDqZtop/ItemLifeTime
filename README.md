# <img src="https://github.com/DavyCraft648/ItemLifeTime/blob/main/icon.png" width="64" height="64" alt="ItemLifeTime Icon"/> ItemLifeTime

[![PMMP Version](https://img.shields.io/badge/PMMP-5.x-blue)](https://pmmp.io)
[![License](https://img.shields.io/github/license/DavyCraft648/ItemLifeTime)](LICENSE)

Customize dropped item despawn times across your PocketMine-MP server with granular world-specific control.

## Features

- ⏱️ Set global default item despawn time
- 🌍 Configure world-specific despawn durations
- 🔍 Optional visual countdown display
- ⚡ Lightweight and efficient
- 🔄 Automatic configuration management

## Installation

1. Download the latest phar from [Releases](https://github.com/xDqZtop/ItemLifeTime/releases)
2. Place the phar in your server's `plugins/` folder
3. Restart your server
4. Configure to your needs (see below)

## Configuration

After first run, edit `plugins/ItemLifeTime/config.yml`:

```yaml
# Global default despawn time (seconds)
# - Range: 0-1938 (≈32 minutes)
# - -1 = Never despawn
item-lifetime: 300

# World-specific overrides
worlds:
  lobby: -1      # Items never despawn in lobby
  pvp_arena: 60  # Quick 1-minute despawn in PvP
  mining: 600    # 10 minutes in mining world

# Visual countdown display
display-time:
  enabled: true  # Show remaining time
  text: "{TIME} remaining"  # Display format