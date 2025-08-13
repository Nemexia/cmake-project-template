cmake_minimum_required(VERSION 3.15...4.0)

project(
  MyProject
  VERSION 0.1.0
  DESCRIPTION "CMake Project Template"
  LANGUAGES CXX)

add_library(mylib STATIC src/mylib.cpp include/my/lib.hpp)
target_include_directories(mylib PUBLIC include)
target_compile_features(mylib PUBLIC cxx_std_20)

add_executable(my apps/my.cpp)
target_link_libraries(my PUBLIC mylib)
