cmake_minimum_required(VERSION 3.25)
project(sdl2_gfx)

find_package(SDL2 REQUIRED)

set(
    sdl2_gfx_source_files
    SDL2_gfxPrimitives.c
    include/SDL2_gfxPrimitives.h
    include/SDL2_gfxPrimitives_font.h
    SDL2_imageFilter.c
    include/SDL2_imageFilter.h
    SDL2_rotozoom.c
    include/SDL2_rotozoom.h
)

add_library(
        sdl2_gfx_dynamic SHARED
        ${sdl2_gfx_source_files}
)

target_link_libraries(sdl2_gfx_dynamic PRIVATE SDL2::SDL2)
target_include_directories(sdl2_gfx_dynamic PUBLIC
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
        $<INSTALL_INTERFACE:include>
)

add_library(
        sdl2_gfx_static STATIC
        ${sdl2_gfx_source_files}
)

target_link_libraries(sdl2_gfx_static PRIVATE SDL2::SDL2)
target_include_directories(sdl2_gfx_static PUBLIC
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
        $<INSTALL_INTERFACE:include>
)
