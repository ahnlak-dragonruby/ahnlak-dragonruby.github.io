---
layout: page
title: Quick Start
permalink: /quickstart/
---

Or, "things I wish I'd known last month".

Starting with a new engine (and in many cases a new language!) can be a frustrating
voyage of discovery, and I've already lost count of the times I've cried out "I wish
I knew that!" when someone casually mentions functionality I've failed to come across
on my own.

So, I thought I should write it down. I've tried to group things into logical 
sections but bear in mind this is a living document and might not be the most
evenly edited thing in the world.


Environment
-----------

When you bring up the console, you can enter commands. You can also - and this is
the really cool bit - use tab completion to explore the SDK. So, fire up DR, open
the console, type in `$gtk.` and hit &lt;TAB&gt;. It will show you all the properties of `$gtk`, 
which lets you see what's possible.


Args
----

There's a bunch of useful things in that `args` parameter. Mostly they are documented
somewhere, but these are the ones I've found most helpful and least obvious:

* `args.grid`, a bunch of metrics about the screen size
* `args.outputs.debug`, a special output queue that is rendered last, and not in your
published game


Co-ordinates
------------

The origin of the screen is bottom left; `x` increases as you move right, and `y` as you
move up. Element locations are the same, so the anchor for sprites and labels are at 
their respective bottom lefts.

Angles are based of geometric polar co-ordinates; this means that 0 degrees is directly
*right* - East in terms of compass points - and proceed *anti-clockwise*, with 90 degrees
being North, 180 degrees West and 270 degrees South.


Persistent Data
---------------

Variables you set in your `tick` method will only last for the duration of that tick. 
The practical upshot of this is that is you try and remember your player's location
in `playerx`, you'll find that nothing moves.

`args.state` is a 'magic' global structure; you can add anything you like to it, and
it will persist across ticks. So storing your location in `args.state.playerx` will
mean that you can save your location between ticks and your player will move!