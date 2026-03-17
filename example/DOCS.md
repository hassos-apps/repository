# Example Addon

This is an example addon for hassos-apps. It demonstrates the structure and automation of a Home Assistant addon.

## Configuration

| Option | Default | Description |
|---|---|---|
| `log_level` | `info` | Log verbosity: trace, debug, info, notice, warning, error, fatal |
| `seconds_between_quotes` | `5` | Interval (seconds) between log messages |

## How it works

The addon runs a loop that logs a message every N seconds. It uses:
- **Bashio** for config reading and logging
- **s6-overlay** for process supervision
- **hassio-addons/base** as the base image (Alpine Linux)
