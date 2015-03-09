---
layout: post
category : Projects
tagline: "| Hello World "
tags : [OSx, mac, OpenGL, C++, uni]
---

{% include JB/setup %}

For the past few weeks we have been faced with the fubar way that OSx deals with OpenGL, trying to get a basic game running on at least OpenGL 3.0. With the ballsed up documentation and complete misunderstanding on multiple forums of how to implement this; with most tutorials forcing you to use Xcode and using massively deprecated versions of OpenGL.

In the end it turned out to be a simple matter of changing the include in the header files from GL/GL.h to OpenGL/gl3.h. So I really hope that this is easier to find than the soloution that we found.
