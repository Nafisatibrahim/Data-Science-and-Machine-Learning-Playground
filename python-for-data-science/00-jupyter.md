# Jupyter

Notes on **Jupyter Notebook** / **JupyterLab** for this playground (install, workflow, shortcuts, and anything else I rely on day to day).


Official site: [Project Jupyter](https://jupyter.org/) (install links, try in browser, subprojects).

---

## What Jupyter is (first time)

- **Notebooks** (`.ipynb`) mix **code**, **text** (Markdown), and **outputs** (prints, plots, tables) in one file.
- A **kernel** runs your code (e.g. Python). **Restart** the kernel if things get stuck or after big environment changes.
- **Run order matters**: cells can use variables from cells run *before* in this session.
- **JupyterLab** is the newer full UI; **Jupyter Notebook** is the classic simpler UI. Same notebook format.

---

## Install & run

**Option A - pip (example)**

```bash
pip install jupyterlab
jupyter lab
```

**Option B - conda (example)**

```bash
conda install -c conda-forge jupyterlab
jupyter lab
```

Opens a browser tab (or copy the URL from the terminal). Create a new notebook from the UI and pick a **Python 3** kernel.

For the classic app only: `pip install notebook` then `jupyter notebook`.

---

## Daily basics

| Action | Typical shortcut (JupyterLab) |
|--------|-------------------------------|
| Run cell, go to next | Shift+Enter |
| Run cell, stay here | Ctrl+Enter |
| Run all | Menu: Run → Run All Cells |
| New code / Markdown cell | Toolbar or command palette |

- Use **Markdown cells** for headings and notes; **Code cells** for Python.
- **Save** the notebook often (file is JSON; fine for Git, diffs can be large if outputs are saved).

---

## Helpful magics (Python)

In a code cell:

```python
%matplotlib inline   # show plots in the notebook (classic; still useful in many setups)
```

See [IPython magics](https://ipython.readthedocs.io/en/stable/interactive/magics.html) for `%timeit`, `%%time`, and more.

---

## More reading

| What | URL |
|------|-----|
| Project Jupyter | [https://jupyter.org/](https://jupyter.org/) |
| Jupyter documentation | [https://docs.jupyter.org/](https://docs.jupyter.org/) |
| JupyterLab | [https://jupyterlab.readthedocs.io/](https://jupyterlab.readthedocs.io/) |
| Jupyter Notebook (classic) | [https://jupyter-notebook.readthedocs.io/](https://jupyter-notebook.readthedocs.io/) |
| IPython magics | [https://ipython.readthedocs.io/en/stable/interactive/magics.html](https://ipython.readthedocs.io/en/stable/interactive/magics.html) |
