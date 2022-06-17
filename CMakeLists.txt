cmake_minimum_required(VERSION 3.23 FATAL_ERROR)

set(PROJECT_NAME BattleCity)
project(${PROJECT_NAME} LANGUAGES CXX)
set(CMAKE_CXX_STANDARD 23) #версія стандарта C++23 

add_executable(
	${PROJECT_NAME} 
	src/main.cpp
)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw)
target_link_libraries(${PROJECT_NAME} GLFW3)

include_directories(external/glfw/include)

add_subdirectory(external/glad)
target_link_libraries(${PROJECT_NAME} glad)