cmake_minimum_required(VERSION 3.1)
project(collective Fortran)

find_package(MPI REQUIRED)

file(GLOB SRC_FILES ${CMAKE_SOURCE_DIR}/Source/collective.cuf)

include_directories(${MPI_Fortran_INCLUDE_PATH})

# Let CMake know .cuf is a Fortran file
set_source_files_properties(${SRC_FILES} PROPERTIES LANGUAGE Fortran)

set(CUSTOM_CMAKE_Fortran_FLAGS "" CACHE STRING "User defined Fortran flags")
set(CMAKE_Fortran_FLAGS "${CMAKE_Fortran_FLAGS} ${CUSTOM_CMAKE_Fortran_FLAGS}")

add_executable(Collective ${SRC_FILES})

target_link_libraries(Collective ${MPI_Fortran_LIBRARIES})
