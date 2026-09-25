# Revora Health Caseload Simulator and Revenue Calculator Concept
> A pitch ready feature prototype built on top of [Revora Health](https://revora.health/) to demonstrate high impact improvements to the care continuity landing page for PT clinics, specifically around proving value to clinic owners, making RTM revenue concrete, and warming up the demo request.

> **Live demo:** [My prototype](https://sarthak-saharan.github.io/Revora-Rebuild/) (feature concept)

> Built by Sarthak Saharan · [LinkedIn](https://www.linkedin.com/in/sarthak-saharan/) · [Portfolio](https://sarthaksaharan.framer.ai/)

## What I Built

I rebuilt Revora's homepage in its own design system and added a section for the person who actually signs the contract: the clinic owner. It has two parts. First, a one week caseload simulator where you watch six patients between visits, see who goes quiet, and press Reach out before they cancel. Flip to "Without Revora" and the same week plays out with no signal until the cancellations land. Second, a calculator where the owner sets four numbers they already know (patient volume, plan length, revenue per visit, completion rate) and Revora's own assumptions sit in a separate, prefilled panel. It turns those numbers into what dropoff costs a year and what Revora could return through kept visits and RTM billing. Every Book a demo button then opens a time picker with those numbers attached to the booking. I picked this because Revora's pitch is about money and retention, and the page never puts a number on either.

## The Problem I Spotted

The page is beautiful and the story is clear for patients. The buyer is a clinic owner, though, and the two claims that matter to them ("patients finish their plan" and "RTM revenue, captured") are stated rather than shown. The seven in ten dropoff stat sits near the top, but nothing connects it to the visitor's own clinic, so it reads as an industry fact rather than their problem. The provider view is a static stack of four cards, which undersells the core mechanic: the list reorders itself as patients go quiet. And the only conversion path is a cold "Book a demo" with no reason to click it today. A skeptical owner leaves without a figure to take to their partner or office manager.

## Before and After

| Dimension | Before (Original Site) | After (This Prototype) |
|---|---|---|
| Product understanding | Provider view shown as a still image of four stacked cards | A playable week where the caseload reorders live and flagged patients rise to the top with a Reach out action |
| The case against doing nothing | Dropoff stat stated once, in the abstract | A "Without Revora" toggle that replays the same week and ends in two cancelled visits the clinic never saw coming |
| Proof of value | "RTM revenue, captured" as a headline with no amount attached | A calculator that shows yearly dollars lost to dropoff, visits kept, and RTM captured, using the visitor's own clinic numbers |
| Demo request | Book a demo leads to a bare calendar with no context about the clinic | The time picker sits next to the visitor's own numbers (clinic size, completion rate, estimated return), and the booking carries them, so sales opens the call already knowing them |

## Target Metrics

* **Demo request rate:** +15 to 30%. Interactive ROI tools on B2B pages tend to beat static CTAs because the visitor leaves with a number they already believe.
* **Lead quality:** most booked demos arrive with clinic size and completion rate attached, which lets sales triage and personalize before the first call.
* **Engaged time on page:** +30 to 50%. The simulator asks for a few clicks per session and the calculator rewards fiddling.
* **Scroll depth past the provider view:** +20 to 35%, measured by how many visitors reach the Clara and FAQ sections after interacting.

These are estimates grounded in how ROI calculators and interactive demos usually perform on SaaS landing pages. A proper A/B test would settle them.

## How I Built It

* **Research:** Read Revora's site closely to understand who buys (outpatient PT clinic owners), what they are sold (plan of care completion, fewer cancellations, RTM billing), and where the page stops short of proving it.
* **Design extraction:** Pulled the exact tokens from the live stylesheet instead of eyeballing them. Fraunces for display type plus Revora's custom glyph font that swaps the f and j, Public Sans for body, the full cream, linen, parchment, mist, pine, teal and terracotta palette, their easing curves, and their blur and rise reveal animation.
* **Stack:** Vanilla HTML, CSS and JS in a single file with local font and image assets. No build step and no dependencies.
* **Fidelity:** The week scrubber reuses the visual language of Revora's own "visit to visit" timeline (terracotta visit dots, hollow day markers), so the new feature looks like it shipped with the page. The calculator lists its assumptions right under the result, since a clinical audience will not trust a number it cannot check.

## Run It Locally

```bash
git clone https://github.com/sarthak-saharan/Revora-Rebuild.git
cd Revora-Rebuild
python3 -m http.server 3000
```

Open http://localhost:3000

## About Me

I am Sarthak Saharan, an AI native Product Manager who builds working prototypes to test ideas before writing a PRD. I go deep on a product until I can see the gap, then ship a working fix in the real design system so people can click it instead of imagining it.

[LinkedIn](https://www.linkedin.com/in/sarthak-saharan/) · [Portfolio](https://sarthaksaharan.framer.ai/)

*Demo data only. Not affiliated with Revora Health. Built as an unsolicited product concept.*
