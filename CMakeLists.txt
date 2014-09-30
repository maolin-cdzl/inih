CMAKE_MINIMUM_REQUIRED(VERSION 2.8.12)

project(inih C)

include(CMakeStdOpt)

set(HEADERS include/inih/ini.h)

set(SOURCES ini.c)

add_library(inih STATIC ${SOURCES} ${HEADERS})

target_include_directories(inih
	PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include
	PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include/inih
	)

