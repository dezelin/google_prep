
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
project (struct) 

add_library (struct placeholder.cc)

enable_testing ()

include_directories (${gtest_SOURCE_DIR}/include ${gtest_SOURCE_DIR})

add_executable (struct_placeholder_test placeholder_test.cc)
target_link_libraries (struct_placeholder_test gtest gtest_main struct)
add_test (placeholder_test struct_placeholder_test)
