# 0.) Create Source and CMakeFile
# 1.) mkdir build
# 2.) cd build
# 3.) cmake ..   -  Generting the Build Files / Configure the Project
# 4.) cmake --build . (Compile all targets)
# 5.) ./Executable

cmake_minimum_required(VERSION 3.22) # CMake Version welche für die Entwicklung benötigt wird

project(CppProjectTemplate VERSION 1.0.0 LANGUAGES C CXX) # Name des Projekts und Version des Programms und die Sprachen die verwendet werden können

# CMake Variablen über die set() Funktion setzen
#          User defined name
#           v          v
set(EXECUTABLE_NAME "Executable") # Name des Executable (In CMake ist alles ein string und kann mit "" oder '' oder ohne geschrieben werden)
set(LIBRARY_NAME "Library") # Name des Library

#          Aufruf der Variable
#                  v
add_library(${LIBRARY_NAME} my_lib.cpp) # Name der Library und die Source Files
add_executable(${EXECUTABLE_NAME} main.cpp) # Name des Executable und die Source Files

# Linking der Library mit dem Executable
target_link_libraries(${EXECUTABLE_NAME} ${LIBRARY_NAME})
