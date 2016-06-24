cmake_minimum_required(VERSION 3.5)

project(handyall)


set(CMAKE_EXPORT_COMPILE_COMMANDS 1)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -std=c++11")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(CMAKE_C_FLAGS_DEBUG "${CMAKE_C_FLAGS_DEBUG} -pthread -Wall -O2")
set(CMAKE_C_FLAGS_RELEASE "${CMAKE_C_FLAGS_RELEASE} -pthread -Wall -O2 -DNDEBUG")

set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -pthread -Wall -O2")
set(CMAKE_CXX_FLAGS_RELEASE "${CMAKE_CXX_FLAGS_RELEASE} -pthread -Wall -O2 -DNDEBUG")


if(ANDROID)
    set(PLATFORM OS_ANDROID)
    add_definitions(
            -DOS_ANDROID
    )
elseif(LINUX)
    set(PLATFORM OS_LINUX)
    add_definitions(
            -DOS_LINUX
    )
endif()



add_subdirectory(handy)
#add_subdirectory(test)
add_subdirectory(examples)
add_subdirectory(raw-examples)
add_subdirectory(10m)