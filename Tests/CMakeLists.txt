include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../Source)

set(CHECK_INSTALL_DIR "C:/Program Files (x86)/check")
list(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR})

find_package(Check REQUIRED)
include_directories(${CHECK_INCLUDE_DIRS})
link_directories(${CHECK_LIBRARY_DIRS})

set(TEST_SOURCES
    test.c)

add_executable(options_tests ${TEST_SOURCES})
target_link_libraries(options_tests OptionsParser ${CHECK_LIBRARIES})