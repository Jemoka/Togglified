# C++ Config
cmake_minimum_required(VERSION 3.14.0)
set( CMAKE_CXX_STANDARD 14 )

# Project Start. Keep this at the topish.
project (Togglified)

# imgui
include_directories("lib/imgui/")
file(
    GLOB imgui
		"lib/imgui/imgui.cpp"
		"lib/imgui/imgui_draw.cpp"
		"lib/imgui/imgui_demo.cpp"
		"lib/imgui/*.h"
)
source_group(imgui_files ${imgui})

add_executable(togglified togglified.cpp)

