cmake_minimum_required(VERSION 3.5)

project(examples)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")


set(CHAT_SOURCE_FILES chat.cc)
add_executable(chat ${CHAT_SOURCE_FILES})

target_include_directories(chat PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(chat
        LINK_PRIVATE handy
        )

set(CODEC_CLI_SOURCE_FILES codec-cli.cc)
add_executable(codec-cli ${CODEC_CLI_SOURCE_FILES})
target_include_directories(codec-cli PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(codec-cli
        LINK_PRIVATE handy
        )

set(CODEC_SVR_SOURCE_FILES codec-svr.cc)
add_executable(codec-svr ${CODEC_SVR_SOURCE_FILES})
target_include_directories(codec-svr PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(codec-svr
        LINK_PRIVATE handy
        )

set(DAEMON_SOURCE_FILES daemon.cc)
add_executable(daemon ${DAEMON_SOURCE_FILES})
target_include_directories(daemon PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(daemon
        LINK_PRIVATE handy
        )

set(ECHO_SOURCE_FILES echo.cc)
add_executable(echo ${ECHO_SOURCE_FILES})
target_include_directories(echo PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(echo
        LINK_PRIVATE handy
        )

set(HSHA_SOURCE_FILES hsha.cc)
add_executable(hsha ${HSHA_SOURCE_FILES})
target_include_directories(hsha PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(hsha
        LINK_PRIVATE handy
        )

set(HTTP_HELLO_SOURCE_FILES http-hello.cc)
add_executable(http-hello ${HTTP_HELLO_SOURCE_FILES})
target_include_directories(http-hello PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(http-hello
        LINK_PRIVATE handy
        )

set(IDLE_CLOSE_SOURCE_FILES idle-close.cc)
add_executable(idle-close ${IDLE_CLOSE_SOURCE_FILES})
target_include_directories(idle-close PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(idle-close
        LINK_PRIVATE handy
        )

set(RECONNECT_SOURCE_FILES reconnect.cc)
add_executable(reconnect ${RECONNECT_SOURCE_FILES})
target_include_directories(reconnect PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(reconnect
        LINK_PRIVATE handy
        )

set(SAFE_CLOSE_SOURCE_FILES safe-close.cc)
add_executable(safe-close ${SAFE_CLOSE_SOURCE_FILES})
target_include_directories(safe-close PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(safe-close
        LINK_PRIVATE handy
        )

set(STAT_SOURCE_FILES stat.cc)
add_executable(stat ${STAT_SOURCE_FILES})
target_include_directories(stat PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(stat
        LINK_PRIVATE handy
        )

set(TIMER_SOURCE_FILES timer.cc)
add_executable(timer ${TIMER_SOURCE_FILES})
target_include_directories(timer PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(timer
        LINK_PRIVATE handy
        )

set(UDP_CLI_SOURCE_FILES udp-cli.cc)
add_executable(udp-cli ${UDP_CLI_SOURCE_FILES})
target_include_directories(udp-cli PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(udp-cli
        LINK_PRIVATE handy
        )

set(UDP_HSHA_SOURCE_FILES udp-hsha.cc)
add_executable(udp-hsha ${UDP_HSHA_SOURCE_FILES})
target_include_directories(udp-hsha PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(udp-hsha
        LINK_PRIVATE handy
        )

set(UDP_SVR_SOURCE_FILES udp-svr.cc)
add_executable(udp-svr ${UDP_SVR_SOURCE_FILES})
target_include_directories(udp-svr PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(udp-svr
        LINK_PRIVATE handy
        )

set(WRITE_ON_EMPTY_SOURCE_FILES write-on-empty.cc)
add_executable(write-on-empty ${WRITE_ON_EMPTY_SOURCE_FILES})
target_include_directories(write-on-empty PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../
        PRIVATE $<TARGET_PROPERTY:handy,INTERFACE_INCLUDE_DIRECTORIES>
        )
target_link_libraries(write-on-empty
        LINK_PRIVATE handy
        )
