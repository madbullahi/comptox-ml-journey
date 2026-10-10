# Syllabus: Computational Toxicology & AMR Machine Learning

A self-paced, 72-week path from Python foundations to publishable work in computational toxicology, with an AMR genomics specialisation.

**Pace:** about 6–8 hours a week. Weeks are a guide, not a deadline. If a week takes two, that's fine.
**Hardware:** everything up to Phase 5 runs on a ThinkPad L390 (CPU). Use Google Colab, Kaggle or BlueBEAR for the GPU and large-genome work in Phases 3 and 6.

**How to use this file:** tick a box (`- [x]`) when you finish a task, commit, and push. Your GitHub history becomes your progress record.

---

## Phase 1 — Python and data foundations (Weeks 1–10)

**Goal:** be comfortable loading, cleaning, analysing and plotting real scientific data.

### Weeks 1–2: Python core
- [ ] Variables, types, lists, dictionaries, tuples
- [ ] Functions, default arguments, return values, scope
- [ ] Loops, conditionals, list comprehensions
- [ ] Reading and writing files (`open`, `csv`)
- [ ] Practice: 20 exercises on Kaggle Learn "Python" course

### Weeks 3–4: NumPy
- [ ] Arrays, shapes, indexing, slicing
- [ ] Vectorised maths and broadcasting
- [ ] Random numbers and reproducibility (`np.random.default_rng(seed)`)
- [ ] Practice: compute dose–response statistics from a small array of LC50 values

### Weeks 5–6: pandas
- [ ] DataFrames, selecting, filtering, sorting
- [ ] Missing data, merging, groupby
- [ ] Practice: load an EPA CompTox Dashboard export and summarise by chemical class

### Weeks 7–8: Visualisation
- [ ] matplotlib and seaborn: scatter, histogram, box, heatmap
- [ ] Making publication-quality figures (labels, units, colour-blind palettes)
- [ ] Practice: visualise toxicity distribution across chemical classes

### Weeks 9–10: Git, GitHub and good habits
- [ ] Git basics: `add`, `commit`, `push`, `.gitignore`, branches
- [ ] Writing a good README
- [ ] Organising a project (data / notebooks / src / results)
- [ ] **Milestone project 1:** *Exploring POP toxicity data* — clean and analyse a public toxicity dataset for persistent organic pollutants and present it in `phase-1-foundations/`

### Maths alongside Phase 1 (about 1 hour a week)
- [ ] Linear algebra: vectors, matrices, dot products (3Blue1Brown *Essence of Linear Algebra*)
- [ ] Probability: distributions, conditional probability, Bayes
- [ ] Statistics refresher: hypothesis tests, confidence intervals, correlation

---

## Phase 2 — Core machine learning (Weeks 11–22)

**Goal:** build, evaluate and honestly report ML models.

### Weeks 11–12: The ML workflow
- [ ] Supervised vs unsupervised learning
- [ ] Train/test split, why data leakage happens
- [ ] Linear and logistic regression

### Weeks 13–14: Tree-based models
- [ ] Decision trees, random forests, gradient boosting (XGBoost / LightGBM)
- [ ] Hyperparameters and grid/random search

### Weeks 15–16: Evaluation done properly
- [ ] Cross-validation, stratification
- [ ] Classification metrics: ROC-AUC, precision, recall, F1, balanced accuracy, MCC
- [ ] Imbalanced data (very common in tox and AMR)
- [ ] Regression metrics: RMSE, MAE, R²

### Weeks 17–18: Interpretability
- [ ] Feature importance and its pitfalls
- [ ] SHAP values
- [ ] Practice: explain which features drive a toxicity classifier

### Weeks 19–20: Unsupervised learning
- [ ] PCA, t-SNE/UMAP for visualising chemical space
- [ ] Clustering (k-means, hierarchical)

### Weeks 21–22: Milestone
- [ ] **Milestone project 2:** *Predicting aquatic toxicity* — build and compare three models on a public aquatic toxicity dataset, with cross-validation, SHAP and an honest limitations section

**Resources:** Andrew Ng's Machine Learning Specialization (audit free), scikit-learn user guide, *Hands-On Machine Learning* (Géron), chapters 1–7.

---

## Phase 3 — Cheminformatics (Weeks 23–32)

**Goal:** represent chemicals so that machines can learn from them.

### Weeks 23–24: Molecules as data
- [ ] SMILES, InChI, InChIKey
- [ ] Install and use RDKit: parse molecules, draw structures, standardise
- [ ] Practice: draw and standardise 20 POPs (PCBs, dioxins, PBDEs, PFAS)

### Weeks 25–26: Molecular descriptors and fingerprints
- [ ] Physicochemical descriptors (logP, MW, TPSA, H-bond donors/acceptors)
- [ ] Morgan (ECFP) fingerprints, MACCS keys
- [ ] Molecular similarity (Tanimoto)

### Weeks 27–28: Chemical data sources
- [ ] PubChem and ChEMBL via their APIs
- [ ] EPA CompTox Chemicals Dashboard and ToxCast
- [ ] Tox21 (via MoleculeNet / DeepChem)
- [ ] Data curation: duplicates, salts, mixtures, inorganics, conflicting labels

### Weeks 29–30: Chemical space and splits
- [ ] Visualising chemical space (PCA/UMAP on fingerprints)
- [ ] Why random splits overestimate performance; scaffold and cluster splits
- [ ] Practice: compare random vs scaffold split performance on the same model

### Weeks 31–32: Milestone
- [ ] **Milestone project 3:** *A Tox21 multi-endpoint classifier* — fingerprint-based models for several Tox21 assays, with scaffold splits and per-endpoint reporting

**Resources:** TeachOpenCADD tutorials, RDKit "Getting Started in Python" docs, Pat Walters' *Practical Cheminformatics* blog.

---

## Phase 4 — Deep learning for chemistry (Weeks 33–42)

**Goal:** understand when neural networks help, and when they don't.

### Weeks 33–35: Neural network fundamentals
- [ ] Perceptrons, activations, backpropagation, optimisers
- [ ] PyTorch tensors, `nn.Module`, training loops
- [ ] Overfitting, dropout, early stopping
- [ ] fast.ai *Practical Deep Learning* lessons 1–4

### Weeks 36–38: Graph neural networks
- [ ] Molecules as graphs (atoms = nodes, bonds = edges)
- [ ] Message passing; GCN and MPNN concepts
- [ ] Chemprop or DeepChem on Colab
- [ ] Practice: GNN vs random forest on the same Tox21 endpoint — which wins, and why?

### Weeks 39–40: Pre-trained chemical models
- [ ] Chemical language models and embeddings (concepts)
- [ ] Using pre-trained embeddings as features
- [ ] Uncertainty estimation (ensembles)

### Weeks 41–42: Milestone
- [ ] **Milestone project 4:** *Classical vs deep models for toxicity* — a fair benchmark with scaffold splits, uncertainty and a clear verdict

---

## Phase 5 — Regulatory computational toxicology (Weeks 43–56)

**Goal:** build models a regulator could trust. This is where your toxicology expertise becomes your advantage.

### Weeks 43–44: The regulatory landscape
- [ ] New Approach Methodologies (NAMs): definitions and examples
- [ ] UK *Replacing animals in science* strategy (Nov 2025) and MHRA NAMs guidance
- [ ] REACH, the EU PFAS restriction process, and UK REACH
- [ ] Integrated Approaches to Testing and Assessment (IATA)

### Weeks 45–46: OECD QSAR validation principles
- [ ] The 5 OECD principles: defined endpoint, unambiguous algorithm, applicability domain, goodness-of-fit/robustness/predictivity, mechanistic interpretation
- [ ] QSAR Model Reporting Format (QMRF)
- [ ] Practice: write a QMRF-style report for your Phase 3 model

### Weeks 47–48: Applicability domain
- [ ] Distance-, leverage- and density-based applicability domain methods
- [ ] Flagging predictions that fall outside the domain
- [ ] Practice: add an applicability-domain check to your model

### Weeks 49–50: Adverse Outcome Pathways
- [ ] AOP framework: molecular initiating event → key events → adverse outcome
- [ ] AOP-Wiki; linking ToxCast assays to key events
- [ ] Read-across and grouping (concepts, OECD QSAR Toolbox overview)

### Weeks 51–52: Environmental fate
- [ ] Persistence, bioaccumulation and toxicity (PBT) prediction
- [ ] Biodegradability models (links to your bioremediation work)
- [ ] EPI Suite / OPERA models as reference points

### Weeks 53–56: Capstone
- [ ] **Capstone project:** *An OECD-aligned PFAS toxicity and persistence screening model*
  - [ ] Curate a PFAS dataset (CompTox PFAS lists + available toxicity endpoints)
  - [ ] Build and validate models with scaffold/cluster splits
  - [ ] Applicability domain and uncertainty
  - [ ] Mechanistic interpretation linked to AOPs where possible
  - [ ] QMRF-style documentation
  - [ ] Write-up as a blog post or preprint

---

## Phase 6 — AMR genomics specialisation (Weeks 57–72)

**Goal:** apply ML to antimicrobial resistance, building on your microbiology.

### Weeks 57–58: Bioinformatics foundations
- [ ] Biopython: reading FASTA/FASTQ/GenBank
- [ ] Command-line basics (WSL2 or Linux Mint on your T430s)
- [ ] Genome assembly and annotation concepts

### Weeks 59–60: AMR databases and tools
- [ ] CARD and the Resistance Gene Identifier (RGI)
- [ ] NCBI AMRFinderPlus and Pathogen Detection
- [ ] BV-BRC (formerly PATRIC) AMR phenotype data

### Weeks 61–63: Genotype-to-phenotype ML
- [ ] Gene presence/absence features
- [ ] k-mer features and why they're powerful (and hard to interpret)
- [ ] Practice: predict ciprofloxacin resistance in *E. coli* from gene presence/absence

### Weeks 64–65: Pitfalls specific to AMR
- [ ] Population structure and phylogenetic leakage
- [ ] Genotype–phenotype discordance
- [ ] Generalising across countries and collections

### Weeks 66–67: Surveillance and One Health
- [ ] Wastewater and metagenomic AMR surveillance
- [ ] Environmental AMR and links to pollutants (co-selection by metals and POPs)
- [ ] WHO Global Action Plan on AMR 2026–2036

### Weeks 68–72: Capstone
- [ ] **AMR capstone:** *Interpretable resistance prediction with phylogeny-aware validation*, or *Co-selection of AMR in polluted environments* (bridges your toxicology and AMR expertise)

---

## Running through all phases

- [ ] Keep `LEARNING_LOG.md` updated weekly (5 minutes is enough)
- [ ] Read one paper a fortnight; note it in `RESOURCES.md`
- [ ] Publish one write-up per milestone (blog, LinkedIn or GitHub README)
- [ ] Join communities: RDKit discussions, Chemprop, the ASCCT, the UK NC3Rs network
- [ ] By month 12: share one milestone project with a colleague or at a group meeting
