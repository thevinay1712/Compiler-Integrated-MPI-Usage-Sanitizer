cmake_minimum_required(VERSION 3.13)

# Umbrella CMakeLists to group MPISan-related subprojects without moving sources.
# This adds the existing `src/pass` and `src/runtime` source directories but
# places their build output under `build/src/mpisan/...` to keep build artifacts
# grouped together.

add_subdirectory(${CMAKE_SOURCE_DIR}/src/pass ${CMAKE_BINARY_DIR}/src/mpisan/pass)
add_subdirectory(${CMAKE_SOURCE_DIR}/src/runtime ${CMAKE_BINARY_DIR}/src/mpisan/runtime)
