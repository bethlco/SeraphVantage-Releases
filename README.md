# Seraph Aero Vantage

One workspace for drone system design, autonomy, code and simulation.

This is the official downloads repository for **Seraph Aero Vantage**, published by **BETHL LLC**. Application development is maintained separately.

## Download for Windows

Download the signed **0.51.45 Windows beta** from the [Vantage download page](https://www.seraphaero.com/download/) or [release assets](https://github.com/bethlco/SeraphVantage-Releases/releases/tag/v0.51.45). Matching source materials and checksums are included in the release.

This beta passed existing-PC uninstall/reinstall and account-access checks. Clean-machine installation testing remains incomplete.

Downloading Vantage is free. During beta, opening the workspace requires a BETHL account and an active **$1/month beta subscription**. Account creation, subscriptions and payments are handled on the [Seraph website](https://www.seraphaero.com/).

## Mission waypoint capabilities

Mission waypoints can be brought into Autonomy and generated as Python in Code. This is a **computer-side mission runner**, not an onboard ArduPilot or PX4 flight program.

| Workflow | Current status |
| --- | --- |
| Saved waypoints → generated code | Verified: waypoint order, coordinates, ground-relative altitude and speed are preserved. |
| Offline mission logic | Verified: supplied scenario events complete, stop on missing results or follow failure outcomes. This does not simulate flight physics. |
| Upload this Python mission to a flight controller | Unavailable. Controller uploads reject this file; Launch and Navigate have no bundled flight adapter. |
| Fly the route on actual firmware or hardware | Not verified or supported by this generated mission path. |

Development checks on November 11, 2026 passed 29 route, mission and delivery tests plus desktop checks. The requirements dropdown fix passed light/dark layout, collapse and selection checks at three window sizes. These source changes are awaiting a future installer release; the **0.51.45 download is unchanged**.

## Verify a download

Published installers are signed by **BETHL LLC**. In Windows, open the installer's Properties → Digital Signatures to inspect its signature. Each release includes `SHA256SUMS.txt` to check that the downloaded files match the published files.

## Source materials and notices

Each published release includes matching third-party source materials, license notices and build information. Those materials retain their respective licenses; this repository does not grant a license to Vantage's proprietary application source.

## Contact

[team@seraphaero.com](mailto:team@seraphaero.com) · [seraphaero.com](https://www.seraphaero.com/)
