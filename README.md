# tool_i3_volume

Volume up/down/mute helpers for PulseAudio/PipeWire desktops, with optional i3status refresh.

## Commands

- `vup` - increase default sink volume
- `vdown` - decrease default sink volume
- `vtoggle` - toggle mute
- `volume` - interactive terminal volume controller

## Dependencies

Required shell:
- Bash

Required commands:
- `pactl`
- `pamixer`

Optional commands:
- `i3status` - refreshed when available/configured

The executable scripts call `need` for required commands before using them.

## Install

```bash
./install.sh
```

Install to a custom prefix:

```bash
PREFIX="$HOME/.local" ./install.sh
```

## Usage

```bash
vup
vdown
vtoggle
volume
```

## Configuration

- Set `I3STATUS_ADDITIONAL_CMD` to a command that refreshes extra i3status text. If unset, `i3status-additional` is used when available.

## Notes

These scripts were extracted from a personal Arch Linux + i3 workspace. Review dependencies and paths before using them on another machine.
