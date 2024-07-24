---
title: Typesetting and References
numbering:
  enumerator: 1.%s
---

(paper_layout)=

## Paper Layout

Your paper should be divided into logical sections.
We recommend using different markdown files as "chapters" of your paper, and then sub-sections inside each file using markdown titles.
We require three sections in the `index.md` file:

- Abstract
- Acknowledgements
- Competing Interests

We also requite that you include both and introduction and conclusion section.
You may organize the remainder of the paper however you wish.
All code and data required to reproduce the results be provided inline or as external download links to public repositories.
Writing style and article content should generally follow the guidelines of the [Microscopy and Microanalysis](https://academic.oup.com/mam/pages/general-instructions#Manuscript) journal.
Note that you can specify acronyms in the `myst.yml` configuration file.
For example try hovering over this text: M&M.

(equations)=

## Equations

Equations can be typeset using LaTeX notation.
To write an inline equation, place it inside a pair of `$` symbols, and create equation blocks using pairs of `$$` symbols.
For example, the general Schrödinger equation is given by $i \hbar \frac{\partial}{\partial t} \psi(t) = \hat{H} \psi(t)$,
while the time-independent Schrödinger equation for fast electrons along the $z$ axis in the small angle scattering limit is given by

$$
\label{eq_schrodinger_electrons}
\frac{\partial \psi(\vec{r}) }{\partial t}
= \frac{i \lambda}{4 \pi} \nabla^2_{xy} \psi(\vec{r}) + i \sigma V(\vec{r}) \psi(\vec{r}),
$$

where $i$ is the imaginary constant, $\hbar$ is the Reduced Planck constant, $\hat{H}$ is a [Hamiltonian operator](<wiki:Hamiltonian_(quantum_mechanics)>), $\psi$ is a wavefunction defined over time $t$ or 3D space $r=(x,y,z)$, $\lambda$ is the reduced electron wavelength, $\sigma$ is the electron-sample interaction constant, and $V(\vec{r})$ is the sample's electrostatic potential [@kirkland2020advanced].

Equations can be linked using the markdown syntax, for example the above equation has the label `eq_schrodinger_electrons`, which can be referenced using
`Equation [](#eq_schrodinger_electrons)`
which is rendered as
Equation [](#eq_schrodinger_electrons).
We suggest using highly descriptive labels for equations and other content.

For other ways to embed mathematical statements, see <xref:mystmd/math>.

(tables)=

## Tables

Tables can be written with markdown syntax:

````
```{list-table} This is a table.
:header-rows: 1
:name: table_example
* - name
  - value 1
  - value 2
* - a
  - 1
  - 2
* - b
  - 3
  - 4
```
````

which will generate this Table:

```{list-table} This is a table.
:header-rows: 1
:name: table_example
* - name
  - value 1
  - value 2
* - a
  - 1
  - 2
* - b
  - 3
  - 4
```

More information on markdown tables is given here <xref:mystmd/tables>.

(citations)=

## Links, References and Citations

You can link to any figure, equation, code block, section of your paper, or external link.
This can performed by using markdown links, or by assigning a `label` to any portion of your paper and then linking to it.
Some examples

- [](./index.md)
- [](./02_typesetting.md)
- [](#paper_layout)
- Equation [](#eq_schrodinger_electrons)
- [](#fig_EWR_graphene_phase)
- [](#fig_movie_widget_ipympl)
- [](#table_example)
- <https://www.go-fair.org/fair-principles/>
- {cite:p}`wilkinson2016fair`

Citations can be implemented using either a BibTeX `.bib` file, or as DOI links.
For example, this BibTeX entry:

```
@article{ophus2019four,
  title={Four-dimensional scanning transmission electron microscopy (4D-STEM):
    From scanning nanodiffraction to ptychography and beyond},
  author={Ophus, Colin},
  journal={Microscopy and Microanalysis},
  volume={25},
  number={3},
  pages={563--582},
  year={2019},
  publisher={Cambridge University Press},
  doi={https://doi.org/10.1017/S1431927619000497},
}
```

can be cited using the commands

```md
@ophus2019four
[@ophus2019four]
[See @ophus2019four, pg. 4]
```

which are in turn rendered as:

- @ophus2019four
- [@ophus2019four]
- [See @ophus2019four, pg. 4]

Writing this citation as a DOI link `[@doi:10.1017/S1431927619000497]` produces:
[@doi:10.1017/S1431927619000497]

Each citation will be added to the bibliography at the bottom of each markdown file.
Note that we require you to include a DOI link for all journal articles, textbooks, and conference proceedings. The DOIs will be checked when you submit your Computational Article.

For more information on markdown links, see <xref:mystmd/cross-references>.
For more information on citations, see <xref:mystmd/citations> especially <xref:mystmd/citations#markdown-citations>.

(code_blocks)=

## Code Blocks

Code can be directly embedded into your article using `.ipynb` files.
You can also print code blocks using markup syntax ` ```language `.
For example, this block:

````myst
```python
import numpy as np

def add_two_numbers(a, b):
  return a + b
```
````

will be rendered as:

```python
import numpy as np

def add_two_numbers(a, b):
  return a + b
```

For common languages such as `python`, syntax highlighting will be automatically applied.

For more information on typesetting code blocks, see <xref:mystmd/code>.
