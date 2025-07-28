cmake_minimum_required(VERSION 3.10)
project(NQueenSolver)

set(CMAKE_CXX_STANDARD 11)

# Tell CMake to find FLTK (used by GitHub workflow with -DCMAKE_PREFIX_PATH)
find_package(FLTK REQUIRED NO_MODULE)

add_executable(nqueen main.cpp)

# Required for image handling (Fl_PNG_Image)
target_link_libraries(nqueen
    fltk
    fltk_images
    comctl32
    ole32
    uuid
    ws2_32
)
