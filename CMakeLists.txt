cmake_minimum_required(VERSION 3.23)

project(imgui)

add_library(${PROJECT_NAME} 
     ${CMAKE_CURRENT_SOURCE_DIR}/imgui_demo.cpp
     ${CMAKE_CURRENT_SOURCE_DIR}/imgui_draw.cpp
     ${CMAKE_CURRENT_SOURCE_DIR}/imgui_tables.cpp
     ${CMAKE_CURRENT_SOURCE_DIR}/imgui_widgets.cpp
     ${CMAKE_CURRENT_SOURCE_DIR}/imgui.cpp
     ${CMAKE_CURRENT_SOURCE_DIR}/backends/imgui_impl_opengl3.cpp
     ${CMAKE_CURRENT_SOURCE_DIR}/backends/imgui_impl_glfw.cpp)

target_include_directories(${PROJECT_NAME}  PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_CURRENT_SOURCE_DIR}/backends)
