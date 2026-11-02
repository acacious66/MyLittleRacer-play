# My Little Racer — Play

A portrait HTML5 toy racing game. This repository contains the browser build and GitHub Pages deployment workflow. Development source is maintained separately.

[Play My Little Racer](https://acacious66.github.io/MyLittleRacer-play/)

## Web release — 2026-11-03

- Neon garage and track, steering tilt, trails, collision feedback, and cosmetic car designs.
- Swipe left/right to steer; swipe up to accelerate and down to brake. Diagonal gestures combine both actions. Keep holding the displaced gesture to maintain input; release to return gradually to cruise.
- Keyboard: Left/Right to steer and Up/Down to accelerate/brake. Direction keys can be combined.
- Three rounds of 4000 metres, with time limits of 30, 25 and 20 seconds. Reach the finish before the deadline while preserving at least one of three lives.
- Beat your fastest successful time in each round. Completing all three rounds awards 100 points to unlock ribbon, pearl and starlight skins.
- Original synthesized music and driving effects, controlled independently with symbol buttons.
- Local persistence for customization, points, skins, timing records and audio preferences. Existing saves are supported. An unfinished series restarts after a page reload.

This branch updates the live site only after its pull request is merged into `main` and the Pages workflow succeeds. No server or account is required to play.

## Validation

TypeScript checking, 46 unit tests, production build and desktop browser automation passed, including three actual 4000-metre rounds, combined controls, timeout handling, rewards, persistence, mobile viewport layouts and audio behavior. Mobile-sized desktop browser tests do not replace actual iPhone Safari acceptance.
