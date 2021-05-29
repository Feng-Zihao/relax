
cmake_minimum_required(VERSION 3.10)
project(Relax CXX)

set(CMAKE_CXX_STANDARD 14)


set(spdlog_DIR ${CMAKE_RPOJECT_DIR}/third_party/spdlog-1.8.5)

find_package(Boost 1.70 REQUIRED COMPONENTS
	date_time filesystem iostreams)

add_subdirectory(third_party/spdlog-1.8.5)
add_subdirectory(third_party/libuv-1.41.0)


include_directories(${Boost_INCLUDE_DIRS})
link_directories(${Boost_LIBRARY_DIRS})


