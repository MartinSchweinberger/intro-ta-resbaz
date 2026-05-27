# Introduction to Computational Text Analytics
## Research Bazaar Brisbane 2026

**Presenter:** Martin Schweinberger (LADAL, University of Queensland)  
**Workshop duration:** 2 hours  
**All materials:** [github.com/MartinSchweinberger/intro-ta-resbaz](https://github.com/MartinSchweinberger/intro-ta-resbaz)

---

## Workshop Description

This workshop introduces the fundamentals of computational text analysis. In the first part (45 min) we cover core concepts: what text analysis is, the text analysis pipeline, and three foundational methods — concordancing, collocation analysis, and keyword analysis. In the second part (60 min) participants work hands-on with the COOEE corpus (letters of early immigrants to Australia, 1788–1900) using either R/RStudio (Track A) or browser-based LADAL tools (Track B).

---

## How to Get These Materials

### Option 1: Download ZIP (recommended if you are not familiar with Git)
1. Click the green **Code** button above
2. Select **Download ZIP**
3. Unzip to your desktop
4. Open `intro-ta-resbaz.Rproj` in RStudio *(Track A only)*

### Option 2: Fork and Clone (recommended for R users who want their own copy)
1. Click **Fork** (top-right of this page)
2. On your fork, click **Code** → copy the URL
3. In your terminal:
   ```bash
   git clone https://github.com/YOUR-USERNAME/intro-ta-resbaz.git
   cd intro-ta-resbaz
   ```
4. Open `intro-ta-resbaz.Rproj` in RStudio

---

## Repository Structure

```
intro-ta-resbaz/
├── intro-ta-resbaz.Rproj       # RStudio project file — open this first
├── 01_intro_slides.qmd         # Part 1: presenter slides (RevealJS)
├── 02_r_notebook.qmd           # Part 2 Track A: R notebook with tasks
├── 03_tools_notebook.qmd       # Part 2 Track B: guided exercises (no R)
├── 04_speaker_guide.md         # Notes for the presenter
└── data/
    ├── COOEE/                  # Full COOEE corpus — one .txt per letter
    ├── COOEE_samples/          # 20-letter sample for Track B exercises
    ├── COOEE_metadata.xlsx     # Metadata: author, year, gender, origin, etc.
    └── BROWN/                  # BROWN corpus for keyword reference analysis
```

---

## Software Requirements (Track A)

- **R** ≥ 4.3 — [cran.r-project.org](https://cran.r-project.org)
- **RStudio** ≥ 2023.06 — [posit.co/downloads](https://posit.co/downloads/)
- **Quarto** ≥ 1.4 — [quarto.org](https://quarto.org) *(included with recent RStudio)*

R packages (install by running the first chunk in `02_r_notebook.qmd`):
`tidyverse`, `quanteda`, `quanteda.textstats`, `quanteda.textplots`, `readxl`, `here`, `igraph`, `ggraph`

---

## No R? Use the Browser Tools (Track B)

Track B uses free browser-based tools — no installation required.  
Go to **[ladal.edu.au/tools.html](https://ladal.edu.au/tools.html)**

> ⚠️ Shiny tools require an Australian/NZ university login (AAF/Tuakiri).  
> If you don't have AAF access, use the **Jupyter/MyBinder** alternatives on the same page — no login needed.

---

## The COOEE Corpus

COOEE = *Corpus of Oz Early English* — 319 letters written by immigrants to Australia, 1788–1900. The corpus captures colonial English in private correspondence and is ideal for studying historical language use, vocabulary change, and the concerns of early settlers.

**Metadata variables include:** author name, birth year, gender, origin, social status, year of writing, place of writing, addressee.

---

## Going Further: LADAL

All methods demonstrated in this workshop have full tutorials at **[ladal.edu.au](https://ladal.edu.au)**:

- [Introduction to Text Analysis: Concepts](https://ladal.edu.au/tutorials/text_analysis_intro/text_analysis_intro.html)
- [Introduction to Text Analysis: Practical](https://ladal.edu.au/tutorials/textanalysis/textanalysis.html)
- [Concordancing](https://ladal.edu.au/tutorials/concordancing/concordancing.html)
- [Collocation Analysis](https://ladal.edu.au/tutorials/collocations/collocations.html)
- [Keyword Analysis](https://ladal.edu.au/tutorials/keywords/keywords.html)

---

## Citation

Schweinberger, Martin. 2026. *Introduction to Computational Text Analytics: ResBaz Brisbane 2026 Workshop Materials*. LADAL, University of Queensland. github.com/MartinSchweinberger/intro-ta-resbaz

## License

Text and materials: CC BY 4.0  
Code: MIT  
COOEE corpus data: see original corpus documentation
