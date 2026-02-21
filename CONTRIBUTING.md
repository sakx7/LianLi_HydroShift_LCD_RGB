# Contributing

Thanks for helping improve the HydroShift SignalRGB plugin.

## Scope
This repository targets LED control for Lian Li HydroShift LCD AIO devices.

Out of scope for now:
- LCD content control
- Pump control
- Fan RPM/speed control

## Development principles
- Keep behavior deterministic across `Forced`, `Canvas`, `Paint/Depaint`, and `Shutdown`.
- Avoid re-init bursts inside render loops.
- Prefer protocol evidence over assumptions.

## Local test checklist
Before opening a PR:
1. Restart SignalRGB.
2. Test all modes: `Forced`, `Canvas`, `Paint`, `Depaint`, `Shutdown`.
3. Verify no flicker/scintillation regressions.
4. If L-Connect is running, ensure LED sync is not writing concurrently.

## Pull request rules
1. Keep PRs focused (single objective).
2. Describe exact hardware used (variant, fan config, VID/PID).
3. Include reproducible test steps and results.
4. Update `README.md` if compatibility behavior changes.

## Repository hygiene
- Do not commit backups or runtime files (`*.bak`, `*.tmp`, `*.temp`, `*.log`).
- Keep only one active plugin file: `LianLi_HydroShift_LCD_RGB.js`.

## Reporting compatibility
If you test another HydroShift variant (`360S`, `360TL`, `360N`, etc.), open a
"Variant compatibility report" issue and include factual results.
