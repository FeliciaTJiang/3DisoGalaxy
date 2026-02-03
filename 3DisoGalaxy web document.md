# 3DisoGalaxy Portal Documentation  
*Isoform foldome × structure similarity × subtype-aware exploration*

---

## 🔬 Project Overview

3DisoGalaxy is an interactive portal for exploring a **high-structure-quality breast-cancer isoform foldome** in a **structure-similarity network**. Each node represents an isoform, and proximity/edges reflect structural similarity. Isoforms with similar structures naturally form clusters, which often correspond to shared **modular architecture** and **functional tendencies inferred from structure**.

The portal is designed for two complementary use cases:

- **Global discovery:** Understand the overall landscape of isoform structural space (and inferred functional distribution) across breast cancer.
- **Targeted investigation:** Rapidly focus on subtype-relevant or expression-shifted isoforms, then drill down into detailed metadata, expression, and nearest structural neighbors.

---

## 📈 Progress Milestones

### Dataset Foundation
- Curated a **high-confidence isoform foldome** (high structure quality).
- Built a **structure similarity space** to organize isoforms into an interpretable global network.

### Functional Annotation Pipeline
- Mapped isoforms into structure-informed neighborhoods to support **function-inclined clustering** (structure-driven inference rather than gene-level assumptions).

### Model Development
- Implemented a **web-based interactive network** with:
  - subtype-aware highlighting,
  - expression-driven filtering,
  - node-centric detail panels,
  - gene-centric focus mode.

### Evaluation
- Ensured the portal supports rapid, human-interpretable exploration:
  - *global → cluster → node → neighbors → gene panel* workflow,
  - consistent visual encoding for subtype association and differential expression.

---

## 🚀 Next Steps (User Workflows)

### 1) Global Structure Network: see the isoform foldome at a glance
**What you see**
- A network of high-quality isoform structures.
- Isoforms cluster according to **structural similarity**, providing an intuitive map of structural (and inferred functional) distributions across breast cancer.

**Why it matters**
- Instead of inspecting isoforms one gene at a time, you can directly observe how isoforms populate the structural space and where subtype-enriched regions appear.

---

### 2) Global Explore & Highlight: instant focus on subtype-relevant isoforms
Use the **control panel (bottom-left)** to highlight isoforms most associated with a specific breast-cancer subtype.

**One-click highlight**
- Choose one subtype (supports **five subtype categories**).
- The portal highlights isoforms with the strongest subtype relevance, allowing you to immediately locate the most informative “core isoforms” within a dense network.

**Use case**
- Rapid hypothesis generation: “Which isoforms best represent this subtype in structural space?”

---

### 3) Expression-driven filtering: Basal vs non-basal Log2FC brush selection
At the bottom of the page, a bar chart displays **RNA-seq differential expression (Log2FC)** for **Basal vs non-basal**.

**How to use**
- Drag (brush) a Log2FC interval to select a region of interest.
- The corresponding isoforms are highlighted in the structural network.

**Why it matters**
- This is a fast route to candidate discovery:
  - highlight **Basal-upregulated isoforms** as potential **targets** or **biomarker candidates**,
  - immediately view where these candidates sit in the structural landscape.

---

### 4) Interpret node appearance (visual encoding)
The network uses simple visual rules so you can read it without opening any panels:

- **Node color** → the isoform’s most representative breast-cancer subtype.
- **Node size** → strength of subtype-specific upregulation (e.g., larger nodes indicate a stronger **Log2 Fold Change** in a given subtype such as Basal-like).

---

### 5) Click any node: deep dive in the right-side panel
Click a node to open a detailed sidebar that includes:

- **Biological metadata** (isoform identity and related annotations)
- **Expression profile visualizations**
- **Nearest structural neighbors**
  - a ranked list of isoforms most structurally similar to the selected isoform,
  - useful for comparing structure-driven functional tendencies and local remodeling patterns.

**Typical workflow**
1. Click a highlighted isoform  
2. Inspect its expression and subtype association  
3. Compare with nearest structural neighbors  
4. Identify whether the isoform is an isolated structural outlier or part of a coherent functional neighborhood

---

### 6) Gene-focused mode: search and isolate all isoforms of a gene
If you already have a gene of interest (e.g., `BRCA1`), use the **search box (top-left)**.

**What happens**
- The portal locates the gene’s isoforms in the network.
- A compact gene-focused view lists **all isoforms of that gene**, enabling a focused comparison across:
  - structure and structure similarity relationships,
  - inferred functional tendencies / annotations,
  - RNA-level expression patterns,
  - translation/protein-level evidence where available (e.g., Ribo-seq layer).

**Why it matters**
- This mode is designed for “I know the gene; show me its isoform diversity in structure, expression, and translation evidence.”

---

## 🌟 Strategic Position (What makes this portal different)

Most breast-cancer resources are gene-centric and summarize at the gene level. This portal is **isoform-centric** and **structure-grounded**, enabling:

- structure-first navigation of isoform space,
- subtype-aware discovery directly in the structural landscape,
- expression-driven candidate prioritization linked to structure,
- immediate comparison of isoforms via nearest structural neighbors.

---

## FAQ / Troubleshooting

**Q1. Why do isoforms cluster—does that mean they have identical functions?**  
Clusters indicate **structural similarity**, which often correlates with shared modular architecture and functional tendencies. This is **inference-friendly**, not proof of identical function.

**Q2. I highlighted a subtype but see nodes across multiple regions. Is that expected?**  
Yes. A subtype may involve multiple biological programs, which can manifest as multiple structural neighborhoods.

**Q3. How should I interpret a large node that is structurally isolated?**  
This can indicate a strongly subtype-shifted isoform with an unusual structure relative to others—often a high-priority candidate for manual inspection.

---

## Citation
If you use this portal in a manuscript, please cite the associated 3DisoGalaxy resource paper (citation text to be added here).

---

## Changelog
- v1.0 — Initial public release (structure network + subtype highlight + Log2FC brushing + node details + gene search)
