cmake_minimum_required(VERSION 3.8.0)
project(imgui)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

file(GLOB SOURCES
  "${PROJECT_SOURCE_DIR}/src/*.h"
  "${PROJECT_SOURCE_DIR}/src/*.cpp"
  "${PROJECT_SOURCE_DIR}/src/**/*.h"
  "${PROJECT_SOURCE_DIR}/src/**/*.cpp"
)

add_library(imgui STATIC ${SOURCES})

target_include_directories(imgui 
  PUBLIC 
    ${PROJECT_SOURCE_DIR}/include
  PRIVATE 
    ${PROJECT_SOURCE_DIR}/src 
    ${PROJECT_SOURCE_DIR}/include/imgui
)
