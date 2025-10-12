---
title: "Project Fake Reviews Detection SOMTE"
layout: post
date: 2024-04-22 09:00:00 -0700
projects: true
category: project
externalLink: https://github.com/almique/Project_Fake_Reviews_Detection_SOMTE
description: "Benchmarking classical ML and deep learning pipelines to distinguish synthetic and human-written reviews across 40k samples."
tag:
  - NLP
  - Machine Learning
  - Text Classification
  - Fraud Detection
---

**Synopsis**

Online consumer reviews help buyers decide what to trust, yet deceptive, computer-generated posts routinely distort perceptions. This research build investigates automated detection strategies beyond BERT by comparing classical algorithms and modern deep learning models on a balanced dataset of 20,000 fake and 20,000 authentic reviews spanning multiple product categories.

**Problem Statement**

The presence of fake reviews undermines the credibility of e-commerce platforms. The goal is to distinguish computer-generated (CG) fake reviews from genuine, human-authored (OR) reviews. By exploring alternative model architectures and feature pipelines—including traditional ML, hybrid ensembles, and transformer-based representations—the project seeks to surface stronger detection signals.

**Highlights**

- Curated and released benchmark datasets that capture diverse review lengths, product domains, and linguistic patterns.
- Built evaluation harnesses that report AUC, accuracy, precision, recall, and other text classification metrics for apples-to-apples comparisons.
- Documented findings to support repeatable academic and industrial experimentation in fake-review detection.

**Tech Stack & Methods**

Python, scikit-learn, PyTorch, transformer encoders, SMOTE variants for imbalance resilience, and experiment tracking with reproducible notebooks.
