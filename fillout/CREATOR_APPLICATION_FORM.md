# Meshy Creator Program - Fillout Form Spec (Lovable-Inspired)

## 1) Form Theme & Layout
**Layout:** multi-step (1 question per screen or grouped by section) with a strong intro screen.

**Theme**
- Primary button color: `#C5F955`
- Background: dark neutral (e.g., `#0f1518`) to match landing page
- Accent text: `#F6C453`
- Font pairing: modern sans for body (default Fillout is fine)
- Add logo to header (top-left)

**Intro screen copy**
- Title: `Meshy Creator Program`
- Subtitle: `Apply to create 3D content with meshy.ai, earn revenue share, and get spotlighted.`
- CTA button: `Start Application`
- Time estimate: `2–3 minutes`

**End screen copy**
- Title: `Thanks for applying!`
- Body: `We review every application within 5 business days. If approved, you will receive your creator kit and next steps.`

---

## 2) Section Flow (Lovable-style)

### Section A — About You
- `Full name` (Short answer) → Notion `Name`
- `Email` (Email) → Notion `Email`
- `Country` (Dropdown) → Notion `Country`
- `Primary language` (Dropdown, default English) → Notion `Language`

### Section B — Your Channel
- `Primary platform` (Dropdown: YouTube, TikTok, X, Instagram, Other) → Notion `Primary Platform`
- `Channel URL` (URL) → Notion `Channel URL`
- `Portfolio URL` (URL) → Notion `Portfolio URL`
- `Audience size` (Number) → Notion `Audience Size`
- `Average views on last 5 posts` (Number) → Notion `Avg Views (last 5)`
- `Example content link` (URL) → Notion `Content Examples`

### Section C — Build In Public (Project Fit)
- `Describe a project you would build with meshy.ai` (Long answer) → Notion `Project Idea`
- `Which workflows do you cover?` (Checkboxes: Blender, Unreal, Unity, 3D Printing, Game Assets, Concept Art, Other)
- `How would you document the build in public?` (Long answer)

### Section D — Program Intent
- `Why do you want to join the program?` (Long answer) → Notion `Why Meshy.ai`
- `How often do you publish content today?` (Multiple choice)
- `Can you commit to 4 pieces per month?` (Yes/No) → Notion `Content Commitment` (new checkbox)
- `I agree to share basic performance metrics` (Checkbox)

### Section E — Optional
- `How did you hear about meshy.ai?` (Multiple choice) → Notion `Acquisition Source` (optional)
- `Anything else we should know?` (Long answer) → Notion `Notes`

---

## 3) Logic Rules
- If `Primary platform = Other`, show `Which platform?` (Short answer)
- If `Audience size < 2000`, show `Tell us why your audience is a strong fit` (Long answer)
- If `Commit to 4 pieces per month = No`, show `What cadence can you commit to?` (Short answer)

---

## 4) Notion Integration Mapping
Connect to `Creator Applications` database and set defaults:
- `Status = Applied`
- `Language = English`
- `Program Fit Score = 0`

Field mapping should follow the labels above.

---

## 5) Legal/Compliance
Add a final small-text paragraph under the submit button:
`By submitting, you agree to the Terms of Use and Privacy Policy.`
Link the text to:
- https://www.meshy.ai/terms-of-use
- https://www.meshy.ai/privacy-policy

---

## 6) Recommended URL + Share Image
- Live form URL: `https://forms.fillout.com/t/e9o8WkxWoWus`
- Form URL slug: `meshy-creator-program`
- Social share image: use logo + tagline (placeholder ok for now)
