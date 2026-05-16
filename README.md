# Behavioral Interview Coach

A mobile-friendly web app for practicing the behavioral interview questions hiring managers actually ask. Type your answer, get a 0–100 score with a STAR-method breakdown, and receive targeted tips to improve your content and delivery.

**Live app:** https://YOUR-USERNAME.github.io/interview-coach/

## Features

- 45 questions across 11 categories: Leadership, Conflict, Failure, Teamwork, Problem Solving, Pressure, Communication, Customer Focus, Adaptability, Ownership, and Classics
- 0–100 overall score with a STAR sub-breakdown (Situation / Task / Action / Result, 25 points each)
- Specific, targeted tips after every answer — flags filler words, hedging, weak ownership ("we" vs. "I"), missing metrics, and length issues
- Verdict labels from "Rough draft" to "Excellent"
- Progress tracking: total answers scored, average score, best score, and a recent history
- Saved locally on your device (uses `localStorage`) — no data leaves your phone
- Mobile-first responsive design; works offline once loaded
- Single self-contained HTML file — no build step, no dependencies

## Use it on your phone

1. Open the live URL above in mobile Safari or Chrome
2. Share → "Add to Home Screen" — it'll behave like an installed app

## Run it locally

Just open `index.html` in any modern browser. No server required.

## How scoring works

The scoring engine is heuristic — it analyzes your text for:

- **Situation**: time/context markers, named entities, proper nouns
- **Task**: explicit goal-statement phrases and stakes language
- **Action**: action verbs and ownership ratio (`I` vs. `we`)
- **Result**: outcome words, numbers/percentages, and reflection/learning

Deductions are applied for excessive filler words ("um", "like", "basically"), hedging ("maybe", "I think"), and answers that are too short (< 80 words) or too long (> 500 words).

## Roadmap

- **V2 — Voice-enabled**: browser-based text-to-speech reads the question, browser-based speech-to-text captures your spoken answer, scoring engine adds delivery metrics (speaking pace, filler-word frequency, pauses, answer duration)
- **V3 — Role-specific question banks**: tailored sets for Engineering Manager, Product Manager, Scrum Master / PM, and others
- **V4 — LLM-graded scoring**: optional Anthropic API integration for nuanced, context-aware grading beyond what regex can catch

## Tech

Vanilla HTML, CSS, and JavaScript. No framework, no build step, no dependencies. The full app is one file: `index.html`.

## License

MIT — see [LICENSE](LICENSE).
