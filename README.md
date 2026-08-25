# tool_i3_volume

Volume up/down/mute helpers for PulseAudio/PipeWire desktops, with optional i3status refresh.

## Commands

- `vup` - increase default sink volume
- `vdown` - decrease default sink volume
- `vtoggle` - toggle mute
- `volume` - interactive terminal volume controller

## Dependencies

Required commands:
- `bash`
- `pactl`
- `pamixer`

Optional commands:
- `i3status` - refreshed when available/configured

Check required commands in your shell:

```bash
need() {
    command -v "$1" >/dev/null || echo "missing: $1"
}

for cmd in bash pactl pamixer; do
    need "$cmd"
done
```

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
