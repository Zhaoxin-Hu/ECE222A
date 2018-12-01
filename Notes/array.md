
# Electromagnetics

Quantities/Names | Formulas
---- | ----
solution to wave equation for $\vec{A}$ | $\begin{aligned} \vec{A} &= \iiint_{V'}\mu\vec{J}\frac{e^{-jkR}}{4\pi R}dV \\ &= \mu\vec{J}(0)\frac{e^{-jkr}}{4\pi r}\iiint_{V'}\frac{\vec{J}(r')}{\vec{J}(0)}e^{jk \hat{r}\cdot\vec{r'}}dV \end{aligned}$
solution to wave equation for $\vec{F}$ | $\begin{aligned} \vec{F} &= \iiint_{V'}\epsilon\vec{M}\frac{e^{-jkR}}{4\pi R}dV \\ &= \epsilon\vec{M}(0)\frac{e^{-jkr}}{4\pi r}\iiint_{V'}\frac{\vec{M}(r')}{\vec{M}(0)}e^{jk \hat{r}\cdot\vec{r'}}dV \end{aligned}$
dot product ($\hat{r}\cdot\vec{r'}$) | $\begin{aligned} \hat{r}\cdot\vec{r'} &= \hat{r}\cdot(\vec{x}x'+\vec{y}y'+\vec{z}z') \\ &= x'\sin\theta\cos\phi+y'\sin\theta\sin\phi+z'\cos\theta \end{aligned}$

# Array

Quantities/Names | Formulas
---- | ----
array factor ($AF$) | $\begin{aligned} AF &= \sum_i \frac{I(i)}{I(0)} e^{jk \hat{r}\cdot\vec{r'_i}}\end{aligned}$
array factor linspace ($d_x$) on x axis ($AF_x$) | $\begin{aligned} AF_x &= \sum_i \frac{I(i)}{I(0)} e^{jkd_x\sin\theta\cos\phi}\end{aligned}$

This repo contains an introduction to [Jupyter](https://jupyter.org) and [IPython](https://ipython.org).

Outline of some basics:

* [Notebook Basics](../examples/Notebook/Notebook%20Basics.ipynb)
* [IPython - beyond plain python](../examples/IPython%20Kernel/Beyond%20Plain%20Python.ipynb)
* [Markdown Cells](../examples/Notebook/Working%20With%20Markdown%20Cells.ipynb)
* [Rich Display System](../examples/IPython%20Kernel/Rich%20Output.ipynb)
* [Custom Display logic](../examples/IPython%20Kernel/Custom%20Display%20Logic.ipynb)
* [Running a Secure Public Notebook Server](../examples/Notebook/Running%20the%20Notebook%20Server.ipynb#Securing-the-notebook-server)
* [How Jupyter works](../examples/Notebook/Multiple%20Languages%2C%20Frontends.ipynb) to run code in different languages.

You can also get this tutorial and run it on your laptop:

    git clone https://github.com/ipython/ipython-in-depth

Install IPython and Jupyter:

with [conda](https://www.anaconda.com/download):

    conda install ipython jupyter

with pip:

    # first, always upgrade pip!
    pip install --upgrade pip
    pip install --upgrade ipython jupyter

Start the notebook in the tutorial directory:

    cd ipython-in-depth
    jupyter notebook
