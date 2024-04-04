cmake_minimum_required(VERSION 3.22.0)

set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON)

project(workbench VERSION 1.0.0)

# Using INTERFACE for header only library
add_library(workbench INTERFACE)

# Giving scope to files inside library
target_include_directories(workbench INTERFACE $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>)