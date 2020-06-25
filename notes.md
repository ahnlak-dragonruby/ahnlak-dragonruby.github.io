---
layout: page
title: Notes
permalink: /notes/
---

This page is a bit of a holding space, for useful DR-related information that I haven't
found a permanent home for.

Render Order
------------

This is the order of rendering as best I can determine; things rendered later overwrite
things rendered earlier so, for example, lines always overwrite sprites.

* solids
* static_solids
* sprites
* static_sprites
* primitives
* static_primitives
* labels
* static_labels
* lines
* static_lines
* borders
* static_borders
