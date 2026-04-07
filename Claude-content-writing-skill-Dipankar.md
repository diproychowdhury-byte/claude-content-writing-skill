---
name: enterprise-microcopy
description: Write, audit, and recommend interface copy (microcopy) for enterprise UI products built on or aligned with IBM Carbon Design System. Use when writing or reviewing any text in an enterprise product interface — buttons, labels, error messages, notifications, forms, empty states, onboarding, confirmations, and help text. Applies the four UX writing quality standards (purposeful, concise, conversational, clear) layered with IBM Carbon's specific content rules: sentence-case capitalization, IBM brand voice, productive tone calibration, and Carbon component-level copy patterns. **Always concludes every recommendation with a Carbon-fidelity mockup rendered as an HTML artifact** showing the copy in a realistic component context (inline field, notification banner, modal, etc.).
---

# Enterprise Microcopy (IBM Carbon)

Write and audit interface copy for enterprise UI products built on or aligned with the IBM Carbon Design System. This skill produces copy recommendations that satisfy both universal UX writing quality standards and IBM Carbon's specific content rules — and always renders each recommendation as a visual mockup so teams can evaluate copy in realistic component context.

**Compatible with:** Claude, Codex, Cursor, and other agents that support the agent skills specification.

---

## When to Use This Skill

Use when:
- Writing or reviewing any UI string in a Carbon-based enterprise product
- Auditing existing microcopy for Carbon compliance and UX quality
- Creating error messages, inline validation, notification banners, or toast copy
- Writing form labels, helper text, placeholder text, and field-level instructions
- Designing empty states, confirmation dialogs, or onboarding flows
- Establishing or checking voice/tone consistency across a product surface
- Producing copy recommendations for design review, handoff, or content audits

---

## Core Quality Standards

Every piece of UI copy must satisfy all four standards before it ships.

| Standard | What It Means |
|---|---|
| **Purposeful** | Helps users achieve a goal or serves a clear business objective |
| **Concise** | Uses the fewest words possible without losing meaning |
| **Conversational** | Sounds natural and human; reads the way a knowledgeable colleague would speak |
| **Clear** | Unambiguous, accurate, and immediately understandable |

---

## IBM Carbon Voice and Tone

### Voice (Always Consistent)
IBM voice is the stable personality beneath all product copy. Per IBM Brand Center, it:
- Has a clear point of view — direct and confident, never vague
- Is simple and logical — persuasive, not poetic
- Elevates facts and outcomes over decoration
- Engages the thinker by speaking like the thinker
- Uses figurative language only for emphasis, never ornament
- Is confident but never boastful

**What this means in practice:** Copy should feel like expert guidance — efficient, precise, grounded in what the user needs to do next. No marketing fluff. No hedging.

### Tone (Adapts to Situation)
Tone is how voice flexes to match the user's context and emotional state. The underlying voice is constant; word choice and sentence structure adapt.

| Situation | Tone | Approach |
|---|---|---|
| Error / failure | Economical, direct | Short phrases; explain cause; give recovery path |
| Onboarding / getting started | Friendly, patient | Full sentences; explain why; celebrate early wins |
| Routine tasks (return users) | Efficient, minimal | Confirmation only; skip explanation |
| High-stakes / destructive actions | Serious, transparent | State consequences clearly; never manipulate |
| Empty / first-use states | Hopeful, actionable | Explain why it's empty; clear CTA |
| Permissions requests | Benefit-led | Lead with user value before asking |

**Exclamation marks:** Use positively, sparingly (one per context maximum). Never use on error or warning messages.

**Contractions:** Allowed and encouraged when they improve flow and match tone.

**Sentence starters (And, But, So):** Permitted when they allow for shorter, more scannable sentences — but do not overuse.

---

## IBM Carbon Writing Rules

These are non-negotiable Carbon-specific requirements. Apply them to every UI string.

### 1. Sentence-Case Capitalization — Always
Carbon mandates sentence case for **all** UI text elements.

- Capitalize only: the first word of a string + proper nouns + trademarked product/service names
- Do **not** use title case for headings, buttons, labels, nav items, or tab labels
- Do **not** use all-caps (slows reading, reduces legibility)
- UI component names (button, tab, modal) are **not** proper nouns — write them lowercase

| ❌ Title Case | ✅ Sentence Case |
|---|---|
| Save Your Changes | Save your changes |
| View Account Settings | View account settings |
| Delete All Files | Delete all files |
| First Name | First name |

**Exception:** Official IBM product/service names and trademarked terms retain their registered capitalization (e.g., IBM Watson Studio, IBM Cloud).

### 2. Second Person by Default
- Use **you / your** as the primary voice in UI copy
- Use **My** (first person) only for labels tied directly to user-owned data: "My account", "My usage"
- Switch to second person in any explanatory text following a first-person label: "Your usage is calculated from the first day of the month."
- Use **we / our** (IBM first person) only in contexts where the user benefits from knowing IBM is the actor — e.g., data collection disclosures: "We use this to personalize your experience."

### 3. Punctuation Rules
- **Labels** (field labels, button labels, nav items): No terminal punctuation
- **Helper text** (persistent below a field): Full sentences with terminal punctuation
- **Placeholder text**: Direct statement, no punctuation
- **Error messages**: Short phrases or full sentences depending on complexity; always include a period if it's a full sentence
- **Tooltip content**: Full sentences with punctuation
- **Confirmation dialogs**: Full sentences with punctuation
- Do **not** use colons after form field labels

### 4. Abbreviations and Acronyms
- Spell out on first use if the term might be unfamiliar to the target audience
- Use all-caps for well-recognized initialisms (IBM, API, GIF, URL)
- Use the official full product name on first reference unless a shortened form is explicitly approved (e.g., IBM CICS)

### 5. Feature and Component Names
- Do **not** capitalize feature names unless they are sold separately or trademarked
- Carbon does not recognize "important words" or "specialness" as a capitalization trigger
- This eliminates inconsistency and prevents content debt

---

## Carbon Component Copy Patterns

### Form Labels
- **Rule:** Sentence case, no colon, short noun phrase
- **Helper text:** Full sentence with punctuation; explains format or why field exists
- **Placeholder:** Sentence case, direct statement, no punctuation; use sparingly — never as a label substitute; never for crucial information
- **Required vs. optional:** In complex enterprise forms (configuration, settings), mark the minority — if most fields are optional, mark required ones. If most are required, mark optional ones.

| Element | Example |
|---|---|
| Label | `First name` |
| Helper text | `Enter the name as it appears on the account.` |
| Placeholder | `name@example.com` |
| Required indicator | `*` with legend: `* Required field` |
| Error (inline) | `Enter a valid email address.` |

### Error Messages

**Inline validation errors**
- Trigger: on field exit (blur) or on submit
- Format: Short, specific, sentence case
- Pattern: `[Specific requirement or correction needed].`
- Never blame the user; never use "invalid" alone

| ❌ Don't | ✅ Do |
|---|---|
| Invalid input | Enter a value between 1 and 100 |
| Error | Email address must include @ |
| Field is required | Enter your organization name |

**System / notification errors (banner or inline notification)**
- Tone: Economical, direct — short phrases preferred over full paragraphs
- Pattern: `[What failed]. [Why, if known]. [What to do next].`
- Link to recovery action when possible

| ❌ Don't | ✅ Do |
|---|---|
| An error has occurred | Connection lost. Changes weren't saved. Reconnect and try again. |
| Something went wrong. Please try again. | Export failed. The file exceeds 500 MB. Split the data and export again. |

**Destructive / high-stakes confirmations**
- State consequences explicitly; do not soften or obscure
- Pattern: `[Action]? [Consequence]. [Irreversibility if applicable].`
- Confirm button: matches destructive verb ("Delete", not "OK" or "Confirm")

| ❌ Don't | ✅ Do |
|---|---|
| Are you sure? | Delete workspace? All projects and data will be permanently removed. |
| This cannot be undone. OK / Cancel | This action cannot be undone. Delete / Cancel |

### Buttons and CTAs
- **Format:** Active imperative verb + object, sentence case, no punctuation
- **Pattern:** `[Verb] [object]` — specific enough to understand without surrounding context
- Destructive actions use the destructive verb itself as the label

| ❌ Don't | ✅ Do |
|---|---|
| Submit | Save configuration |
| OK | Delete deployment |
| Click here | Download report |
| Yes | Remove user |

### Notifications and Toasts
- **Title:** Verb-first, sentence case, no punctuation
- **Body:** One sentence; full sentence with punctuation
- **Positive:** One exclamation mark permitted in title if celebratory
- **Negative/warning:** No exclamation marks; direct, recovery-focused

| Type | Title | Body |
|---|---|---|
| Success | `Deployment complete` | `Your changes are live in the production environment.` |
| Warning | `Storage limit approaching` | `You've used 90% of your allocated storage. Review usage or upgrade your plan.` |
| Error | `Export failed` | `The connection timed out. Try again or contact support if the issue persists.` |
| Info | `Scheduled maintenance` | `The system will be unavailable on March 12 from 2:00–4:00 AM UTC.` |

### Empty States
- **First-use:** Explain what the space is for + primary action to populate it
- **User-cleared:** Acknowledge + path to add content
- **No results:** Clarify search/filter scope + offer to broaden or reset

| Type | Headline | Body | CTA |
|---|---|---|---|
| First-use | `No deployments yet` | `Create a deployment to run your application in a managed environment.` | `Create deployment` |
| No results | `No results for "prod-cluster-07"` | `Check the spelling or adjust your filters.` | `Clear filters` |

### Onboarding and Getting Started
- Use full sentences with friendly explanations — this is the highest-conversational-tone context
- Explain *why* steps matter, not just *what* to do
- Celebrate early wins with one positive acknowledgment (one exclamation mark maximum)

---

## Tone Calibration by User Emotional State

| User State | Voice Adjustments |
|---|---|
| **Frustrated** (error, blocker) | Empathetic, solution-first. No blame. Short phrases. Clear next step. |
| **Confused** (first use, complex feature) | Patient, explanatory. Full sentences. Context before action. |
| **Confident** (routine task) | Minimal. Confirmation only. Skip explanation. |
| **Cautious** (destructive action, data loss) | Serious. State full consequences. No manipulation or false urgency. |
| **Successful** (completion, achievement) | Brief, positive. Proportional to achievement. One celebration maximum. |

---

## Accessibility Requirements

Carbon's content accessibility requirements apply to all microcopy:

- **Screen reader labels:** All interactive elements must have explicit, descriptive labels ("Submit application", not "Submit")
- **Link text:** Descriptive and meaningful out of context ("Read the privacy policy", not "Click here")
- **Error messages:** Must pair with field label when read by a screen reader — write them to make sense as: `[Field label]: [Error text]`
- **Color independence:** Never rely on color alone to convey meaning — pair with text or icon
- **Sentence length:** Target 8–14 words for instructions (8 words = 100% comprehension; 14 words = 90%)
- **Reading level:** 7th–8th grade for general enterprise audiences; up to 10th–11th grade for technical/developer tools
- **Avoid:** idioms, sarcasm, regional colloquialisms, emoticons in UI copy

---

## Sentence Length and Character Targets

| Element | Word Target | Character Target |
|---|---|---|
| Button label | 2–4 words (6 max) | 15–25 characters |
| Form field label | 2–4 words | 10–30 characters |
| Inline error | 6–12 words | 30–55 characters |
| Notification title | 3–6 words | 20–40 characters |
| Notification body | 10–20 words | 55–100 characters |
| Helper text | ≤20 words | ≤100 characters |
| Tooltip | ≤25 words | ≤120 characters |
| Empty state headline | 3–6 words | 20–40 characters |
| Empty state body | ≤20 words | ≤100 characters |
| Confirmation body | ≤30 words | ≤150 characters |

---

## Editing Checklist (Four-Phase Review)

Run every string through this sequence before finalizing.

**Phase 1 — Purposeful**
- [ ] Does this help the user complete their task?
- [ ] Does it serve a clear business objective?
- [ ] Is the user benefit visible or implied?

**Phase 2 — Concise**
- [ ] Can any word be removed without changing meaning?
- [ ] Is the most important information front-loaded?
- [ ] Are redundant phrases eliminated?

**Phase 3 — Conversational**
- [ ] Would a knowledgeable colleague say this out loud?
- [ ] Is active voice used (unless passive is clearly clearer)?
- [ ] Are contractions used where they aid flow?

**Phase 4 — Carbon-Compliant**
- [ ] Sentence case throughout (not title case)?
- [ ] Second person (you/your) unless first-person exception applies?
- [ ] Correct punctuation for element type (label = no period; helper text = period)?
- [ ] No all-caps (unless well-known abbreviation)?
- [ ] Feature names lowercase (unless trademarked)?
- [ ] Exclamation marks used only positively and no more than once per context?
- [ ] No blame language in error messages?
- [ ] Destructive confirmations state consequences explicitly?

---

## Common Mistakes to Avoid

| Mistake | Carbon / UX Rule Violated |
|---|---|
| Title Case Button Labels | Carbon: always sentence case |
| "Submit" on a form button | UX: generic label; be specific ("Save account settings") |
| "Invalid input" error | UX: no blame; Carbon: be specific and direct |
| "An error has occurred" | UX: vague; no recovery path |
| Placeholder text as label replacement | Carbon: placeholder disappears on type; always use persistent label |
| "Click here" links | Accessibility: non-descriptive out of context |
| Exclamation mark on error message | Carbon: only positive contexts |
| Capitalizing UI component names | Carbon: not proper nouns |
| All-caps headings or labels | Carbon: slower to read, accessibility risk |
| Passive voice predominance | UX: weakens clarity and user agency |

---

## Mockup Requirement

**Every copy recommendation produced by this skill must include a rendered HTML mockup.**

The mockup must:
1. Use realistic Carbon Design System visual conventions — IBM Plex Sans typeface (or system sans-serif fallback), Carbon color tokens (white background `#ffffff`, text `#161616`, interactive blue `#0f62fe`, error red `#da1e28`, success green `#198038`, warning yellow `#f1c21b`), Carbon spacing scale (multiples of 4px/8px), 1px `#e0e0e0` borders
2. Show the copy string in the **correct component type** — do not show button copy in a modal, or error copy in a standalone paragraph
3. Include all relevant component states if the recommendation addresses multiple states (e.g., default + error + success for a form field)
4. Label the mockup clearly so reviewers can identify which copy string is being evaluated
5. Be self-contained HTML (inline CSS, no external dependencies) unless the task specifies otherwise

**Component type selection guide:**

| Copy Type | Mockup Component |
|---|---|
| Form label / helper / error | Text input field with label, helper text zone, inline error state |
| Button copy | Primary or ghost button in correct hierarchy |
| Inline notification / toast | Carbon notification banner (error / warning / success / info variant) |
| Modal confirmation | Modal dialog with title, body, and action buttons |
| Empty state | Card or full-panel empty state with headline, body, and CTA button |
| Tooltip | Interactive element with tooltip overlay |
| Onboarding | Contextual guidance panel or getting-started tile |

---

## Workflow

1. **Intake** — Identify the component type, user goal, error/state context, and emotional state of the user at this moment in the journey
2. **Draft** — Write 1–3 candidate strings applying Carbon voice, sentence case, correct punctuation, and second-person rule
3. **Edit** — Run the four-phase checklist; cut until every word is earning its place
4. **Carbon compliance check** — Verify sentence case, punctuation rules, persona rules, exclamation mark policy
5. **Accessibility check** — Verify screen-reader label quality, reading level, color-independence
6. **Mockup** — Render the final recommendation in an HTML artifact using the correct Carbon component type and color tokens
7. **Rationale** — Briefly explain why the chosen copy satisfies each of the four quality standards

---

## Quick Reference Card

| Rule | Correct | Incorrect |
|---|---|---|
| Capitalization | `Save changes` | `Save Changes` |
| Button label | `Delete deployment` | `Submit` / `OK` |
| Form label | `Email address` | `Email Address:` |
| Placeholder | `name@example.com` | `Enter your email address here` |
| Helper text | `Use the format DD/MM/YYYY.` | `Use the format DD/MM/YYYY` (missing period) |
| Inline error | `Enter a date in the future.` | `Invalid date` |
| Notification title | `Export complete` | `Export Complete!` |
| Destructive confirm | `Delete pipeline? This action cannot be undone.` | `Are you sure?` |
| Exclamation (positive only) | `Deployment complete!` | `Limit reached!` |
| Feature name | `Use the quick start wizard` | `Use the Quick Start Wizard` |

---

## Reference Sources

- IBM Carbon Design System — Content guidelines: https://carbondesignsystem.com/guidelines/content/overview/
- IBM Carbon Design System — Writing style: https://carbondesignsystem.com/guidelines/content/writing-style/
- IBM Carbon Design System — Form usage: https://carbondesignsystem.com/components/form/usage/
- IBM Carbon Design System — Text input usage: https://carbondesignsystem.com/components/text-input/usage/
- IBM Carbon Design System — Typography: https://carbondesignsystem.com/guidelines/typography/overview/
- The IBM Style Guide: Conventions for Writers and Editors (IBM Press, 2011)
- IBM Brand Center verbal expression guidelines (IBMers)
- IBM Accessibility content design guidance: https://www.ibm.com/able/
- WCAG 2.1 AA: https://www.w3.org/TR/WCAG21/
