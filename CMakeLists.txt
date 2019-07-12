cmake_minimum_required (VERSION 2.6)
project (jsonrpc-cpp)

# External dependencies retrieval
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/Modules/")

# Define Executable Output Directory
set (EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR})

# Include our configuration header
include_directories(${CMAKE_SOURCE_DIR}/src)

# Build the different applications
add_subdirectory (src)
add_subdirectory (test)
add_subdirectory (examples)
