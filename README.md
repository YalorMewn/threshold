# Threshold

A three-day immersive initiation for men ready to confront themselves, reclaim their power, and step into grounded, embodied masculinity.

## Live URL

After enabling GitHub Pages (Settings -> Pages -> Build and deployment -> Source: Deploy from a branch -> main / root -> Save), the page will be live at:

**https://yalormewn.github.io/threshold/**

## What this is

A single-page audio gateway with a multi-stage application embedded as the `#apply` subpage.

- `index.html` -- the entire experience (visualizer, hero, application form, confirmation state)
- `threshold-audio.mp3` -- the 44.57-second resonance recording that plays through the visualizer

No build step, no dependencies. Drop into any static host.

## Stack

- Plain HTML, CSS, and JavaScript
- Web Audio API + Canvas 2D for the audio-reactive radial-spike visualizer
- Google Fonts: Instrument Serif, Space Grotesk, JetBrains Mono
- Application submissions wired to Formspree (form id `mgodpjwr`)
  - Subject line: `THRESHOLD PETITION - {signalId} - {name}`
  - Reply-To routed to the applicant's email so replies go straight back to them
  - Local backup of every submission written to `localStorage.threshold_apps` before the network call

## Application flow

1. Landing reveals the audio gateway with a press-play affordance.
2. Pressing play engages a gold-and-flame radial-spike visualizer reacting to the source audio in real time. At peak amplitude moments, a flame flash overlay fires.
3. The "Begin Application" CTA transitions the page to the `#apply` subpage via in-page hash routing.
4. Three stages of screening:
   - Stage 01 -- Basic Info
   - Stage 02 -- Deeper Screening (Intent, Reckoning, Readiness, Safety & Outcome)
   - Stage 03 -- Commitment Filter (1-10 scale, willingness to unplug, willingness to follow group agreements) + a closing oath
5. Submitted petitions arrive in the facilitator's inbox via Formspree.
6. Applicant sees a "Received." confirmation with a unique signal ID and an option to copy a transcript of their answers.

## License

All rights reserved.
