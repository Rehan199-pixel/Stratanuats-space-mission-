# Tech Stack, Dependencies and Attribution

## 1. Runtime, frameworks and libraries (versions from `package.json`, verified 13 Nov 2026)
| Package | Version | Purpose | Licence |
|---|---|---|---|
| react / react-dom | 19.2 | UI rendering | open source |
| @tanstack/react-start | 1.168.35 | SSR and server functions | open source |
| @tanstack/react-router | 1.170.18 | Typed routing | open source |
| vite | current | Build tool and dev server | open source |
| typescript | current | Typed JavaScript | Apache-2.0 |
| tailwindcss | 4.2.1 | Styling | open source |
| three | 0.186 | 3D scenes | open source |
| @react-three/fiber | 9.x | React renderer for three.js | open source |
| @react-three/drei | 10.x | 3D helpers and controls | open source |
| zustand | 5.0.15 | Mission state store | open source |
| @supabase/supabase-js | 2.117.2 | Cache database client | open source |
| drizzle-orm | current | Schema and queries for the cache | Apache-2.0 |
| i18next / react-i18next | 26.4.2 | Six-language localisation | open source |
| radix-ui primitives | current | Accessible UI primitives | open source |
| lucide-react | current | Icons | ISC |
| recharts | current | Telemetry charts | open source |
| zod · react-hook-form | current | Validation and forms | open source |
| sonner | current | Toasts | open source |
| clsx / tailwind-merge | current | Class utilities | open source |

Deployment: Vercel with the Nitro serverless engine. Package manager: bun and npm lockfiles are both present.

## 2. Fonts
| Font | Use | Licence |
|---|---|---|
| Rajdhani | Display / UI headings | SIL Open Font License 1.1 |
| Share Tech Mono | Numeric / telemetry text | SIL Open Font License 1.1 |

Loaded via Google Fonts. OFL permits web embedding and redistribution with attribution.

## 3. NASA and partner material
| Asset / dataset | Where used | Terms & credit |
|---|---|---|
| NSSDCA Planetary Fact Sheet | Destination facts, physics constants | NASA public data; cited in-app and in documentation |
| JPL Approximate Positions of the Planets | Mean orbital elements | NASA/JPL public data; cited |
| JPL Horizons (live) | Today's Earth→target distance, light-time | NASA/JPL public API; labelled "Live · Horizons" |
| NASA DONKI (live) | Space-weather station | NASA CCMC public API; labelled LIVE / CACHED / DEMO |
| NASA APOD (live) | Daily astronomy briefing | NASA public API; credited on screen |
| NASA NeoWs (live) | Close approaches → debris-hazard field | NASA/JPL CNEOS public API; credited on screen |
| DSCOVR EPIC · Mars Rover Photos · JPL SBDB · JPL Sentry | Supported in the server proxy, connected to no screen | Declared **not live**; not presented as a feature |
| NASA Image and Video Library | Mission-brief destination imagery | NASA Media Usage Guidelines; images not altered to mislead |
| NASA 3D Resources — MRO model | Reference spacecraft view | Credit in-app: "NASA MRO · Reference only · NASA/JPL-Caltech / Brian Kumanchik" |
| NASA Visible Earth — Blue Marble | Earth texture | Credit in-app: "Earth · NASA / Reto Stöckli · Blue Marble" |
| SLS / Orion / RL10 / NSTAR / NERVA / MMRTG references | Vehicle and engine parameters | Technical facts from NASA publications; cited in documentation §11 |

**NASA Media Usage Guidelines summary:** NASA content is generally not subject to copyright in the United States, but NASA does not endorse or sponsor this project, and any identifiable person or third-party rights must be respected. This project therefore displays: *"Independent educational project · Not endorsed by NASA."* and never uses the NASA insignia or logotype as a project logo.

## 4. Originality, code lineage and AI assistance
### 4.1 What the team built
The challenge interpretation and concept; the full gameplay loop; spacecraft configuration and decision systems; the rescue-mission concept; the choice of NASA/JPL sources; the provenance-labelling rule; visual direction; testing; feature selection; demonstration and submission.

### 4.2 Code lineage (disclosed)
The repository `LICENSE` carries two copyright lines: *"Team Stratanauts (Stratanauts Space Mission modifications)"* and *"Team Ghost Hunter (Mission Forge)"*. Part of the codebase descends from the earlier open-source **Mission Forge** project. That attribution is retained deliberately and disclosed here rather than removed.

### 4.3 AI assistance (disclosed)
The application was built with the **Lovable AI app builder** under team direction — code generation, UI implementation, debugging, 3D scenes, data-layer code, translations and documentation. All AI output was run in the live preview and then kept, changed or discarded by the team. AI was not the source of any NASA value: NASA/JPL values are fetched at runtime from the cited sources, and simplified mechanics are labelled as game estimates. Mentor dialogue uses the browser's speech synthesis. Full statement: repository `AI_USE.md`, `docs/nasa-ai-disclosure.md`, and the AI-Use Disclosure document in the submission Drive folder.

### 4.4 Third-party assets
NASA imagery and NASA 3D Resources under the NASA Media Usage Guidelines (credited in-app); Google Fonts under SIL OFL 1.1; open-source libraries, each under its own licence. No NASA insignia is used as project branding.

## 5. Checklist before publishing the repo
- [ ] `LICENSE` present at the repository root so the licence notice is visible
- [ ] `README.md` present with setup steps
- [ ] `TECH-STACK-AND-CREDITS.md` present
- [ ] No `.env`, API keys or credentials in history (`git log -p | grep -i "api_key"`)
- [ ] `node_modules/` and `dist/` not committed
- [ ] `.env` removed from the repository and any archive (keep `.env.example` only)
- [ ] Placeholder names/URLs removed from `README.md`
- [ ] `AI_USE.md` and `docs/nasa-ai-disclosure.md` `[TEAM TO CONFIRM]` items resolved
- [ ] Public visibility confirmed in an incognito window
