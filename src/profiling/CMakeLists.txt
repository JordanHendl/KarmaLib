# 
# Copyright (C) 2020 Jordan Hendl
# 
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
# 
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
# 
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <http://www.gnu.org/licenses/>.
# 

SET( IRIS_PROFILING_SOURCES 
     Timer.cpp
   )
      
SET( IRIS_PROFILING_HEADERS
     Timer.h
   )

SET( IRIS_PROFILING_INCLUDES
   )

SET( IRIS_PROFILING_LIBRARIES
    )

ADD_LIBRARY( iris_profiling SHARED ${IRIS_PROFILING_SOURCES} ${IRIS_PROFILING_HEADERS} )

BUILD_TEST( TARGET iris_profiling )
INSTALL( FILES ${IRIS_PROFILING_HEADERS} DESTINATION ${HEADER_INSTALL_DIR}/profiling )
INSTALL( TARGETS iris_profiling EXPORT Iris 
                 LIBRARY  DESTINATION ${EXPORT_LIB_DIR} 
                 RUNTIME  DESTINATION ${EXPORT_LIB_DIR}
                 ARCHIVE  DESTINATION ${EXPORT_LIB_DIR}
                 INCLUDES DESTINATION ${EXPORT_INCLUDE_DIR} )