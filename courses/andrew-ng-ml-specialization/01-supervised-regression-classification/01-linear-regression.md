# Linear regression (one variable)

Notes from **Course 1** (Andrew Ng ML Specialization): what linear regression is, how a **model** $f$ fits into supervised learning, and the notation $f_{w,b}(x) = wx + b$.

---

## Supervised learning recap


| Idea                    | Meaning                                                                   |
| ----------------------- | ------------------------------------------------------------------------- |
| **Supervised learning** | Learn from **labeled** examples: input **x** with known **target** **y**. |
| **Regression**          | Predict a **number** from many (or infinitely many) possible values.      |
| **Classification**      | Predict a **category** from a **small, finite** set of labels.            |


**Example (regression):** predict **house price** from **house size** (and possibly other features later).

Linear regression is **one** regression model; others exist (polynomial, trees, neural nets, ...).

---

## Terminology for the data


| Symbol / term      | Meaning                                                                                                     |
| ------------------ | ----------------------------------------------------------------------------------------------------------- |
| **Training set**   | The data used to **train** the model (features + targets).                                                  |
| **Feature**        | Input variable, often written **x** (also called input variable).                                           |
| **Target**         | The true output we want to predict, **y** (also called output variable or target variable).                 |
| **m**              | Number of **training examples**.                                                                            |
| **One example**    | A pair **$(x, y)$**.                                                                                        |
| **$i$-th example** | **$(x^{(i)}, y^{(i)})$** - the superscript **$(i)$** indexes the **training example** (not exponentiation). |


---

## From training set to prediction

**Flow:** the **training set** and **learning algorithm** produce a **model** **$f$**; for a **new** **$x$**, you evaluate **$f$** to get the **prediction** **$\hat{y}$**.

1. **Training set** contains **features** and **targets** (many $(x^{(i)}, y^{(i)})$ pairs).
2. **Learning algorithm** uses that set to choose a good **model**.
3. The **model** is a **function** **$f$**.
4. For a **new** feature value **$x$**, the model outputs **$\hat{y}$** (“y-hat”), the **prediction** (estimate of **$y$**). The **target** **$y$** is the actual value in data; **$\hat{y}$** is what **$f$** outputs.

**Concrete instance:** **size** (feature) $\to$ **$f$** $\to$ **price** (estimated) = **$\hat{y}$**.

### Color legend (as in the slides)


| Color role          | Meaning                                    |
| ------------------- | ------------------------------------------ |
| **Feature / input** | **$x$** (e.g. size)                        |
| **Model**           | **$f$** - the learned function             |
| **Prediction**      | **$\hat{y}$** - estimated output           |
| **Target**          | **$y$** - true output in the training data |


---

## How to represent $f$? (Univariate linear regression)

For a **straight-line** relationship with **one** feature, use a **linear function** with parameters **$w$** (weight, slope) and **$b$** (bias, intercept):

$$
f_{w,b}(x) = wx + b
$$

You can abbreviate **$f_{w,b}(x)$** as **$f(x)$** when the parameters are clear from context.

- **$w$** and **$b$** are **parameters** (also called **coefficients** or **weights** in some texts). The learning algorithm **adjusts** **$w$** and **$b$** so that **$f_{w,b}(x^{(i)})$** is close to **$y^{(i)}$** on the training set.
- **Univariate linear regression** = linear regression with **one** variable **$x$** (one feature per example).

On a plot, **$x$** is on the horizontal axis and **$y$** (or **$\hat{y}$** on the line) on the vertical axis; the graph of **$f$** is a **line**—the equation **$f_{w,b}(x) = wx + b$** is that line in **$x$**–**$y$** space.

---

## What comes next

This note uses **one** feature for simplicity. **Multivariate** linear regression uses many features and replaces **$wx$** with a **weighted sum** of inputs (vector **$\mathbf{w}$** and dot product with **$\mathbf{x}$**), still linear in the parameters.

---

## Quick glossary (this page)


| Term                | Meaning                                                       |
| ------------------- | ------------------------------------------------------------- |
| **$f$** / **model** | Function mapping feature **$x$** to prediction **$\hat{y}$**. |
| **$\hat{y}$**       | Prediction; read as “y-hat.”                                  |
| **$w$, $b$**        | Weight and bias in **$f_{w,b}(x) = wx + b$**.                 |
| **Univariate**      | One input feature **$x$** per example.                        |


