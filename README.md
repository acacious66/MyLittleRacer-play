# My Little Racer — Play

A portrait HTML5 toy racing game. This public repository contains only the browser build, release notes and GitHub Pages deployment workflow. Development source is maintained separately in a private repository.

[Play My Little Racer](https://acacious66.github.io/MyLittleRacer-play/)

## English edition — 2026-11-11

The complete interface, car-preview labels, canvas messages, tooltips, accessibility descriptions, instructions and result screens are in English. Bomb countdowns on the car and in both warning areas display whole seconds, without changing fractional internal timing. English copy wraps within narrow portrait screens. Legacy settings, skins, coins and results remain compatible.

This branch contains the prepared English update; the live site changes after its PR is merged and Pages deployment succeeds.

## Gameplay

- Collect coins along the road. Each cleared round awards 20 coins; completing all three rounds adds 100 coins. Exchange coins for cosmetic skins in the existing garage. A separate shop is deferred.
- Existing points migrate to coins one-to-one, preserving skins, records and customization. Coins and settings remain local to this browser; there is no database, account or cross-device synchronization.
- Each hazard group contains three individual bombs, staggered sideways and 160 world units apart, with room to dodge. Round one has two groups; later rounds have three. A shared water puddle appears 420 units after the last bomb.
- Bomb contact starts an eight-second fuse shown on the car. Further bomb contacts do not reset it. Reach water before expiry to defuse it. An explosion costs one life and half the current round's road coins, rounded up and capped at ten; historical savings are protected.
- Arming, ticking, urgent final-three-second warnings, water rescue and explosion sounds. Music and effects retain independent symbol controls; music starts after user interaction when enabled.
- Three original synthesized rock tracks, one per round, with different riffs, keys and tempos. No third-party recordings or audio downloads.
- Straight first round, seeded random bends and changing widths in later rounds, varied regular obstacles, neon presentation and cosmetic car customization.
- Swipe left/right to steer and up/down to accelerate/brake; diagonal gestures combine inputs. Keyboard arrow keys support the same combinations.
- Three rounds of 4000 metres with 30/25/20-second limits and three lives per round. Pause, exit, timing records and local persistence remain available.

This branch updates the live site only after its pull request is merged into `main` and the Pages workflow succeeds. The existing Pages workflow is unchanged. No game backend is required.

## Validation

TypeScript checking, 70 unit tests and production build passed. English DOM/SVG/canvas and fallback-message audits passed at 320×568 and 390×844, including success, timeout and out-of-lives results and whole-second bomb displays. Four portrait layouts, loot, progression and music checks passed. Tests cover wallet migration, rewards, pickup ordering, fuse timing and seeded route reachability. Browser gameplay assertions passed for complete three-round dodge and rescue runs, on-car countdown, audio switching, persistence, four portrait viewport sizes and the production subpath. All three actual audio renders are distinct and non-silent with no clipping detected. Desktop mobile viewport checks are not physical iPhone Safari tests. Existing large-bundle warning remains.
