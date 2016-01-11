cmake_minimum_required(VERSION 3.0)
project(QRecentFilesMenu LANGUAGES CXX)

find_package(Qt5 REQUIRED COMPONENTS Core Widgets)

add_library(QRecentFilesMenu STATIC "${CMAKE_CURRENT_SOURCE_DIR}/QRecentFilesMenu.cpp")

set_property(TARGET QRecentFilesMenu APPEND
             PROPERTY INTERFACE_INCLUDE_DIRECTORIES "${CMAKE_CURRENT_SOURCE_DIR}")
set_property(TARGET QRecentFilesMenu PROPERTY CXX_STANDARD 14)
target_link_libraries(QRecentFilesMenu Qt5::Core Qt5::Widgets)
