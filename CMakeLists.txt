cmake_minimum_required(VERSION 3.23 FATAL_ERROR)

project(BattleCity LANGUAGES CXX)
set(CMAKE_CXX_STANDARD 23) #версія стандарта C++23 

add_executable(
	BattleCity 
	src/main.cpp
)