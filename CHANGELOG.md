# Changelog

All notable changes to this project. Format: [Keep a Changelog](https://keepachangelog.com/en/1.1.0/); versions follow [SemVer](https://semver.org/).

Each release's section becomes the notes of its GitHub Release (`tools/release_notes.sh`). On a `release/vX.Y.Z` branch, rename **Unreleased** to `[X.Y.Z] - YYYY-MM-DD` and set the same version in `project.godot` (`application/config/version`).

## [Unreleased]

### Added
- **The starter, extracted from [paulshannon/game](https://github.com/paulshannon/game)** at `17d86a8` (its v0.1.1 plus later develop work): everything except the space game and its Kenney packs. For the history of each piece, see that repo's CHANGELOG.
  - Networking: `Net` (WebSocket transport), `Protocol`, `LaunchConfig` (command line and page URL), `InputRelay` (sender checks, stale and timed-out input), `Replication`, `BotInput`.
  - Game plumbing: `GameBase` (spawner, join choice, back to select, smoke reports), `PlayerNet`, `PlayerSlots`, `ServerBots` (bots the server flies itself).
  - Client: `SnapshotBuffer` / `SnapshotClock` interpolation on the server timeline, `StateTimeline`, input actions with keyboard and controller defaults, remapping (`InputBindings`, `ControlsEditor`), touch stick and action button, `Hud`, `GameMenu`.
  - Two skeleton games to copy: `box_arena_2d` (the default) and `box_arena_3d`.
  - Tests (`TestCase` runner with error capture), every `tools/` command, `deploy/` (Caddy, systemd, Docker) and CI / release workflows.
