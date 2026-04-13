# Supervised learning — introduction

Notes from **Course 1** of Andrew Ng’s Machine Learning Specialization: what ML is, where it shows up, and how **supervised** learning fits in.

---

## What is machine learning?

> **In one sentence:** **Machine learning** is the science of getting computers to **learn from data** instead of being **explicitly programmed** for every rule.

---

## Why it matters — use cases

| Area | Example |
|------|--------|
| **Web** | Ranking and search |
| **Speech** | Voice recognition from audio |
| **Healthcare** | Diagnosis from X-rays or scans |
| **Transport** | Self-driving systems |
| **Language** | Machine translation |

These ideas show up across **healthcare, finance, insurance, construction, manufacturing, retail**, and many other fields.

---

## AGI in one line

**AGI (Artificial General Intelligence)** refers to systems as broadly capable as humans, including **general reasoning**. Today’s practical ML is usually narrower than that vision.

---

## A classic definition — Arthur Samuel (1959)

> **Arthur Samuel (1959):** *“Field of study that gives computers the ability to learn without being explicitly programmed.”*

### What Samuel’s checkers program did (intuition)

Samuel programmed the computer to play **many thousands of games against itself**. By noticing **which board positions tended to lead to wins** versus **losses**, the program **learned over time** which situations were good or bad. Because the machine could run that loop at scale, it gained far more experience than a human could manually, and **eventually played checkers better than Samuel himself**.

> **Takeaway:** Learning means **feedback from experience** (outcomes), not only hand-written rules.

---

## The two big families of ML

| Type | Labels **y** | Goal (high level) |
|------|----------------|-------------------|
| **Supervised learning** | Known for training examples | Learn **input → output** mapping |
| **Unsupervised learning** | Not given | Find **structure** or **patterns** (no single “right answer” per example) |

---

## Supervised learning

**Supervised learning** means algorithms that learn an **input → output** mapping. You give the learner **labeled examples**: for each input **x**, the correct **y** is known.

### Two supervised problem types

| | **Regression** | **Classification** |
|---|----------------|---------------------|
| **Predicts** | A **number** from many possible values | A **category** from a **small, finite** set |
| **Example** | House **price** from size | Tumor **benign vs malignant** from features |

- **Regression:** output is on a **continuous** scale (e.g. price in dollars).
- **Classification:** output is a **class** or **category** (e.g. benign / malignant — **two** classes → classification).

---

## Unsupervised learning

**Unsupervised learning:** the **label y is not given**. The algorithm looks for **structure** — clusters, groupings, or patterns — without a provided “correct class” for each point.

**Example:** **Google News**-style **clustering** — grouping related stories even when no human labeled every article in advance.


---

## Quick glossary (this page)

| Term | Meaning here |
|------|----------------|
| **Label (y)** | The correct output you want to predict |
| **Regression** | Predict a numeric value |
| **Classification** | Predict a discrete category |
| **Clustering** | Group similar items (unsupervised) |
