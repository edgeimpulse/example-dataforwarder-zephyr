cmake_minimum_required(VERSION 3.13.1)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# This sample is specific to x_nucleo_iks02a1 shield. Enforce -DSHIELD option
set(SHIELD x_nucleo_iks02a1_shub)

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})

project(example-dataforwarder-zephyr)

# Needed for colorful output
zephyr_compile_options(-fdiagnostics-color=always)

target_sources(app PRIVATE src/main.cpp)
