cmake_minimum_required(VERSION 3.5)

project(10m)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")


set(10M_CLI_SOURCE_FILES 10m-cli.cc)
add_executable(10m-cli ${10M_CLI_SOURCE_FILES})

target_include_directories(10m-cli PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(10m-cli
        LINK_PRIVATE handy
        )

set(10M_SVR_SOURCE_FILES 10m-svr.cc)
add_executable(10m-svr ${10M_SVR_SOURCE_FILES})

target_include_directories(10m-svr PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(10m-svr
        LINK_PRIVATE handy
        )
