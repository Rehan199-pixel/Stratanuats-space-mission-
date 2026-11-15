# AI use disclosure — how Super Intelligence was used in this project

**Project:** Stratanauts Space Mission · **Team:** The Stratanauts (6 members), Kopargaon, India
**Event:** NASA Space Apps Challenge 2026 · **Challenge:** Space Mission Design Game

NASA Space Apps permits Super Intelligence (SI) tools and asks teams to say clearly where and how they were used. This file is that statement for the repository. It matches `../02_Project-Documentation/AI-Use-Disclosure.pdf` in the submission Drive folder.

## Tools, and exactly what each one did

| Tool | Used for | What the team did | Where it shows up |
|---|---|---|---|
| **Lovable** (AI application builder) | Generating and editing application code: UI components, the 3D hub scenes, the NASA/JPL data layer, budget and readiness logic, translations | Directed every change, specified the mechanics and numbers, reviewed each build in the live preview, tested the whole mission flow, rejected and reworked what did not work | The deployed app and this repository |
| **AI text-to-speech** | Reading the team-written narration aloud for the 28-second project demo and the extended walkthrough | Wrote the script, chose the wording, checked every claim in it, approved the final audio | The voice in the demo videos (Drive folder) |
| **AI assistants for drafting** | Drafting and formatting help on documentation and submission text | Supplied the facts, corrected the drafts, verified every link and figure before publishing | `docs/`, the submission Drive folder |

The in-app mentor character *Dr. Ayesha* uses the **browser's built-in speech synthesis** — no cloud speech service and no shipped AI audio file inside the application.

## Where SI output is labelled

- **Video:** every frame of the demo carries the on-screen line *"AI-assisted narration and SI-assisted development — disclosed"*.
- **Video metadata:** the same statement sits in the MP4 `title`, `artist`, `comment` and `description` tags, so the disclosure travels with the file if it is re-uploaded.
- **Repository:** this file and [`nasa-ai-disclosure.md`](nasa-ai-disclosure.md).
- **Submission:** the *Use of Super Intelligence (SI)* field on the Project tab.
- **No NASA branding:** no NASA logo, wordmark or implied endorsement anywhere in the interface or media.

## What the team did itself

- The concept, the challenge framing, the 14-step mission flow, the budget model, the seven-station readiness poll and the debrief scoring.
- Every source and constant in the model, each cited in the references document.
- The narration script, all slide and documentation text, and the decision about what to cut to fit the 30-second demo limit.
- All testing: end-to-end mission flow, GO / HOLD behaviour, the language switcher, and the offline fallback when a NASA endpoint is unavailable.

SI tools were instruments. No factual claim, citation, dataset or design decision in this project was published without the team checking it.

## What is not here

- No AI-generated images or video of people. Every screenshot and every frame of footage is captured from the running application.
- No likeness of any person under 18.
- No personal data, API keys, credentials or secrets in the repository or in the history of it.
