# Copilot in Action — PowerPoint & Outlook

A reusable, customer-agnostic Microsoft 365 Copilot lab: *Making Copilot real across PowerPoint and Outlook.*

A single-page walkthrough of eight scenarios, with every prompt copy-ready and every lab file downloadable in the place it is actually used. No customer name, no programme branding, no session numbering — point any engagement at it.

**Live site:** https://moinster.github.io/copilot-in-action/

## What's here

| Section | Contents |
|---|---|
| 1 · Welcome | Objectives, prerequisites, practice-data note |
| 2 · Lab files | The three attendee files, plus a scenario → file matrix |
| 3–6 · PowerPoint | Grounded content generation, template-based creation, Brand Kits, Skills |
| 7–10 · Outlook | Inbox prioritization, calendar governance, inbox clean-up, executive triage assistant |
| 11 · Q&A | Open floor and next steps |

The PowerPoint scenarios are a chain: scenario 1 produces the unpolished deck that scenario 3 restyles, and scenario 2 produces the on-brand deck that scenario 4 runs Skills against.

## Lab files

Served from `assets/` and linked from both the Field kit rail and the scenarios that use them.

| File | Used by |
|---|---|
| `Northstar_Consumer_Research_Summary.docx` | PowerPoint 1, PowerPoint 2 |
| `Zava_Corporate_Template.pptx` | PowerPoint 2, PowerPoint 3 |
| `Copilot_Prompt_Guide.docx` | All eight scenarios |

The Outlook scenarios need no files — they run against the attendee's own mailbox, calendar, and work context.

## Delivering this to a customer

Nothing needs editing to run it. Two placeholders are filled in live by attendees, not by the presenter:

- **`[agency name]`** in the Outlook prioritization criteria — attendees substitute the agency, partner, or account team they actually work with. Prioritization only has value when the criteria are theirs.
- **`Marketing Director`** as the audience in both PowerPoint prompts — a worked example. Attendees outside marketing swap in whoever they actually present to; the point of the prompt is that the audience is *stated*, not which audience it is.

Everything else — the Zava brand and Project Northstar research — is fictional practice data that works for any audience.

## Prompt fidelity

Every prompt rendered on the site matches the bundled Prompt Guide verbatim, with two presentational changes:

- The guide's `<agency name>` placeholder is rendered as `[agency name]`, matching the bracket convention used elsewhere.
- Smart quotes are rendered as straight quotes so the copied text pastes cleanly into Copilot.

The executive triage brief is rendered with its priority list as bullets; the wording is unchanged.

Scenario 4 (PowerPoint Skills) has no prompt, by design — the Prompt Guide contains none, because in that scenario the instruction *is* the artifact being built. The site marks it as a live demonstration.

## Content note

All lab content is fictional. **Zava** is a fictional materials brand and **Project Northstar** is a fictional consumer research programme; every company, person, figure, and research finding is invented for Microsoft 365 Copilot demonstration purposes.

The site carries no customer name, no delivery-programme branding, and no customer-identifying content.

## Structure

```
index.html                 Self-contained page — markup, styles, and behaviour
.nojekyll                  Serve files verbatim from GitHub Pages
assets/                    Attendee files
```

No build step and no dependencies. Open `index.html`, or serve the folder:

```
python -m http.server 8099
```

The design system is shared with the executive Copilot lab, so the two sites read as one family.

## Deployment

Published as a GitHub Pages site from `main`, root. Feature availability for Brand Kits, Skills, calendar instructions, and scheduled prompts varies by licence, tenant configuration, and release channel — the page states this in its footer rather than asserting availability.
