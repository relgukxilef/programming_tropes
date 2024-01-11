cmake_minimum_required(VERSION 3.16)

project(programming_tropes LANGUAGES CXX C)

add_executable(programming_tropes main.cpp)
target_link_libraries(programming_tropes PUBLIC cppcms)

add_subdirectory(submodules/cppcms)
target_include_directories(cppcms PUBLIC submodules/cppcms)
target_include_directories(cppcms PUBLIC submodules/cppcms/booster)
target_include_directories(cppcms PUBLIC ${CMAKE_BINARY_DIR}/submodules/cppcms)
target_include_directories(cppcms PUBLIC ${CMAKE_BINARY_DIR}/submodules/cppcms/booster)