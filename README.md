# Team Ownership Simulator

A short browser experience (about 4 minutes) for managers. You decide, in four connected scenes, how to help a team member called Alex. Then you see what your help does to Alex's ownership and trust over time.

## Run it
Open `app/index.html` in any modern browser. No install, no server, no internet.

## What it does
- **Four connected scenes:** a client presentation, an angry customer, blocked data from another team, and a decision while you are on holiday. Alex's words and behaviour in later scenes depend on your earlier choices.
- **Five kinds of help:** take over, coach, show then step back, remove an obstacle, leave alone. No single answer is always right. Taking over lowers ownership, leaving Alex alone lowers trust, and sometimes only the manager can remove a blocker.
- **Consequences you can see:** a pop-up after each choice (what happened, what Alex thinks, what you feel), two meters, a timeline of choices, and an ending three months later with a chart of ownership over time.
- **Replay and restart:** try another response, previous or next scene, the clickable choice dots, and "replay from" 1–4. State is saved in the browser and survives a reload.
- **For busy managers:** a home page with situations tagged by urgency, and a Report button that jumps to the result.
- **English and German:** a switch in the header.

## How it is built
One HTML file with plain JavaScript and CSS, no libraries.
- **Data:** scenes and choices live in one list, and each choice changes ownership and trust.
- **State:** two numbers plus a snapshot before every scene, so replay restores the exact state.
- **Rules:** ownership 0–41 means Alex waits for you, 42–61 means Alex asks first, 62–100 means Alex comes with a plan. Trust below 40 means Alex leaves the team.

## Tested
A headless-browser script played all 192 possible paths (4 × 4 × 4 × 3) and checked every button, replay, reload and the language switch. There were no errors.

## Files
| Path | Content |
|---|---|
| `app/index.html` | The app |
| `app/process.html` | One-page overview: steps, requirements, scenes, tests, decisions |
| `docs/NOTE.pdf` | Short note: main decision, AI output corrected, what is unfinished |
| `docs/README.pdf` | How the app works (PDF) |
| `docs/How_I_built_it.docx` | Step-by-step explanation |
| `docs/requirements.md` | The requirements checklist used during the build |

## Shortcuts
The numbers are my judgement and should be tuned by an expert. Fixed text, no live AI model. The German needs a native speaker review. Not yet tested with real managers.

Built with Claude Code.
