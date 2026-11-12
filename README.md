# Seraph Aero Vantage

One workspace for drone system design, autonomy, code and simulation.

This is the official downloads repository for **Seraph Aero Vantage**, published by **BETHL LLC**. Application development is maintained separately.

## Download for Windows

Download the signed **0.51.46 Windows beta** from the [Vantage download page](https://www.seraphaero.com/download/) or [release assets](https://github.com/bethlco/SeraphVantage-Releases/releases/tag/v0.51.46). Matching source materials and checksums are included in the release.

This beta passed existing-PC upgrade, uninstall and reinstall, preserving 26 project files and 44 additional protected files. The packaged app and installed copy each passed two fresh-profile account-gate launches. Clean-machine installation testing remains incomplete.

Downloading Vantage is free. During beta, opening the workspace requires a BETHL account and an active **$1/month beta subscription**. Account creation, subscriptions and payments are handled on the [Seraph website](https://www.seraphaero.com/).

## Mission and Code verification

The signed **0.51.46** installer includes the following mission and Code workflows.

| Workflow | Verified behavior and limits |
| --- | --- |
| Saved waypoints → Code → onboard mission | Flight-only routes compile to native missions for ArduPilot 4.7.1 and PX4 1.16.0 quadcopters. Python itself does not run on the controller. |
| Review and upload | Review takeoff-relative heights, controller-managed timing and end behavior. Upload saves a recovery copy and verifies the controller's mission contents. It does not arm or start the aircraft. |
| Actual firmware simulation | Both firmwares passed waypoint routes with return/landing, wait → return home → land, and hold until the simulated pilot lands. Both also passed interrupted-upload recovery and mission restoration. |
| Companion Python | Reviewed file transfer preserves folders and generated integration helpers. Optional Upload & run executes the selected Python entry file with a five-minute limit. Python 3, the standard timeout utility and implemented integrations are required. |
| Complex or unsupported mission logic | Branches, loops, dynamic inputs and unsupported flight actions are rejected by native compilation. Companion execution still needs working integration drivers; there is no universal flight/sensor adapter. |
| Physical aircraft | Not validated by these checks. No physical installation or flight support is claimed. |

Release checks on November 12, 2026 passed **1,480 automated tests**, desktop upload/recovery checks in light and dark modes, a production build, and **six actual-firmware simulation scenarios** across the two firmware versions. Companion tests used real SSH/SFTP and local Python with a controlled execution endpoint, not a physical Raspberry Pi. Earlier requirements dropdown checks passed layout, collapse and selection at three window sizes.

## Verify a download

Published installers are signed by **BETHL LLC**. In Windows, open the installer's Properties → Digital Signatures to inspect its signature. Each release includes `SHA256SUMS.txt` to check that the downloaded files match the published files.

## Source materials and notices

Each published release includes matching third-party source materials, license notices and build information. Those materials retain their respective licenses; this repository does not grant a license to Vantage's proprietary application source.

## Contact

[team@seraphaero.com](mailto:team@seraphaero.com) · [seraphaero.com](https://www.seraphaero.com/)
