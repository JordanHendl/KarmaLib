SET( IRIS_LOG_SOURCES 
     Log.cpp
   )
      
SET( IRIS_LOG_HEADERS
     Log.h
   )

SET( IRIS_LOG_INCLUDES
   )

SET( IRIS_LOG_LIBRARIES
    )

ADD_LIBRARY( iris_log SHARED ${IRIS_LOG_SOURCES} ${IRIS_LOG_HEADERS} )

BUILD_TEST( TARGET iris_log )

INSTALL( FILES   ${IRIS_LOG_HEADERS}  DESTINATION ${HEADER_INSTALL_DIR}/log )
INSTALL( TARGETS iris_log EXPORT Iris
                 RUNTIME  DESTINATION ${EXPORT_LIB_DIR}
                 LIBRARY  DESTINATION ${EXPORT_LIB_DIR} 
                 ARCHIVE  DESTINATION ${EXPORT_LIB_DIR}
                 INCLUDES DESTINATION ${EXPORT_INCLUDE_DIR} )
