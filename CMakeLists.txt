cmake_minimum_required(VERSION 3.0)
project(GameOfLife)

# Find ncurses library
find_package(Curses REQUIRED)
include_directories(${CURSES_INCLUDE_DIR})

# Add executable
add_executable(GameOfLife game_of_life.cpp)

# Link ncurses library
target_link_libraries(GameOfLife ${CURSES_LIBRARIES})
