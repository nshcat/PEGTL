#######################################################################################
## PEGTL CMake Project File
##
## This simple project file makes it easy and clean to include PEGTL in CMake projects
## by either including the repo as git submodule or cloning it into the project tree.
## The resulting folder can be directly used as subproject and defines a variable that
## contains the location of PEGTL header files.
##
## Usage:
## -------
##
## In main project file, before any subprojects that depend on PEGTL:
##    add_subdirectory(pegtl)
##
## In each subproject that uses PEGTL:
##    include_directories(${PEGTL_INCLUDE_DIRS})
##
##

# Version requirement and project info
cmake_minimum_required(VERSION 3.1)
project(pegtl)

## TODO use this with the interface version of this project.
# Require support for at least C++11.
# set_property(TARGET pegtl PROPERTY CXX_STANDARD 11)
# set_property(TARGET pegtl PROPERTY CXX_STANDARD_REQUIRED ON)

# PEGTL is a header-only library. Just export include directory.
set(PEGTL_INCLUDE_DIRS ${CMAKE_CURRENT_SOURCE_DIR} CACHE INTERNAL "")
