---
title: Research
subtitle: "Causal inference for real-world healthcare data, Bayesian tree models, and applied machine learning."
author: "Adam M. Kurth"
date: ''
slug: []
aliases:
  - /projects/
categories: []
tags: []
---

## Current work

### When can cancer immunotherapy be stopped?

*Brown University, Department of Biostatistics — with Rebecca Hubbard*

Immune checkpoint inhibitors are effective for a substantial share of patients, which raises a difficult clinical question: once a patient is responding well, is continued treatment still necessary? Randomized trials of de-escalation are slow and expensive, so I approach this by **emulating a target trial** in nationwide oncology electronic health records (Flatiron Health).

The methodological difficulty is that treatment discontinuation is not random. Patients stop because they experience an adverse event or because their disease progresses — exactly the factors that also predict survival. I implement **inverse probability of treatment and censoring weighting (IPTW, IPCW)** under both baseline and time-varying confounding, within a grace-period design that reflects how discontinuation decisions are actually made in the clinic.

Alongside the applied analysis, I design R simulation studies that deliberately vary the confounding structure and the **mismeasurement of time-to-adverse-event**, to quantify how imprecision in the recorded timing of the event that triggers discontinuation propagates into bias in downstream treatment assignment.

## Master's thesis

### DM-CART: Bayesian tree summaries of the full birth-weight distribution

*Arizona State University — advisor: P. Richard Hahn · defended May 2025*

Low birth weight is usually modeled as a binary outcome against a fixed cutoff, which discards most of the distribution. This work develops **DM-CART** (Dirichlet–Multinomial Classification and Regression Trees), a Bayesian nonparametric framework that models the *full* birth-weight distribution from U.S. Natality data.

The method extends CART by replacing the usual splitting objective with a **Dirichlet–Multinomial likelihood** over categorical birth-weight bins, with priors informed by quantiles from the 2020 natality file. A two-tier bootstrap procedure yields stable ensemble predictions, which tightens subgroup-level risk estimates enough to support inference rather than description alone.

Maternal race, smoking status, and marital status emerge as the dominant risk determinants. Restricting attention to low-birth-weight cases alone, infant sex and maternal age become the primary discriminators. The result is a set of interpretable trees with calibrated uncertainty quantification, suitable for targeted intervention and health equity analysis in maternal–infant care.

<div class="doc-actions">
<a href="https://hdl.handle.net/2286/R.2.N.201810">Published thesis</a>
<a href="/files/ms_kurth_thesis.pdf" class="secondary">Thesis PDF</a>
<a href="https://github.com/adamkurth/dm-cart" class="secondary">Code on GitHub</a>
</div>

## Earlier work

### Classifying Mars surface tasks by workload demand

*NASA Glenn Research Center, CHP-PRA team — advisor: Mona Matar · summer 2024*

NASA's Human Research Program needs to know which physiological and cognitive systems each Mars surface task will tax. Working from 1,058 expert-labeled tasks across 18 human-system categories, I built **multi-label deep learning and NLP classifiers in PyTorch** to predict those demands from task protocol text.

The data were severely imbalanced with noisy labels, so the work centered on training strategy: focal loss and targeted resampling rather than increased model capacity. Classifier outputs fed into a **Human Reliability Analysis** framework supporting probabilistic risk assessment for deep-space missions. Presented at the NASA HRP Investigators' Workshop and nominated for a Glenn Research Center Rising Star award.

<div class="doc-actions">
<a href="/files/kurth_iws25_poster.pdf" class="secondary">IWS 2025 poster</a>
<a href="/files/kurth_iws25_abstract.pdf" class="secondary">IWS 2025 abstract</a>
</div>

### Comparing IRT estimation software

*Arizona State University — faculty mentor: Mark Reiser*

Five software packages are in wide use for fitting item response theory models, with limited published evidence on how their estimates compare. I ran the end-to-end analysis for a **Monte Carlo comparison** of Mplus, flexMIRT, SAS PROC IRT, `ltm`, and `mirt`, fitting models in all but SAS and conducting every analysis in R. Manuscript in preparation.

### Signal and noise in low-flux crystallography

*ASU Compact X-ray Free Electron Laser (CXFEL) Labs, Biodesign Institute — advisor: Sabine Botha · 2023–2024*

Compact X-ray sources produce far less flux than full-scale free electron lasers, which makes separating Bragg peaks from water background the central difficulty. I engineered high-throughput diffraction data pipelines in Python, MATLAB, and Bash, and developed a **three-ring integration algorithm** that masks peak intensities to isolate and subtract background noise. I also co-developed a **CNN to detect Bragg peaks** and estimate photon energy and sample–detector distance directly from raw diffraction images.

<div class="doc-actions">
<a href="/files/kurth_bioxfel_poster.pdf" class="secondary">BioXFEL poster</a>
<a href="/files/kurth_bioxfel_abstract.pdf" class="secondary">BioXFEL abstract</a>
<a href="/files/kurth_apm_report.pdf" class="secondary">Technical report</a>
</div>

### Protein entanglement in neurodegenerative disease

*Arizona State University — advisor: Eleni Panagiotou · spring 2025*

Applied **topological data analysis** and knot-theoretic invariants to quantify structural entanglement in intrinsically disordered proteins implicated in neurodegenerative disease, using molecular simulations run with Wenwei Zheng across a range of temperature states and molecular configurations.

## Publications

1. **A. M. Kurth**, P. R. Hahn. Bayesian tree summaries of the full birth-weight distribution: risk profiles from U.S. natality data. *In preparation for submission to Statistics in Medicine.*
2. M. Reiser, **A. M. Kurth**. A Monte Carlo comparison of the efficacy of Mplus, flexMIRT, PROC IRT, `ltm`, and `mirt` in IRT model estimation. *In preparation.*

A full list of talks and posters is on the **[CV](/cv/)**.
