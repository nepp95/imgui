cmake_minimum_required(VERSION 3.14)

project(imgui VERSION 1.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Sources
file(GLOB_RECURSE SOURCES
    "imgui.cpp"
    "imgui_draw.cpp"
    "imgui_tables.cpp"
    "imgui_widgets.cpp"
    "imgui_demo.cpp"
)

add_library(imgui STATIC ${SOURCES})

target_include_directories(imgui PRIVATE "../glm")