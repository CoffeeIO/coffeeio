---
layout: default
type: "docs"
title:  "DOM-based VRT license"
permalink: dom-based-vrt/license
---

{% include vrt-nav.html %}





<p align="center">
    <img alt="Rax" src="/assets/project/dom-based-vrt/dom-based-vrt.png" width="600">
</p>

### The problem

When developing on a web application unintended side effects in the form of visual changesare likely to occur. The manual process for finding these issues is long and tedious and existing tools suffer from either bad recall or bad precision.


The most prevalent technique to define where there is a visual change is referred to as the pixel-by-pixel method and simply consists of comparing the individual pixels of two images. One image is taken before the change and the other image is taken after the code changes are applied. The idea behind this is that if a pixel has changed color, this must bean indicator that either an element has moved, been removed, changed property or state in some way.


<p align="center">
    <img alt="Rax" src="/assets/project/dom-based-vrt/figure3.png" width="600">
</p>

This novel approach suffers from 2 issues.


- We don’t know what the issue is and have no means of easily identify it.
- We are highly suceptible for the cascading error problem.

Here is the same test, but with 1 additional change. Header has added 20px padding on the bottom. Now test has too many false positives that to be useful for anything.

<p align="center">
    <img alt="Rax" src="/assets/project/dom-based-vrt/figure4.png" width="600">
</p>


---

---

Copyright &copy; 2016 Mathias Grundtvig Andreasen (MGApcDev). Licensed under the terms of the [BSD license](LICENSE.md).
