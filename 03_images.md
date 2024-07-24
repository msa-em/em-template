---
title: Figures and Image Widgets
numbering:
  enumerator: 1.%s
---

Figures are typically the most important part of any scientific paper, especially for studies focused on microscopy. 
We can include figures in many ways, for example by inserting conventional static figures using markdown:

:::{figure} ./figures/EWR_graphene_v03.pdf
:name: fig_EWR_graphene
HRTEM focal series reconstruction of a single-layer graphene GB. (a) Exit wave phase, enlarged in (b). (c) Exit wave amplitude, enlarged in (d).
Adapted from {cite:t}`ophus2016automatic`.
:::

However, figures such as [](#fig_EWR_graphene) are very limited. 
We need to make a trade-off between showing the entire FOV and zooming in to show the atomic details. 
This is solved in [](#fig_EWR_graphene) by having two panels for both the complex wave phase and amplitude, one showing the full FOV and another as an enlarged panel. 
These kinds of trade-offs are unavoidable for print journals where page space is limited. 

However, since this journal is intended be read online, we can make more efficient use of the screen real estate. 
One method is to use tabbed viewing in order to show each figure panel individually:

:::::{tab-set}

::::{tab-item} Graphene GB exit wave phase
:sync: tab1

:::{figure} ./figures/EWR_graphene_phase.jpg
:name: fig_EWR_graphene_phase
:width: 512px
Exit wave phase of a single-layer graphene GB, from HRTEM focal series reconstruction. Adapted from {cite:t}`ophus2016automatic`.
:::

::::

::::{tab-item} Graphene GB exit wave amplitude
:sync: tab2

:::{figure} ./figures/EWR_graphene_amp.jpg
:name: fig_EWR_graphene_amp
:width: 512px
Exit wave amplitude of a single-layer graphene GB, from HRTEM focal series reconstruction. Adapted from {cite:t}`ophus2016automatic`.
:::

::::

:::::

Note that while we only display a single tab at a time, we can reference these panels individually: the EWR phase is shown in [](#fig_EWR_graphene_phase), while the EWR amplitude is show in [](#fig_EWR_graphene_amp). 
If you mouse over either of these links, previews of the figure panel will pop up.


Tabbed image viewing is certainly more space-efficient than conventional figure panel layouts. 
However with python widgets we can do far better! 
In addition to placing multiple panels into the same space, we can also allow the reader to zoom in or out, pan around, and even change the image contrast. 
This is especially important for microscopy images which may have large dynamic ranges, or require both a large FOV and high resolution to fully appreciate.


:::{figure} #app:interactive_image
:name: fig_EWR_graphene_interactive
:placeholder: ./figures/EWR_graphene_interactive.png
Exit wave reconstruction of a single-layer graphene GB, from HRTEM focal series. Adapted from {cite:t}`ophus2016automatic`.
:::

Try playing around with this figure!
You can zoom in, pan around, change the contrast range, and even change the colormap. 
Additionally we can use a dropdown menu to select either the EWR phase or amplitude. 
We reference [](#fig_EWR_graphene_interactive) in the same manner as before.

