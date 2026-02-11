# Inbound Creator Pipeline (Example: Meshy)

A practical inbound creator pipeline built for growth marketers. This repo uses **Meshy** as the example program, but the framework is reusable for any product that relies on creator-led growth.

## What this project is
A ready-to-ship pipeline for:
- Attracting creator applications (landing page + application form)
- Qualifying and segmenting creators (Notion database schema)
- Managing ongoing content + performance tracking

This is designed for **inbound** applications (creators apply to you), not outbound outreach.

## What’s included
- **Landing page** for the creator program
- **Notion database setup** (applications, creators, deliverables, ops)
- **Fillout form spec** with logic + Notion mappings

## Repository structure
- `landing/` → static landing page (HTML/CSS/JS)
- `notion/` → Notion setup guide
- `fillout/` → Fillout form spec

## Quick start
1. **Customize the landing page**
   - Update copy, CTA, and brand elements in `landing/index.html`.
   - Ensure the CTA points to your Fillout form URL.

2. **Create the Notion databases**
   - Follow `notion/CREATOR_PROGRAM_NOTION_SETUP.md`.
   - Add the properties, relations, rollups, and views as described.

3. **Build the Fillout form**
   - Follow `fillout/CREATOR_APPLICATION_FORM.md`.
   - Connect it to your Notion “Creator Applications” database.

4. **Publish the landing page**
   - Host via GitHub Pages, Vercel, Netlify, or your site builder.

## Example program assumptions (Meshy)
- Primary platform: YouTube
- Primary tier: 10k–150k subscribers
- Content cadence: 4 pieces/month
- Incentives: credits, 10% rev share (first 6 payments), paid collabs, spotlight

## Success metrics to track
- Application volume
- Qualification rate
- Activation rate (first post within 14 days)
- Content cadence adherence
- Conversions and revenue per creator

## How to adapt for your product
- Swap program name and value proposition in the landing page.
- Update the incentives and tier definitions to match your budget.
- Adjust the application fields to reflect your creator criteria.

---

If you want help tailoring this to your product, share your target creator niche, incentives, and platform focus.
