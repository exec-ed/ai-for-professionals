# Folder Structure — AI for Professionals

## Organisation

### `participant-materials/` — Participant-Facing Content
**Purpose:** Everything participants see and use during and after the workshop.

**Markdown Files (converted to HTML by build script):**
- frameworks-reference-sheet.md — All 4 frameworks on one reference sheet
- personal-action-plan-template.md — Week/month/quarter planning worksheet

**Why here:** Single source of truth for all participant materials. Build script processes this folder.

---

### `activities/` — Exercise Materials (Instructor Use)
**Purpose:** Exercise instructions, worksheets, and data files used during the workshop.

**Files:**
- prompt-engineering-worksheet.md — 6 workplace scenarios for Exercise 2
- retailflow-customer-service-data.csv — 260-row dataset for Exercise 3
- data-analysis-worksheet.md — Guided analysis worksheet for Exercise 3
- workflow-mapping-template.md — Before/after workflow redesign for Exercise 4

**Why here:** Instructors distribute these during the workshop (print or digital). NOT published to the participant-facing website — distributed directly.

---

### `instructor-materials/` — Facilitator Guides
**Purpose:** Complete delivery instructions, teaching notes, answer keys.

**Files:**
- FACILITATOR-START-HERE.md — Master delivery guide (read first)
- exercise-1-facilitator-guide.md — AI Tool Test Drive facilitation
- exercise-2-facilitator-guide.md — Prompt Engineering Workshop facilitation
- exercise-3-facilitator-guide.md — Data Analysis Challenge facilitation
- exercise-4-facilitator-guide.md — AI-Enhanced Workflow facilitation
- answer-keys.md — Sample outputs and calibration for all exercises

**Why here:** Facilitator preparation and delivery support. Converted to password-protected HTML in the instructor portal.

---

### `pre-readings/` — Required Pre-Course Reading
**Purpose:** Material participants must read before the workshop.

**Files:**
- ai-for-the-rest-of-us.md — 20-minute reading covering AI basics, strengths, weaknesses, and account setup

**Why separate:** Emphasises this is a PRE-course requirement, not a day-of material.

**Build:** Converted to HTML and accessible from the materials page.

---

### `content/` — Slide Deck and Images
**Purpose:** Presentation materials for the facilitator.

**Structure:**
- slide-deck.md — 27 slides in Pandoc/Quarto markdown format
- images/ — Slide images (PNG files)
- images/IMAGE-SPECS.md — Specifications for generating each image

**Why here:** Slides are a separate deliverable from the web materials. Rendered with Quarto or Pandoc into HTML/PPTX/PDF.

---

### `docs/` — GitHub Pages Output (GENERATED)
**Purpose:** Built website served on GitHub Pages.

**Structure:**
- *.html — Participant material pages (generated from markdown)
- instructor/ — Password-protected instructor pages
- css/ — Stylesheets (copied from build/templates/)
- js/ — JavaScript (copied from build/templates/)
- images/ — Slide and content images

**DO NOT edit generated files directly — edit source files and rebuild.**

---

### `build/` — Build System
**Purpose:** Convert markdown to HTML and deploy to docs/.

**Structure:**
- scripts/build.sh — Main build script
- templates/ — Pandoc HTML templates + CSS/JS
  - material-page.html — Template for participant pages
  - instructor-page.html — Template for password-protected pages
  - materials.css — Stylesheet for material pages
  - shared.css — Shared stylesheet for all pages
  - auth.js — Password protection for instructor portal

---

## What Gets Published

### Via GitHub Pages (docs/ folder):
- Pre-reading (1 md → html)
- Reference materials (2 md → html)
- Instructor portal (6 md → password-protected html)

### NOT Published (instructor-only):
- activities/ folder (exercise worksheets, CSV data)
- instructor-materials/ source markdown
- build/ folder (build system)
- content/ folder (slide deck source)

---

## File Type Guide

### Markdown (.md) Files
**Purpose:** Source files that get converted to HTML.
**Located in:** participant-materials/, pre-readings/, instructor-materials/, activities/
**Action:** Edit these, then run build script to regenerate HTML.

### CSV Files
**Purpose:** Exercise data distributed directly to participants.
**Located in:** activities/
**Action:** Distribute via email, shared drive, or USB during the workshop.

### Static HTML (.html) Files
**Purpose:** Hand-written pages (index, materials hub).
**Located in:** docs/ only
**Action:** Edit directly in docs/ (not generated).

---

## Rules for Adding New Materials

### To add a new participant material:
1. Create .md file in `participant-materials/`
2. Add filename to FILES array in `build/scripts/build.sh`
3. Run `bash build/scripts/build.sh`
4. Add link to materials.html

### To add a new instructor material:
1. Create .md file in `instructor-materials/`
2. Add filename to INSTRUCTOR_FILES array in `build/scripts/build.sh`
3. Run build script
4. Update instructor index in build.sh if needed

### To update the website:
1. Edit source files (not docs/ generated files)
2. Run `bash build/scripts/build.sh`
3. Test locally: `cd docs && python3 -m http.server 8000`
4. Commit and push
5. GitHub Pages auto-deploys
