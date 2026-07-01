---
name: study-guide-universal
description: Build fully structured, goal-oriented study plans and project roadmaps for any user. Use this skill whenever someone asks for a study plan, prep schedule, roadmap, learning guide, or wants to prepare for any exam, competition, project, or skill-building goal. Trigger on phrases like "make me a study plan", "help me prep for", "build me a schedule for", "how do I learn X", "I want to get better at", "I have Y weeks to learn Z", or any request to structure a learning or project goal over time. Always interview the user before building — do not skip the intake questions. Produces a complete, downloadable interactive HTML file every time.
---

# Universal Study Guide Skill

## Purpose
Build anyone a fully structured, interactive study plan or project roadmap as a downloadable HTML file. Always ask questions first. Never assume context.

---

## Step 1 — Run the intake interview

Ask all questions using clickable prompts where possible (ask_user_input_v0). Do not ask more than 3 questions at once. Split into two rounds.

### Round 1 — The goal

Ask these three together:

**Q1: What type of guide do you need?**
- Exam or competition prep (SAT, AMC, AP, etc.)
- School subject (math, science, history, language, etc.)
- Skill building (coding, video editing, music, art, sport, etc.)
- Project roadmap (business, app, creative project, etc.)
- Something else

**Q2: What's the specific goal?**
(Free text — what are they trying to achieve or reach?)

**Q3: When is the deadline or target date?**
- Less than 2 weeks
- 2–4 weeks
- 1–3 months
- 3–6 months
- 6+ months / ongoing

### Round 2 — The setup

After Round 1, ask these:

**Q4: How much time can you realistically study per week?**
- Less than 2 hours
- 2–4 hours
- 4–6 hours
- 6–10 hours
- 10+ hours

**Q5: What's your current level with this subject?**
- Complete beginner (never studied this)
- Some exposure (learned basics but inconsistent)
- Intermediate (know fundamentals, want to go deeper)
- Advanced (strong foundation, want to optimize)

**Q6: Have you taken a practice test or diagnostic?**
- Yes — I know my weak areas
- No — starting cold
- Not applicable

If yes: ask them to describe the results briefly (free text, not clickable).

**Q7: What's your preferred theme?**

Dark:
- Midnight (dark navy, orange accents)
- Obsidian (pure black, high contrast)
- Hacker (dark green on black)

Light:
- Clean (white, blue accents)
- Paper (warm off-white, ink tones)
- Academic (cream, red accents)

---

## Step 2 — Confirm the plan structure

Before building, state back to the user in 3–5 bullet points:
- The goal
- The timeline
- How many sessions per week
- The main topics or milestones you'll cover
- The output format

Then ask: "Does this look right, or anything you'd change?"

Wait for confirmation before building.

---

## Step 3 — Build the HTML file

Build the complete file. No outlines, no drafts, no "here's what I'll make." The finished, working file.

### Required HTML features

- Week/unit selector dropdown with prev/next navigation
- Progress bar showing position in plan
- Per-session step-by-step breakdown with time badges on every step (e.g. "10m")
- Built-in timer button per session using cuckoo.team — pre-filled with total session time
- Direct resource links (specific pages, not homepages)
- Score or skill targets per week anchored to the baseline they described
- "If short on time" fallback note on every week
- Biweekly review chips on every week showing what to revisit
- Intake summary panel on Week 1 (their goal, deadline, current level, weak areas)

---

## Themes — CSS variables

Apply via :root. Never hardcode colors.

**Midnight**
```css
--bg:#0f1117; --surface:#1a1d27; --surface2:#22263a;
--border:rgba(255,255,255,0.08); --border-strong:rgba(255,255,255,0.15);
--text:#e8eaf0; --muted:#7a7f99;
--accent:#f5a623; --accent2:#4a9eff; --accent3:#36d399;
```

**Obsidian**
```css
--bg:#000000; --surface:#111111; --surface2:#1a1a1a;
--border:rgba(255,255,255,0.1); --border-strong:rgba(255,255,255,0.2);
--text:#f0f0f0; --muted:#666666;
--accent:#ff6b2b; --accent2:#4a9eff; --accent3:#36d399;
```

**Hacker**
```css
--bg:#0a0f0a; --surface:#0f1a0f; --surface2:#162516;
--border:rgba(0,255,65,0.12); --border-strong:rgba(0,255,65,0.25);
--text:#c8ffc8; --muted:#4a8a4a;
--accent:#00ff41; --accent2:#00d4ff; --accent3:#ffff00;
```

**Clean**
```css
--bg:#f8f9fa; --surface:#ffffff; --surface2:#f0f2f5;
--border:rgba(0,0,0,0.08); --border-strong:rgba(0,0,0,0.15);
--text:#1a1d27; --muted:#6b7280;
--accent:#2563eb; --accent2:#7c3aed; --accent3:#059669;
```

**Paper**
```css
--bg:#f5f0e8; --surface:#faf7f2; --surface2:#ede8df;
--border:rgba(0,0,0,0.1); --border-strong:rgba(0,0,0,0.18);
--text:#1c1917; --muted:#78716c;
--accent:#b45309; --accent2:#1d4ed8; --accent3:#15803d;
```

**Academic**
```css
--bg:#fdf8f0; --surface:#ffffff; --surface2:#f5ede0;
--border:rgba(0,0,0,0.1); --border-strong:rgba(0,0,0,0.2);
--text:#1a1209; --muted:#6b5c45;
--accent:#c0392b; --accent2:#2c3e7a; --accent3:#196f3d;
```

---

## Session structures by guide type

### Exam / Competition prep
1. Concept review — direct wiki/resource link — 8–12 min
2. Worked example — read a fully solved problem — 8–10 min
3. Practice problems — 4–6 targeted problems — 20–25 min
4. Error log — write topic + exact insight missed — 8 min
5. Biweekly review (even weeks) — redo 2 old error log problems — 5–7 min

### School subject
1. Read + take notes on the concept — 12–15 min
2. Answer 3–5 practice questions from the textbook/resource — 20 min
3. Self-quiz: close notes, write what you remember — 10 min
4. Error log — what did the quiz show you didn't know yet? — 8 min

### Skill building (coding, video, art, music, etc.)
1. Study a technique — watch, read, or analyze an example — 10–15 min
2. Apply it — build, shoot, edit, practice — 25–30 min
3. Review your own work — what worked, what didn't, log it — 8–10 min

### Project roadmap
Use milestone structure instead of sessions:
- Each week = one milestone with: goal, deliverables, success criteria
- Each milestone has a "what failure looks like" note
- Include a "if behind" recovery path for each milestone

---

## Content standards

### What makes a step good
- Title is an action verb ("Solve 4 problems" not "Practice problems")
- Description is specific — what exactly to do, not vaguely what to think about
- Time badge on every step
- Link is direct to the specific resource page

### Score/skill targets
Always tie to what the user told you in the intake:
- If they gave a diagnostic score, use it as the baseline
- If they're starting cold, use qualitative targets ("able to solve X type of problem without hints")
- Express progress as concrete milestones, not vague improvement

### Spaced repetition
Every even-numbered week: one session includes a 5–7 min step to redo 2 problems or exercises from the error log 2 weeks prior. Include this on every plan regardless of subject.

---

## Quality checklist

Before calling present_files, verify:
- [ ] Intake summary panel on Week/Unit 1
- [ ] Every step has a visible time badge
- [ ] Every resource reference has a direct link
- [ ] Every session has a cuckoo.team timer button
- [ ] Score/skill targets reference the user's actual baseline
- [ ] Biweekly review chips on every week
- [ ] "If short on time" note on every week
- [ ] Theme applied via CSS variables
- [ ] Prev/next navigation functional
- [ ] File renders correctly offline with no external dependencies
