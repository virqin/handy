cmake_minimum_required(VERSION 3.5)

project(raw-examples)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

if(LINUX)
    set(EPOLL_SOURCE_FILES epoll.cc)
    add_executable(epoll ${EPOLL_SOURCE_FILES})

    target_include_directories(epoll PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
            PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
            )
    target_link_libraries(epoll
            LINK_PRIVATE handy
            )

    set(EPOLL_ET_SOURCE_FILES epoll-et.cc)
    add_executable(epoll ${EPOLL_ET_SOURCE_FILES})

    target_include_directories(epoll-et PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
            PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
            )
    target_link_libraries(epoll-et
            LINK_PRIVATE handy
            )
endif()

if(MACOS)
    set(KQUEUE_SOURCE_FILES kqueue.cc)
    add_executable(kqueue ${KQUEUE_SOURCE_FILES})

    target_include_directories(kqueue PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
            PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
            )
    target_link_libraries(kqueue
            LINK_PRIVATE handy
            )
endif()