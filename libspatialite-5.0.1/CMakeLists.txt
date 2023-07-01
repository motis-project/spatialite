cmake_minimum_required(VERSION 3.10)
project(libspatialite LANGUAGES C)

file(GLOB_RECURSE spatialite-src-files src/*.c)
add_library(spatialite ${spatialite-src-files})
target_include_directories(spatialite SYSTEM PUBLIC . src)