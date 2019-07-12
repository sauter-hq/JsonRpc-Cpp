ADD_EXECUTABLE(system system.cpp)
TARGET_LINK_LIBRARIES(system jsonrpc ) 

ADD_EXECUTABLE(tcp-server tcp-server.cpp test-rpc.cpp)
TARGET_LINK_LIBRARIES(tcp-server jsonrpc)

ADD_EXECUTABLE(tcp-client tcp-client.cpp test-rpc.cpp)
TARGET_LINK_LIBRARIES(tcp-client jsonrpc)

ADD_EXECUTABLE(udp-server udp-server.cpp test-rpc.cpp)
TARGET_LINK_LIBRARIES(udp-server jsonrpc)

ADD_EXECUTABLE(udp-client udp-client.cpp test-rpc.cpp)
TARGET_LINK_LIBRARIES(udp-client jsonrpc)
