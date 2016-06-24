cmake_minimum_required(VERSION 3.5)

project(handy)


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
else()
    set(PLATFORM OS_LINUX)
    add_definitions(
            -DOS_LINUX
    )
endif()


file(GLOB HEADERS "*.h")

file(GLOB SOURCES "*.cc")

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/)

add_library(handy ${SOURCES} ${HEADERS})


#target_include_directories(handy
#	PRIVATE $<TARGET_PROPERTY:scl,INTERFACE_INCLUDE_DIRECTORIES>
#	)

#install(TARGETS 
#		handy
#		ARCHIVE DESTINATION ${INSTALL_LIB_DIR}
#		LIBRARY DESTINATION ${INSTALL_LIB_DIR}
#		)

