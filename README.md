# ChoomCity

![ChoomCity transmission banner with a neon Night City skyline](assets/choomcity-banner.svg)

**Your V. Your crew. One Night City.** Choom-op brings experimental PC co-op to Cyberpunk 2077. Meet up in the host’s world, take a passenger seat, and explore together using your own V and save.

**[Get v0.5.1 for Windows](https://github.com/Mackaboi/ChoomCity-Releases/releases/tag/v0.5.1)** · [All builds](https://github.com/Mackaboi/ChoomCity-Releases/releases) · [Report a bug](https://github.com/Mackaboi/ChoomCity-Releases/issues)

> [!WARNING]
> **Very experimental · Early development.** The v0.5.1 release passed automated checks, including a two-player simulation. The project is still awaiting its first live test inside Cyberpunk 2077. Expect bugs and broken sessions.

## Inside ChoomCity

- **Meet in the CHOOMCITY hub.** Host or join from the main or pause menu using Steam invites, a join code, or an IP address. Set a lobby password and ready up before you head out.
- **Show up as your own V.** Friends see your outfit and weapon, along with actions like sprinting, crouching, aiming, and reloading. Face sync is experimental.
- **Ride shotgun.** Share a car, keep your seat, and try shooting from the passenger side. Vehicle sync is designed to keep one copy of each car.
- **Explore the host’s streets.** Nearby guests see mirrored traffic, pedestrians, and enemies. Fight the same enemies while time and weather follow the host.
- **Keep your own progress.** Each player loads their own save. Co-op saves are organized by host, with synchronized autosaves and dialogue voting for groups playing at the same story point.

## Get into Night City

1. Download **`ChoomLauncher.exe`** from the release page and run it. The launcher looks for your game automatically.
2. In the launcher, open **Mods** and select **Download everything** to install Choom-op and its dependencies. The launcher can update both itself and the mod.
3. Start Cyberpunk 2077, open **CHOOMCITY**, and host or join a session.

**Manual install** · Install RED4ext, Cyber Engine Tweaks, and redscript, then extract `CoopMod-*.zip` into your Cyberpunk 2077 folder. Native Settings UI is optional.

## Known limits and first tests

- **Connections are direct.** Steam invites still need a reachable host. If automatic port mapping fails, the host can forward UDP port 7777 or use Tailscale.
- **The shared world is local to the host.** NPC mirroring covers the area near the host (150 m by default). Mirrored NPCs can behave differently on each screen.
- **Story progress depends on where you start.** Play from the same story point. The optional journal test copies quest objectives, while each game still runs its own quest scripts.
- **Back up saves before testing.** Manually overwriting a solo save during co-op can still replace it.

The first live tests should cover opening **CHOOMCITY**, joining from the main menu, loading the right save, face and outfit sync, passenger combat, shared NPC damage, and dialogue votes. If **Continue my game** stalls, try the game’s own **Continue**. If faces look wrong, disable **Show friends’ faces**.

## Field diagnostics

![Telemetry panel showing the F10 overlay shortcut, connection stats, frame timing, and session logs](assets/choomcity-telemetry.svg)

**Press F10** during a session to see ping, packet loss, bandwidth, position update freshness, and how much frame time the mod uses. v0.5.1 also adds retries for one-time messages such as votes, saves, and car handovers.

When something breaks, open **CHOOMCITY → Help → Copy problem report** and paste it into a [GitHub issue](https://github.com/Mackaboi/ChoomCity-Releases/issues). Include what the host and guest were doing. For lag or desync, attach `coop_stats.log` if available.
