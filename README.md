# Copilot in Action — Learn and practice

A reusable, customer-agnostic Microsoft 365 Copilot learning site: from a first prompt to practical work across Microsoft 365.

The standalone beginner path contains 13 core guides and three optional explorations with fictional practice content, numbered steps, checkable outcomes, practice alternatives, and direct public Microsoft sources.

**Learning path:** https://moinster.github.io/copilot-in-action/start.html

## Beginner path

`start.html` is a self-contained learning path. It does not link to or require `index.html`, any existing lab, or files in `assets/`. All practice inputs are included on the page; learners create their own source document and working artifacts. Public Microsoft links provide supporting documentation rather than prerequisite course material.

| Guides | Contents |
|---|---|
| 01-05 | Work-account setup, first prompt, goal/context/source/expectations, iteration, grounding, review and privacy |
| 06-12 | Word, Excel, PowerPoint, Outlook, Teams, OneNote, Copilot Pages and the distinction from Loop |
| 13-15 | Optional Create/image generation, agents including Researcher/Analyst orientation, Copilot Notebooks |
| 16 | Cross-app challenge and self-check |

Core practice takes approximately 90 minutes. The audience already has Microsoft 365 Copilot licenses: guidance focuses on using the product, not choosing or comparing licenses. Practical notes cover app interfaces, source permissions, editing modes, and meeting transcription. Optional guides are enrichment, not a separate licensing tier. All practice data is fictional. The site never connects to Microsoft 365 or sends prompts.

Navigation supports direct lesson hashes, browser back/forward, a show-all reading mode, keyboard access, clipboard fallback, and printing all lessons. Check-offs last only for the current visit; bookmarking a lesson preserves its address, not completed status. With JavaScript disabled, all content remains readable and prompts can be copied manually.

Public Microsoft Learn and Support sources are linked within the guides, reviewed for the 22 September 2026 edition. This is everyday foundational coverage, not an exhaustive feature or licensing catalog.

The on-page practice kit includes copyable welcome-session source notes and links to the included spreadsheet exercise and document-building steps. Print all guides includes all lessons, prompts, practice inputs, and self-check answers; no separate prompt guide is required.

## Retained eight-scenario page

`index.html` and its assets remain unchanged for existing users and bookmarks. They are separate from, and not prerequisites for, the standalone learning path.

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

Every prompt in the original eight-scenario lab matches the bundled Prompt Guide verbatim, with two presentational changes:

- The guide's `<agency name>` placeholder is rendered as `[agency name]`, matching the bracket convention used elsewhere.
- Smart quotes are rendered as straight quotes so the copied text pastes cleanly into Copilot.

The executive triage brief is rendered with its priority list as bullets; the wording is unchanged.

Scenario 4 (PowerPoint Skills) has no prompt, by design — the Prompt Guide contains none, because in that scenario the instruction *is* the artifact being built. The site marks it as a live demonstration.

## Content note

All lab content is fictional. **Zava** is a fictional materials brand and **Project Northstar** is a fictional consumer research programme; every company, person, figure, and research finding is invented for Microsoft 365 Copilot demonstration purposes.

The site carries no customer name, no delivery-programme branding, and no customer-identifying content.

## Structure

```
index.html                 Original eight-scenario lab and beginner-path entry links
start.html                 Standalone learning path, inline practice kit, styles and behaviour
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
