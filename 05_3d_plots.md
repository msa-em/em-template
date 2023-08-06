---
title: 3D Plots and 3D Widgets
numbering:
  enumerator: 3.%s
---

While most microscopy images are often obtained in projection, advanced techniques such as electron tomography and multislice ptychography enable the 3D reconstruction of structures.
Due to the limitations of print journals, these results are often presented as 2D slices of the 3D objects of interest or at-best as 360° orbit movies.
These make the results difficult to interpret and evaluate.

To overcome these limitations, we can embed interactive 3D visualization libraries directly on the page including volumetric rendering as in [](#fig_volume_rendering) and volume slicing as in [](#fig_volume_slicing).

:::::{tab-set}

::::{tab-item} Volume Rendering
:sync: tabmovie2

:::{figure} #app:interactive_volume_rendering
:name: fig_volume_rendering
Joint ptychographic-tomographic reconstruction of a simulated CNT with a missing wedge of 60 deg. Reproduced from [G Varnavides](https://github.com/py4dstem/py4DSTEM_tutorials/blob/main/notebooks/ptycho05_CNT_overlap-tomography.ipynb).
:::

::::

::::{tab-item} Volume Slicing
:sync: tabmovie1

:::{figure} #app:interactive_volume_slicing
:name: fig_volume_slicing
Joint ptychographic-tomographic reconstruction of a simulated CNT with a missing wedge of 60 deg. Reproduced from [G Varnavides](https://github.com/py4dstem/py4DSTEM_tutorials/blob/main/notebooks/ptycho05_CNT_overlap-tomography.ipynb).
:::

::::

:::::

