---
output:
  html_document: default
---
# ResBaz Brisbane 2026 — Workshop Speaker Guide
## Introduction to Computational Text Analytics
### Delivered by: [Your Name]
### Materials: github.com/MartinSchweinberger/intro-ta-resbaz

---

## Overview

| Segment | Duration | File | Key Activities |
|---|---|---|---|
| Part 1: Concepts | 45 min | `01_intro_slides.qmd` | Presentation + Q&A |
| Break / Track Split | 5 min | — | Direct people to Track A or B |
| Part 2: Hands-on | 60 min | `02_r_notebook.qmd` (Track A) / `03_tools_notebook.qmd` (Track B) | Guided tasks |
| Wrap-up | 5 min | — | Reflection, LADAL pointer |

**Total: ~2 hours** (flexible — Part 2 can run short if setup takes longer)

---

## Before the Workshop

### Room setup
- Projector connected and tested with slides open
- Your laptop has R ≥ 4.3 and RStudio installed
- You have run the demo notebook (`02_r_notebook.qmd`) end-to-end at least once before the day
- The GitHub repo is public and all data is in place

### Test the LADAL tools (day before)
Launch each Shiny tool once to confirm they load. Shiny tools on ARDC BinderHub require 1–3 minutes to spin up. If any tool is down, note the Jupyter/MyBinder alternative at ladal.edu.au/tools.html — these do not require AAF login.

### Print or share the handout link
Participants need: **github.com/MartinSchweinberger/intro-ta-resbaz**  
Write this on the whiteboard before people arrive.

---

## Part 1: Concepts and Foundations (45 min)

### Slide-by-slide notes

**Slide 1 (Opening questions)**  
Open with the three questions from the abstract. Pause after each one. Ask for a show of hands: "How many of you have more text than you can comfortably analyse manually?" This grounds the workshop in real need.

**Slide 2 (Today's Plan)**  
Briefly orient people. Emphasise that *both tracks* cover the same intellectual content — Track B is not a lesser option, it is a different tool path.

**Slides 3–5 (What is TA, Four Fields, Why Now)**  
Keep these brisk — 8 minutes total. The key point to land: we are using computers to assist human interpretation, not replace it. The "Computational methods produce patterns; researchers produce meaning" line is worth saying out loud and letting sit.

**Slides 6–7 (Pipeline)**  
The pipeline diagram is the structural backbone of the session. Take 5 minutes here. Emphasise that today covers stages 3 (pre-processing / cleaning) and 5 (three methods). Everything else in the pipeline is in the LADAL tutorials.

**Slide 8 (Start with a question)**  
This is a genuine intellectual point, not just housekeeping. Spend 2 minutes. Ask: "Has anyone ever run an analysis and then wondered what it meant?" Common experience. The lesson: method choice follows the question.

**Slides 9–10 (Corpus, Pre-processing)**  
Introduce COOEE briefly here. One sentence of context: 319 letters, immigrants to Australia, 1788–1900, metadata includes author gender, origin, year. This makes the data feel real before attendees touch it.

**Slides 11–13 (Three methods)**  
Each method gets one slide. Don't rush — these are the conceptual payoff of Part 1. For collocations, the key conceptual move is: *not just co-occurrence, but co-occurrence above chance*. For keywords: *not most frequent, but most distinctive compared to a reference.*

**Slides 14–15 (Terminology)**  
The types/tokens/lemmas slide is worth 3 minutes. Use the example sentence. Ask the room: "How many tokens? How many types?" Let them answer before revealing. It makes the concept stick.

**Slide 16 (LADAL)**  
Spend 3 minutes. This is the long-term resource pointer. LADAL is where they go after today to go deeper. Mention it has 60+ tutorials from beginner to BERT and local LLMs.

**Slide 17 (Questions)**  
Take genuine questions. 5 minutes maximum. If a question is deep, offer to discuss in the break or after the session.

**Slide 18 (Part 2 Overview)**  
This is the track-split slide. Direct people clearly: "If you use R and are comfortable in RStudio, go to Track A. If you don't use R or prefer not to code today, go to Track B. Both are equally valid."

---

### Timing check
| Point | Elapsed |
|---|---|
| Opening questions | 0:00 |
| Four Fields + Why Now | 0:08 |
| Pipeline overview | 0:16 |
| Three Methods | 0:26 |
| Terminology | 0:36 |
| LADAL + Q&A | 0:40 |
| Part 2 intro + track split | 0:44 |

---

## Break / Track Split (5 min)

Say clearly:

> "Track A — you need RStudio open and the repo downloaded. If you haven't done that yet, now is the time. Go to github.com/MartinSchweinberger/intro-ta-resbaz, click Code → Download ZIP, unzip it, and open the `.Rproj` file in RStudio."

> "Track B — open a browser. Go to ladal.edu.au/tools.html. I'll walk you through launching the TextCleaner in just a moment."

If the room allows it, ask Track A and Track B participants to sit in separate halves of the room so you can circulate efficiently.

---

## Part 2: Hands-on (60 min)

### Live Demo for Track A (first 15 min)

**What you are demonstrating:**

1. The project structure (show the repo folder in RStudio's Files pane: `data/`, `02_r_notebook.qmd`, `.Rproj`)
2. Open `02_r_notebook.qmd` and run it chunk by chunk, narrating each step
3. Focus your narration on the *pipe logic* — each `|>` step transforms the data in one readable move. Say something like: "We can read this left-to-right: take the text, then remove tags, then collapse whitespace, then trim. Each step does one thing."
4. Run the concordance for "land" — show the KWIC output
5. Run the collocation analysis — show the table
6. Run the network plot — this is the visual payoff, let it sit for a moment
7. Run the keyword analysis — show the keyness plot

**What to emphasise:**
- Every step is documented and reproducible
- They can swap "land" for any other word
- The LADAL tutorial has more depth on each method

**After the demo (~15 min in):** say "Now work through the notebook at your own pace. Tasks 1–5 are marked with 🔧. Task 1 is on cleaning, Tasks 2–3 on concordancing, Task 4–5 on keywords."

### Facilitating Track B (simultaneous with Track A demo)

If there is a co-facilitator: they run Track B from the start of Part 2.  
If you are alone: briefly orient Track B participants before starting the Track A demo.

Say: "Track B — open the tools notebook (`03_tools_notebook.qmd` rendered as HTML, or just read it from your screen). Start with Exercise 1: launch TextCleaner, upload the sample files from `data/COOEE_samples/`, and work through the questions. I'll come check in with you shortly."

The Track B notebook is designed to be self-guiding. Most participants can work independently. Check in every 15 minutes.

### Timing for Part 2

| Point | Elapsed from Part 2 start |
|---|---|
| Live demo (Track A) / TextCleaner intro (Track B) | 0:00–0:15 |
| Track A: Tasks 1–3 (cleaning + concordancing) | 0:15–0:35 |
| Track B: Exercises 1–3 (cleaning + concordancing) | 0:15–0:35 |
| Track A: Tasks 4–5 (keywords + diachronic) | 0:35–0:55 |
| Track B: Exercises 4–6 (collocations + keywords) | 0:35–0:55 |
| Wrap-up + reflection | 0:55–1:00 |

---

## Wrap-up (5 min)

Bring both tracks together. Ask 2–3 people to share:

> "What is one thing you found in the data that surprised you or sparked a question?"

Then say:

> "Everything we've done today is the foundation. Concordancing, collocations, and keywords are the core of corpus-based text analysis. LADAL has deep-dive tutorials for each of these, plus sentiment analysis, topic modelling, POS tagging, network analysis, and all the way up to transformer models. All free, all open access, all citable. Start at ladal.edu.au."

Close with the GitHub repo URL and the LADAL URL on screen.

---

## Common Problems and How to Handle Them

### Track A: Git/GitHub issues
- **Can't clone the repo:** Skip git — just download the ZIP (Code → Download ZIP). The `.Rproj` file still works.
- **Package installation fails:** The most common cause is a corporate proxy or firewall. If `install.packages()` fails, try setting a mirror: `options(repos = c(CRAN = "https://cloud.r-project.org"))`. If it still fails, ask them to work from a pre-rendered HTML version of the notebook.
- **`here()` returns the wrong path:** Check that they opened the `.Rproj` file (not just the `.qmd` file directly). The `.Rproj` sets the working directory.
- **`map_chr` reads empty files:** Some `.txt` files may have encoding issues. Add `\(f) read_file(f, locale = locale(encoding = "latin1"))` as a fallback.

### Track A: Collocation network is empty
This means `lambda > 3` matched no collocations — possible if the corpus is small. Reduce the threshold: `filter(lambda > 1)`.

### Track B: Shiny tool won't load
- Check AAF login — the institution must be AAF/Tuakiri registered
- If login fails, go to ladal.edu.au/tools.html and use the Jupyter/MyBinder versions
- MyBinder takes 2–3 minutes to start — tell participants to click Launch and do something else while it loads

### Track B: "I don't have enough hits"
The sample corpus is small (~20 letters). For low-frequency words, recommend searching with a wildcard (e.g., `home*`) or using a broader term. Alternatively, participants can upload additional COOEE files from the full dataset in `data/COOEE/`.

---

## Repo Structure (for your reference)

```
intro-ta-resbaz/
├── intro-ta-resbaz.Rproj       # open this in RStudio
├── 01_intro_slides.qmd         # Part 1 presenter slides
├── 02_r_notebook.qmd           # Part 2 Track A (R users)
├── 03_tools_notebook.qmd       # Part 2 Track B (no R)
├── 04_speaker_guide.md         # this file
└── data/
    ├── COOEE/                  # full COOEE corpus (.txt files)
    ├── COOEE_samples/          # ~20 letters for Track B exercises
    ├── COOEE_metadata.xlsx     # COOEE metadata spreadsheet
    └── BROWN/                  # BROWN corpus (.txt files)
```

---

## Key URLs (keep these on a sticky note)

| Resource | URL |
|---|---|
| Workshop repo | github.com/MartinSchweinberger/intro-ta-resbaz |
| LADAL home | ladal.edu.au |
| LADAL tools | ladal.edu.au/tools.html |
| LADAL text analytics tutorials | ladal.edu.au/tutorials.html#text-analytics |
| Concordancing tutorial | ladal.edu.au/tutorials/concordancing/concordancing.html |
| Collocations tutorial | ladal.edu.au/tutorials/collocations/collocations.html |
| Keywords tutorial | ladal.edu.au/tutorials/keywords/keywords.html |
| Martin Schweinberger (LADAL) | m.schweinberger@uq.edu.au |
