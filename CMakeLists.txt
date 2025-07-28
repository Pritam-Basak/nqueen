cmake_minimum_required(VERSION 3.10)
project(NQueenSolver)

set(CMAKE_CXX_STANDARD 11)

# Include FLTK
set(FLTK_SKIP_FLUID TRUE)
find_package(FLTK REQUIRED NO_MODULE)

add_executable(nqueen main.cpp)

# Link required FLTK libs
target_link_libraries(nqueen
    fltk
    fltk_images
    comctl32
    ole32
    uuid
    ws2_32
)
