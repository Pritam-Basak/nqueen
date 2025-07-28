cmake_minimum_required(VERSION 3.10)
project(NQueenApp)

set(CMAKE_CXX_STANDARD 11)

# FLTK setup
find_package(FLTK REQUIRED NO_MODULE)

add_executable(nqueen main.cpp)
target_link_libraries(nqueen fltk fltk_images comctl32 ws2_32 ole32 uuid)
