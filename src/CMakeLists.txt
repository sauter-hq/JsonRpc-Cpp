find_package(Threads REQUIRED)
find_package(CURL REQUIRED)

# Source files to compile with executable
file(GLOB_RECURSE LIBJSONRPC-CPP_SOURCE_FILES "*.cpp")

ADD_LIBRARY(jsonrpc SHARED ${LIBJSONRPC-CPP_SOURCE_FILES})
TARGET_LINK_LIBRARIES(jsonrpc jsoncpp ${CMAKE_THREAD_LIBS_INIT} ${CURL_LIBRARIES})
SET_TARGET_PROPERTIES(jsonrpc PROPERTIES VERSION 0.0.4 SOVERSION 0.0.4)

# Install instructions for this target
INSTALL(TARGETS jsonrpc
  RUNTIME DESTINATION bin
  LIBRARY DESTINATION lib
  ARCHIVE DESTINATION lib
)

# Install headers
file(GLOB INCLUDE_FILES "*.h")
INSTALL(FILES ${INCLUDE_FILES} DESTINATION include/jsonrpc) 
