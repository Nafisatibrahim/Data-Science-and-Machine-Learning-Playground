# Google Colab

Notes on **Google Colaboratory** for this playground: browser notebooks, runtime, Drive, and how it compares to local Jupyter.

Official entry points: [Colab app](https://colab.research.google.com/) and [Colab overview / learn](https://colab.google/).

---

## What Colab is (first time)

- **Colab** runs **Jupyter-style notebooks in the browser**. You get a Python environment without installing Python on your machine (optional GPU/TPU runtimes for some workloads).
- Notebooks are the same **`.ipynb`** idea: **code cells**, **Markdown**, and **outputs** in one document.
- A **runtime** is the VM that executes your code. Runtimes **disconnect** after idle time or when you close the tab for long enough - **save to Google Drive** or **download** the notebook so you do not lose work.
- **Run order matters**, same as Jupyter: variables exist only after the cells that define them have been run in this session.

---

## Getting started

1. Open [colab.research.google.com](https://colab.research.google.com/) while signed into a **Google account**.
2. **File → New notebook** (or open an existing `.ipynb` from Drive / GitHub / upload).
3. Run a cell with **Shift+Enter** (or the play button). The first run may take a few seconds while the runtime starts.

---

## Runtime, hardware, and limits

- **Runtime → Change runtime type** lets you pick **CPU**, **GPU**, or **TPU** when available. Free tiers have **usage limits** and queues; details change over time - see the official FAQ below.
- If you need a **long-running** job or **full control** of packages, local **Jupyter** or a paid cloud VM is often easier.

---

## Saving and sharing

- **File → Save a copy in Drive** keeps a copy tied to your Google Drive.
- **File → Download** saves `.ipynb` (or export to HTML / PDF from the menu where offered).
- **Share** works like other Google files if the notebook lives in Drive (check permissions).
- **GitHub**: you can open notebooks from GitHub via Colab integrations / URLs (see docs); good for coursework repos.

---

## Files, data, and Google Drive

- The default runtime filesystem is **temporary**. Upload small files with the **folder icon** in the left sidebar, or fetch data with `urllib`, `pandas.read_csv(url)`, etc.
- To use **Drive** files from a notebook:

```python
from google.colab import drive
drive.mount('/content/drive')
# then read paths under /content/drive/MyDrive/...
```

---

## Packages and plotting

Install packages in a code cell (prefer `%pip` so the running kernel sees the install):

```python
%pip install some-package
```

Many scientific stacks are **preinstalled**. For plots, **matplotlib** often works without extra setup; try:

```python
import matplotlib.pyplot as plt
```

---

## Daily basics

| Action | Typical shortcut |
|--------|------------------|
| Run cell, focus next | Shift+Enter |
| Run cell, stay | Ctrl+Enter |
| Run all | Runtime → Run all |
| Comment line | Ctrl+/ |

---

## Good habits

- **Do not put passwords or API keys** in notebooks you share or commit to Git; use Colab **secrets** (where available) or environment-specific config outside the repo.
- **Restart runtime** (Runtime → Restart session) if imports or installs behave oddly.
- **Re-run all** before assuming a notebook is “clean” from top to bottom.

---

## More reading

| What | URL |
|------|-----|
| Open Colab | [https://colab.research.google.com/](https://colab.research.google.com/) |
| Colab (Google) | [https://colab.google/](https://colab.google/) |
| Welcome / intro notebook | [https://colab.research.google.com/notebooks/intro.ipynb](https://colab.research.google.com/notebooks/intro.ipynb) |
| FAQ | [https://research.google.com/colaboratory/faq.html](https://research.google.com/colaboratory/faq.html) |

For local notebooks, see [Jupyter](00-jupyter.md) in this folder.
