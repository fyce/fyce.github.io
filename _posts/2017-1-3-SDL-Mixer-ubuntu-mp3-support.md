---
layout: post
title:  “Mixer not built with MP3 support” on ubuntu 16.04.1 LTS x86_64
---

I was in the process of building(using make) a [tetris game](https://github.com/brenns10/tetris) when I got the error message, "unable to initialize SDL\_mixer" (error handling message defined in the main.c of this program). Further digging pointed to the error, "Mixer not built with MP3 support" (from the [Mix\_GetError](https://www.libsdl.org/projects/SDL\_mixer/docs/SDL\_mixer.pdf) function).
Google search led me [here](http://sdl.5483.n7.nabble.com/quot-Mixer-not-built-with-MP3-support-quot-on-ubuntu-td45263.html), where someone else had encountered this error while using the SDL2\_Mixer in Ubuntu 14.04 LTS x86\_64 and had submitted a patch.

I didn't try using the patch, since I didn't understand the bug, so I dug a little deeper by taking a look at the [SDL\_Mixer 1.2 source](git://anonscm.debian.org/pkg-sdl/packages/sdl-mixer1.2.git).  
 
A bit more research and it turns out that this bug was fixed in [SDL\_mixer 2.0.0](http://hg.libsdl.org/SDL_mixer/rev/1aca2b6d570f) so I stopped here and just used it instead of SDL\_mixer 1.2.  
I'd like to get back to understanding this bug sometime, for learning purposes. 
