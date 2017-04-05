---
layout: post
category : Personal
tagline: "| Open file browser from terminal current directory"
tags : [Personal, ZSH, Open]
---

{% include JB/setup %}

# Opening the current working directory Mac & Windows

To open the current directory of the terminal in Mac or Windows is as simple as typing `open .`, essentially open here, nice and simple.

# For Linux

Things are a little less straight forward, due to the plethora of various desktop environments and file managers things can't be as 
simple as the above, you'd instead need to specify your chosen file manager and well.... that's effort, especially if you work over various linux environments.

But I had a cunning plan! Why not set an alias for your environment be able to use `open .` in place of `neautlous .`?
In looking into this though I discovered an even neater way of achieving this using `xdg-open`. Your preference for your file manager can be
set in xdg and by setting an alias for `open="xdg-open "` I can now use `open .` to my hearts content. Even better it will still allow opening
any directory passed to open as it's still essentially `xdg-open` but shorter.
