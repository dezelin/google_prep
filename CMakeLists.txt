#
#  This file is part of google_prep.
#
#  google_prep is free software: you can redistribute it and/or modify
#
#  it under the terms of the GNU General Public License as published by
#  the Free Software Foundation, either version 3 of the License, or
#  (at your option) any later version.
#
#  google_prep is distributed in the hope that it will be useful,
#  but WITHOUT ANY WARRANTY; without even the implied warranty of
#  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
#  GNU General Public License for more details.
#
#  You should have received a copy of the GNU General Public License
#  along with google_prep.  If not, see <http://www.gnu.org/licenses/>.
#

cmake_minimum_required (VERSION 2.8) 
project (google_prep) 

if (CMAKE_BINARY_DIR STREQUAL ${CMAKE_SOURCE_DIR})
    message(FATAL_ERROR "type: git clean -df && mkdir build && cd build && cmake .. && make")
endif()

if (CMAKE_BUILD_TYPE MATCHES Debug)
    set(CMAKE_VERBOSE_MAKEFILE 1)
else ()
    set(CMAKE_VERBOSE_MAKEFILE 0)
endif ()

add_definitions ("-Wall -std=c++11")

add_subdirectory (3rd_party/gtest-1.6.0)
add_subdirectory (algo) 
add_subdirectory (struct)

enable_testing ()
