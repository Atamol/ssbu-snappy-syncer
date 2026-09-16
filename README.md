### ![ja](https://flagcdn.com/20x15/jp.png) [日本語版はこちら](README.ja.md)

# ssbu-snappy-syncer

Cuts 4F of input delay from Super Smash Bros. Ultimate. Serves the same purpose as other low-latency mods like [ssbu-online-deluxe](https://github.com/saad-script/ssbu-online-deluxe), but holds up reliably under load and makes the mod usage subtle enough that opponents or third parties won't notice.

Compatible with [ssbu-combat-latency-slider](https://github.com/Atamol/ssbu-combat-latency-slider), but INCOMPATIBLE with [ssbu-vsync-disabler](https://github.com/Atamol/ssbu-vsync-disabler). Do not use this mod and [ssbu-vsync-disabler](https://github.com/Atamol/ssbu-vsync-disabler) at the same time.

> v13.0.5 only. Use at your own risk, Idk though.

## Features

* Simple

No plugin dependencies.

* Overclock

Stock clocks held the 4 frame reduction up to 13.0.4 and no longer do on 13.0.5, so the cpu clock is raised.

Also, it runs at 720p instead of 1080p (FHD) by default. You can switch to 1080p in the config, but lag might occur in some scenes. If that is a concern, try using [ssbu-combat-latency-slider](https://github.com/Atamol/ssbu-combat-latency-slider) + [ssbu-vsync-disabler](https://github.com/Atamol/ssbu-vsync-disabler) instead.

* Heavy HS, heavy KO cutscenes and the foreground KO bug

None of the lags on heavy hitstop, heavy KO cutscenes or a foreground KO.

## Install

1. Copy the `atmosphere` folder from [Release](https://github.com/Atamol/ssbu-snappy-syncer/releases) to the root of your SD card
2. Reboot the console (Album → Reboot to Payload)

## Config

Written to `sd:/ultimate/ssbu-snappy-syncer/config.txt` on first launch.

**Leave it on the defaults unless you have a reason not to**.

| Key                      | Default            |                                                                                      |
| ------------------------ | ------------------ | ------------------------------------------------------------------------------------ |
| `index_mode`           | `0`              | 0: lowest latency, 1: +1F, 2: vanilla                                                |
| `render_opts`          | `true`           | records fighter render commands after the scene update                               |
| `double_buffer`        | `true`           | `false`: triple buffering                                                          |
| `resolution`           | `720p`           | 1080p gets heavy, 576p clips the cut-ins and the countdown                           |
| `vsync`                | `false`          |                                                                                      |
| `pacer`                | `true`           |                                                                                      |
| `cutin_render_opts`    | `true`           | drops render opts for the length of the KO                                           |
| `match_only_immediate` | `true`           |                                                                                      |
| `overclock`            | `true`           |                                                                                      |
| `overclock_by_match`   | `true`           |                                                                                      |
| `overclock_profile`    | auto               | `singles`: 1428, `ffa`: 1683, auto: by player count (3 or more raises the clock) |
| `overclock_custom`     | `1785,1267,1996` | `cpu,gpu,mem` in MHz, docked only                                                  |
| `legacy_sync`          | `false`          |                                                                                      |
