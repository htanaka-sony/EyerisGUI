cmake_minimum_required(VERSION 3.19)

# Version指定
project(EyerisGUI VERSION 1.0.0)

set(CMAKE_CXX_STANDARD 20)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin) # exeやDLLの出力先
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin) # DLLの出力先
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib) # 静的ライブラリの出力先

# モジュールパス
set(OUTPUT_DIR "${CMAKE_RUNTIME_OUTPUT_DIRECTORY}")

include(3DViewer/CMakeUtils/UtilityFunction.cmake)
include(3DViewer/CMakeUtils/QtUtil.cmake)
include(3DViewer/CMakeUtils/3DViewerUtil.cmake)

add_subdirectory(EyerisProject)
add_subdirectory(3DViewer)
