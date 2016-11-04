#######################################################################################
## PEGTL CMake Project File
##

# Version requirement and project info
cmake_minimum_required(VERSION 3.1)
project(pegtl)

# Define pegtl as header only interface
add_library(pegtl INTERFACE)

# Add header files als interface dependencies
target_include_directories(pegtl INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})

# Require support for at least C++11.
set_property(TARGET pegtl PROPERTY CXX_STANDARD 11)
set_property(TARGET pegtl PROPERTY CXX_STANDARD_REQUIRED ON)

set(PEGTL_LIBRARIES pegtl CACHE INTERNAL "")
