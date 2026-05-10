# RTK Forecast

Android app for professional GNSS/RTK field planning.

RTK Forecast helps surveyors decide whether conditions at a given location
are suitable for GNSS/RTK work before leaving for the field. It pulls live
satellite geometry, space-weather data from NOAA SWPC, and local weather
from Open-Meteo into a single screen, with a 48-hour planning timeline and
PDF export.

Live portfolio: https://rtk-forecast.vercel.app

Source code is private. This repository is a public project case study.

---

## What it does

- Computes PDOP, HDOP, and VDOP using a proper N x (3+K) H matrix with
  per-constellation clock-bias columns (GPS, GLONASS, Galileo, BeiDou).
  This matches the formulation used by professional receivers, not the
  simplified single-clock GPS-era approximation.
- Shows a live polar sky view of all visible satellites, updated every
  30 seconds, with a 10 degree elevation mask.
- Displays the official NOAA SWPC 3-hour Kp index, a live 1-minute
  estimate, and a 48-hour Kp forecast.
- Accepts location input via Google Maps picker or typed coordinates
  in decimal degrees, degrees-decimal minutes, or degrees-minutes-seconds.
- Generates a 5-slot timeline comparison (Now, +1h, +2h, +3h, Tomorrow
  09:00) and exports it as a PDF.

## Validation

DOP calculations were validated against Trimble GNSS Planning Online.
Results at a test location: PDOP 0.84, HDOP 0.42, VDOP 0.73 vs
Trimble's 0.83 / 0.44 / 0.70.

Predicted satellite count was compared in the field against a
Stonex S850+ RTK receiver. The app consistently showed more satellites
than the receiver tracked, which is expected: the app predicts
geometrically visible satellites with no obstructions, while the receiver
applies signal quality thresholds and real-world site conditions.

## Project status

Functional Android app. Play Store closed testing in progress.

## Stack

React Native, Expo SDK 54, TypeScript, satellite.js v6, NOAA SWPC API,
CelesTrak TLE data, Open-Meteo, Google Maps SDK, EAS Build, Hermes.

## How it was built

The app was architected by George Kouikoglou, a freelance surveying
engineer based in Kavala, Greece. The source code was written with
AI coding tools (Claude Code, Codex) under his direction. All technical
decisions, data source choices, validation work, and field testing were
done by him.

## Screenshots

<img width="1080" height="2374" alt="Screenshot_2026-05-09-11-36-44-93_b29aabb9387aa77602b391a7c331c2dc" src="https://github.com/user-attachments/assets/0c89efa6-cd9d-4a4c-bfff-8aba8c0e331b" />
<img width="1080" height="2374" alt="Screenshot_2026-05-09-11-37-44-19_b29aabb9387aa77602b391a7c331c2dc" src="https://github.com/user-attachments/assets/525925d1-c80f-481c-adae-d5e0707fb2dc" />
<img width="1080" height="2374" alt="Screenshot_2026-05-09-11-38-38-18_e2d5b3f32b79de1d45acd1fad96fbb0f" src="https://github.com/user-attachments/assets/618ecd0a-5f6e-4564-861f-854d7ec77177" />
<img width="1080" height="2374" alt="Screenshot_2026-05-09-11-37-11-32_b29aabb9387aa77602b391a7c331c2dc" src="https://github.com/user-attachments/assets/780a1bf8-90b9-4a3d-8d2d-f865be614c56" />
<img width="1080" height="2374" alt="Screenshot_2026-05-09-11-37-05-76_b29aabb9387aa77602b391a7c331c2dc" src="https://github.com/user-attachments/assets/2c69cfad-ae78-409d-88f2-2cfec61725e0" />


## Notes

This repository does not include source code. It exists to document the
project publicly for portfolio and contest submission purposes.
