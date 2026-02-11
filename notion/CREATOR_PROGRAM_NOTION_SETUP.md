# Meshy Makers - Notion Setup

This setup uses four databases. Create each database first, then add relations and rollups.

## 1) Database: Creator Applications
**Purpose:** inbound intake and qualification.

**Properties**
- `Name` (Title)
- `Application Date` (Date)
- `Primary Platform` (Select: YouTube, TikTok, X, Instagram, Other)
- `Channel URL` (URL)
- `Portfolio URL` (URL)
- `Email` (Email)
- `Country` (Select)
- `Language` (Select, default: English)
- `Audience Size` (Number)
- `Avg Views (last 5)` (Number)
- `Content Examples` (URL)
- `Project Idea` (Text)
- `Why Meshy` (Text)
- `Program Fit Score` (Number, 0–100)
- `Tier Recommendation` (Select: Builder, Creator, Partner)
- `Status` (Select: Applied, Qualified, Accepted, Active, Rejected)
- `Assigned Reviewer` (Person)
- `Notes` (Text)
- `Creator Record` (Relation → Creators)

**Views**
- `Applications (Table)`
- `Pipeline (Board)` grouped by `Status`
- `High Score (Table)` filter `Program Fit Score >= 70`

---

## 2) Database: Creators
**Purpose:** active creator profile and program status.

**Properties**
- `Name` (Title)
- `Tier` (Select: Builder, Creator, Partner)
- `Primary Platform` (Select)
- `Channel URL` (URL)
- `Email` (Email)
- `Affiliate Code` (Text)
- `Credits Allocated` (Number)
- `Paid Collab Eligible` (Checkbox)
- `Monthly Content Target` (Number, default 4)
- `Last Published` (Date)
- `Status` (Select: Active, Paused, Offboarded)
- `Applications` (Relation → Creator Applications)
- `Deliverables` (Relation → Content Deliverables)
- `Ops Tracker` (Relation → Program Ops)

**Rollups**
- `Published This Month` (Rollup on Deliverables → `Published Link` count filtered this month)
- `Total Views` (Rollup on Deliverables → `Views` sum)
- `Total Signups` (Rollup on Deliverables → `Signups` sum)

**Views**
- `Active Creators (Table)` filter `Status = Active`
- `Tier Board` grouped by `Tier`

---

## 3) Database: Content Deliverables
**Purpose:** track each content piece and performance.

**Properties**
- `Title` (Title)
- `Creator` (Relation → Creators)
- `Platform` (Select)
- `Content Type` (Select: Short, Long, Showcase)
- `Topic` (Text)
- `Due Date` (Date)
- `Published Link` (URL)
- `Published Date` (Date)
- `Views` (Number)
- `Clicks` (Number)
- `Signups` (Number)
- `Revenue` (Number)
- `Status` (Select: Planned, In Production, Published, On Hold)

**Views**
- `Content Calendar` (Calendar by `Due Date`)
- `Published` (Table filter `Status = Published`)

---

## 4) Database: Program Ops
**Purpose:** operational checklist and compliance.

**Properties**
- `Title` (Title)
- `Creator` (Relation → Creators)
- `Kit Sent` (Checkbox)
- `Trial Credits Sent` (Checkbox)
- `Affiliate Link Issued` (Checkbox)
- `First Post Date` (Date)
- `Activation Target` (Date)
- `Feedback Sent` (Checkbox)
- `Next Action` (Text)
- `Owner` (Person)

**Views**
- `Activation Watch` filter `First Post Date is empty`
- `Ops Checklist` (Table)

---

## Optional: Templates
Create templates in the `Creators` database:
- `New Builder` template: sets Tier = Builder, Monthly Content Target = 4, Status = Active.
- `New Creator` template: sets Tier = Creator, Monthly Content Target = 4, Status = Active.

---

## Recommended Workflow
1. Fillout form submits to `Creator Applications`.
2. Reviewer scores and assigns tier.
3. On acceptance, create a `Creator` record and link it via `Creator Record`.
4. Create 4 `Content Deliverables` per month per creator.
5. Track performance in deliverables and review monthly.
