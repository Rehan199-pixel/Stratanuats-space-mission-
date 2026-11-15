# Stratanauts Space Mission

**A playable 3D space-mission design game built on five live NASA/JPL services.**
NASA International Space Apps Challenge 2026 · Challenge: *Space Mission Design Game* · Team **The Stratanauts**, Kopargaon, India.

> Choose a destination. Engineer a spacecraft. Survive a Flight-Director GO/NO-GO poll. Fly the mission, decide the hazards, and learn from a debrief built from your own numbers.

| | |
|---|---|
| **Play it now** | https://stratanauts-space-mission.vercel.app |
| **28-second demo** | https://drive.google.com/file/d/1cVpSmypy2a_UV3AgKfxDVHFMBP9hUBq4/preview |
| **Full submission (Drive)** | https://drive.google.com/drive/folders/1Mws28lQntObffWkKjuPTt0fuIvPHAgHb |

No install, no account, no cost. Runs in any modern browser.

![The 3D hub](docs/screenshots/01-hub.png)

---

## Why this exists

Mission design is taught as separate subjects — Δv in one lesson, solar flux in another, power budgets in a third — so students can calculate but cannot judge what happens when those systems fight each other under one budget. This game makes them fight, then explains the outcome.

## What you actually do

1. **Choose a world** — Moon, Mars, Ceres, Jupiter or Saturn, with real gravity, orbital period and distance from the Sun.
2. **Design the mission in 14 steps** — objective, route (Hohmann / fast / science flyby / gravity assist), budget posture, fuel, power, communications, instruments, spacecraft preset.
3. **Build it in a 3D hangar** — RL10 cryogenic, NSTAR ion or NERVA nuclear thermal; tanks, solar wings, RTG, battery, antennas, debris shield. Mass, power and Δv recalculate on every change.
4. **Face seven readiness stations** — booster, propulsion, power, comms, shielding, science and *live NASA DONKI space weather* each return GO / HOLD / NO-GO.
5. **Launch and fly** — staged SLS ascent, telemetry, correction burns, hazard decisions, rescue, then the arrival sequence in the correct physical order.
6. **Read the debrief** — Objective · Science · Safety · Resources · Landing, with a lesson generated from your own numbers. Missions are archived for comparison.

Plus a **Science Lab** with seven narrated steps per concept, and a **Crew Mission** mode for 2–4 players with role setup and voting.

## What it looks like

| Choose a world — every constraint follows from it | Seven stations vote GO or HOLD |
|---|---|
| ![Choose a world](docs/screenshots/02-choose-a-world.png) | ![GO / NO-GO poll](docs/screenshots/03-go-no-go-poll.png) |

| Countdown, ascent, orbit insertion |
|---|
| ![Launch](docs/screenshots/04-launch.png) |

## NASA and JPL data

| Source | Used for | Status |
|---|---|---|
| NASA APOD | Daily astronomy briefing | Live |
| NASA NeoWs | Close approaches → debris-hazard field | Live |
| NASA DONKI (FLR) | Space-weather GO/NO-GO station — the only live source that changes gameplay | Live |
| NASA Image and Video Library | Destination imagery | Live |
| JPL Horizons | Planet positions, real Earth→target distance, light-time | Live |
| NASA NSSDCA Planetary Fact Sheet | Diameter, gravity, period, distance constants | Published data |
| NASA SLS / Orion, Glenn RL10, Dawn NSTAR, Glenn NERVA, RPS MMRTG | Lift limit, ascent events, engine and power performance | Published specs |
| DSCOVR EPIC · Mars Rover Photos · JPL SBDB · JPL Sentry | Supported in the server proxy, connected to no screen | **Not live — declared** |

Every external value carries a provenance label in the interface: **LIVE**, **CACHED**, or **DEMO DATA** when a source is unavailable. Simplified game mechanics are labelled **game estimate** and NASA-derived values **NASA source**. We never let a player mistake one for the other. Spacecraft geometry and planet textures are generated in code (Three.js) or bundled from NASA public assets under the NASA Media Usage Guidelines.

## Tech stack

| Layer | Technology |
|---|---|
| UI | React 19, TanStack Start v1 + TanStack Router, Vite, TypeScript |
| Styling | Tailwind CSS v4, Radix UI primitives, lucide-react |
| 3D | three.js r186, @react-three/fiber v9, @react-three/drei v10 |
| State / forms | Zustand v5, React Hook Form, Zod |
| i18n | i18next — English, বাংলা, हिन्दी, Español, العربية (RTL), Français |
| Server | one NASA/JPL proxy server function with a cache; keys never reach the browser |
| Data store | Supabase (Postgres) cache, Drizzle ORM |
| Deploy | Vercel (Nitro serverless) |

Full dependency list and licences: [`TECH-STACK-AND-CREDITS.md`](TECH-STACK-AND-CREDITS.md) · data sources and provenance labels: [`docs/data-sources.md`](docs/data-sources.md)

## Run it locally

```bash
git clone https://github.com/Rehan199-pixel/Stratanuats-space-mission-.git
cd Stratanuats-space-mission-
npm install
cp .env.example .env      # add your own NASA API key (https://api.nasa.gov) and Supabase values
npm run dev               # http://localhost:5173
```

Build and lint:

```bash
npm run build
npm run lint
```

The app degrades gracefully without keys: it falls back to NASA's rate-limited `DEMO_KEY` and labels data **DEMO DATA**.

## Project structure

```
src/
  components/game/        mission screens, crew mode, archive, science lab, mentor
  components/game/city/   the walkable 3D hub
  components/ui/          design system
  lib/                    mission-sim (Δv, power, readiness, scoring), nasa.functions (proxy)
  locales/                six language bundles
  routes/                 TanStack routes and server functions
public/                   bundled NASA imagery and models
docs/                     data sources, limitations, credits, AI disclosure
```

## AI-use disclosure

This application was built with the **Lovable AI app builder** under the team's direction. AI generated code, UI, debugging help, translations and documentation drafts; every change was run in the live preview and kept, changed or discarded by the team. AI was never the source of a NASA value. Full disclosure: [`AI_USE.md`](AI_USE.md) and [`docs/nasa-ai-disclosure.md`](docs/nasa-ai-disclosure.md). The mentor character's voice uses the browser's built-in speech synthesis.

## Licence and attribution

- **Source code:** © Team The Stratanauts 2026 — see [`LICENSE`](LICENSE). Free to use, copy and adapt for education and research, with credit to Team The Stratanauts. The same file carries an attribution line for *Team Ghost Hunter (Mission Forge)*: part of this codebase descends from that earlier open-source project, and that attribution is retained.
- **NASA imagery, models and data:** used under the [NASA Media Usage Guidelines](https://www.nasa.gov/nasa-brand-center/images-and-media/), credited in-app and in the documentation.
- **Fonts:** Rajdhani and Share Tech Mono, SIL Open Font License 1.1.
- **Libraries:** open-source, individually listed in `TECH-STACK-AND-CREDITS.md`.

This is an independent educational project. **It is not endorsed by or affiliated with NASA.**

## Team

| Member | Role |
|---|---|
| Rehan Shaikh | Team Lead — product concept, mission systems, integration |
| Shubham Rajendra Tanpure | Mission simulation and data layer |
| Omkar Maruti Karad | 3D scene and visual design |
| Tejas Bhaurav Thombare | Gameplay and readiness systems |
| Tejas Dhavane | Testing, localisation and documentation |
| Atharav Joshi | Demo, presentation and outreach |

## Known limitations

Δv and transit times are rounded, simplified figures rather than computed trajectories; the 3D solar system compresses distances; the route map is illustrative; readiness, hazards and scoring are game rules rather than NASA flight rules; the launch sequence runs on a compressed timeline. The full list is in [`docs/limitations.md`](docs/limitations.md).

## Docs in this repository

| File | What it covers |
|---|---|
| [`AI_USE.md`](AI_USE.md) | How SI was used, by tool, and where each use is labelled |
| [`docs/nasa-ai-disclosure.md`](docs/nasa-ai-disclosure.md) | The same, mapped to the guide's code / data / audio / image requirements |
| [`docs/data-sources.md`](docs/data-sources.md) | Every NASA and JPL endpoint and reference value, with provenance labels |
| [`docs/limitations.md`](docs/limitations.md) | What is simplified, what is a game rule, what is declared but unused |
| [`TECH-STACK-AND-CREDITS.md`](TECH-STACK-AND-CREDITS.md) | Stack, assets, code lineage and AI assistance |
| [`LICENSE`](LICENSE) | © Team The Stratanauts 2026 — free for education, credit the team |
