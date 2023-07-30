---
title: Figures and Image Widgets
numbering:
  enumerator: 1.%s
---


Figures are typically the most important part of any scientific paper, especially for studies focused on microscopy. We can include figures in many ways, for example by inserting conventional static figures using markdown:



We can also use tabbed viewing in order to show each figure panel individually:




Tabbed image viewing is certainly more space-efficient than conventional figure panel layouts. However with python widgets we can do far better! In additiona to placing multiple panels into the same space, we can also allow the reader to zoom in or out, pan around, and even change the image contrast. This is especially important for microscopy images which may have large dynamic ranges, or require both a large FOV and high resolution to fully appreciate.


```{figure} #app:image_widget

```



more text