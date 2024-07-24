---
title: Movies and Movie Widgets
numbering:
  enumerator: 2.%s
---

Often, the data we wish to present are logically arranged in a sequence, e.g. an acquired movie during an in-situ TEM experiment or 360° orbits around 3D visualizations.
In typical print journals these are often presented as snapshots or attached as supplemental materials.

Since the journal is intended to be read online, we can instead embed movies directly on the page.
Below we demonstrate a number of ways to accomplish these including direct HTML embedding as in [](#fig_movie_html), precomputed animations as in [](#fig_movie_widget_ipympl), and fully-interactive movie players as in [](#fig_movie_widget_ipympl_ipywidgets).

:::::{tab-set}

::::{tab-item} Direct Embedding
:sync: tabmovie1

:::{figure} ./notebooks/data/STEM4D_remake.mp4
:name: fig_movie_html
:width: 300
Animation showing the principles of conventional HAADF-STEM and 4D-STEM. Reproduced from [C Ophus](https://www.youtube.com/watch?v=2QUFgO5x1OY&lc=UgyE2dCdpNqakBdpAfB4AaABAg).
:::

::::

::::{tab-item} Animations
:sync: tabmovie2

:::{figure} #app:animated_movie
:name: fig_movie_widget_ipympl
Multislice HRTEM simulation of a hollow gold nanosphere. Sample morphology estimated from  {cite:p}`lindley2021spatiotemporal`.
:::

::::

::::{tab-item} Interactive Movies
:sync: tabmovie3

:::{figure} #app:interactive_movie
:name: fig_movie_widget_ipympl_ipywidgets
:placeholder: ./figures/movie_widget_ipympl_ipywidgets.png
Multislice HRTEM simulation of a hollow gold nanosphere. Sample morphology estimated from  {cite:p}`lindley2021spatiotemporal`.
:::

::::

:::::

