cmake_minimum_required(VERSION 3.22)
project(tetr)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_EXE_LINKER_FLAGS "-static -static-libgcc")
set(SFML_STATIC_LIBRARIES TRUE)

add_executable(tetr WIN32 main.cpp)

set(SFML_DIR "C:\\Users\\japanbot\\CLionProjects\\lip\\sfml\\SFML-2.5.1-windows-vc15-64-bit\\SFML-2.5.1\\lib\\cmake\\SFML")

target_link_libraries(tetr sfml-graphics)

set(CMAKE_MODULE_PATH "${CMAKE_CURRENT_LIST_DIR}/cmake_modules")
find_package(SFML 2.5 REQUIRED graphics network audio window system)
