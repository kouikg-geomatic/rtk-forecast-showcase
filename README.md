# RTK Forecast

**GNSS field-planning app for surveyors**

RTK Forecast helps surveyors decide whether current and upcoming field conditions are suitable for GNSS/RTK work. The app combines satellite geometry, space-weather risk, and local field conditions into a mobile-first dashboard.

> Source code is private. This repository is a public project case study with screenshots, feature notes, and architecture overview.

## Live demo

https://rtk-forecast.vercel.app/

## Project status

- Android app in development
- Built with React Native / Expo and TypeScript
- Public landing page available
- Planned Google Play release

## Core features

- Multi-constellation GNSS planning: GPS, GLONASS, Galileo, BeiDou
- Visible satellite sky view with a 10° elevation mask
- PDOP / HDOP / VDOP indicators for survey planning
- NOAA SWPC space-weather data, including official 3-hour Kp and alerts
- 48-hour planning timeline for comparing field windows
- Local weather conditions using Open-Meteo
- Location override by map or coordinates
- PDF export concept for field notes or client documentation

## Technical stack

- React Native / Expo SDK 54
- TypeScript
- satellite.js for orbital propagation
- CelesTrak TLE data
- NOAA SWPC API
- Open-Meteo API
- Google Maps SDK
- Hermes JavaScript engine
- EAS Build

## Why this project exists

Many surveyors check GNSS conditions only after arriving on site, or rely on older desktop planning tools. RTK Forecast is designed as a practical mobile tool for the decision made before leaving for the field: whether today is a good time to survey, and which time window is likely to be better.

## Screenshots

<img width="1080" height="2374" alt="Screenshot_2026-05-09-11-36-44-93_b29aabb9387aa77602b391a7c331c2dc" src="https://github.com/user-attachments/assets/0c89efa6-cd9d-4a4c-bfff-8aba8c0e331b" />
<img width="1080" height="2374" alt="Screenshot_2026-05-09-11-37-44-19_b29aabb9387aa77602b391a7c331c2dc" src="https://github.com/user-attachments/assets/525925d1-c80f-481c-adae-d5e0707fb2dc" />
<img width="1080" height="2374" alt="Screenshot_2026-05-09-11-38-38-18_e2d5b3f32b79de1d45acd1fad96fbb0f" src="https://github.com/user-attachments/assets/618ecd0a-5f6e-4564-861f-854d7ec77177" />
<img width="1080" height="2374" alt="Screenshot_2026-05-09-11-37-11-32_b29aabb9387aa77602b391a7c331c2dc" src="https://github.com/user-attachments/assets/780a1bf8-90b9-4a3d-8d2d-f865be614c56" />
<img width="1080" height="2374" alt="Screenshot_2026-05-09-11-37-05-76_b29aabb9387aa77602b391a7c331c2dc" src="https://github.com/user-attachments/assets/2c69cfad-ae78-409d-88f2-2cfec61725e0" />


## Notes

This repository intentionally does not include the source code. It is meant to document the project publicly for portfolio, CV, and contest purposes while keeping implementation details private.
