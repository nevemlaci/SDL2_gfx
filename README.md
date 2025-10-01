# SDL2 GFX with CMake support

This is a fork of SDL2_GFX. I've removed the system specific build configurations and added a simple `CMakeLists.txt` .

There are two CMake targets:
* `sdl2_gfx_static` is a static library built from the sources of `SDL2_GFX`
* `sdl2_gfx_dynamic` is a dynamic library built from the sources of `SDL2_GFX`

There is no support for `cmake install` yet.

## Disclaimer
I am not the author of this library!

I am in no way associated with the author (Andreas "aschiffler" Schiffler).

The original page for the library can be found at: https://www.ferzkopp.net/wordpress/2016/01/02/sdl_gfx-sdl2_gfx/

You can find the old readme in `README.old.md` .
