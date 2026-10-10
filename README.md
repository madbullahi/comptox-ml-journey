# Computational Toxicology & AMR Machine Learning — Learning Journey

A structured, public record of my path from Python foundations to machine learning for **computational toxicology** (New Approach Methodologies, QSAR, PFAS and persistent organic pollutants) and **antimicrobial resistance genomics**.

**Background:** BSc Microbiology · PhD Biosciences (toxicology, bioremediation of POPs, AMR pathogens) · Research Fellow, University of Birmingham

## Why this niche

- **Animal testing is being phased out.** The UK's *Replacing animals in science* strategy (Nov 2025) sets deadlines for replacing animal tests and backs AI-based alternatives. Regulators need validated, non-animal predictive models.
- **PFAS regulation.** The EU's proposed universal PFAS restriction covers thousands of substances that cannot all be tested in a lab.
- **AMR.** Whole-genome sequencing is now standard for AMR surveillance, and the WHO Global Action Plan on AMR runs to 2036.

## Progress

| Phase | Topic | Weeks | Status |
|---|---|---|---|
| 1 | Python & data foundations | 1–10 | 🟡 In progress |
| 2 | Core machine learning | 11–22 | ⚪ Not started |
| 3 | Cheminformatics | 23–32 | ⚪ Not started |
| 4 | Deep learning for chemistry | 33–42 | ⚪ Not started |
| 5 | Regulatory computational toxicology + PFAS capstone | 43–56 | ⚪ Not started |
| 6 | AMR genomics specialisation | 57–72 | ⚪ Not started |

Status key: ⚪ Not started · 🟡 In progress · ✅ Complete

The full week-by-week plan with checkboxes is in **[SYLLABUS.md](SYLLABUS.md)**.

## Projects

| # | Project | Phase | Link |
|---|---|---|---|
| 1 | Exploring POP toxicity data | 1 | *coming soon* |
| 2 | Predicting aquatic toxicity | 2 | *coming soon* |
| 3 | Tox21 multi-endpoint classifier | 3 | *coming soon* |
| 4 | Classical vs deep models for toxicity | 4 | *coming soon* |
| 5 | OECD-aligned PFAS screening model (capstone) | 5 | *coming soon* |
| 6 | AMR resistance prediction (capstone) | 6 | *coming soon* |

## Repository layout

```
├── SYLLABUS.md            # week-by-week plan with checkboxes
├── LEARNING_LOG.md        # weekly notes on what I learned
├── RESOURCES.md           # courses, datasets, papers
├── environment.yml        # conda environment for all projects
├── phase-1-foundations/
├── phase-2-core-ml/
├── phase-3-cheminformatics/
├── phase-4-deep-learning/
├── phase-5-regulatory-tox/
└── phase-6-amr-genomics/
```

## Setup

```bash
conda env create -f environment.yml
conda activate comptox
python -c "import rdkit, sklearn, torch; print('Ready')"
```

## Contact

Open an issue or get in touch if you work on NAMs, computational toxicology or AMR — I'm always glad to connect.
