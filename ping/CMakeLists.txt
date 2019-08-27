project(cping)
CMAKE_MINIMUM_REQUIRED(VERSION 2.8)
MESSAGE(STATUS "#########################")
SET(CMAKE_BUILD_TYPE Release)
ADD_DEFINITIONS(-std=c++11 -g -Wall )

SET(EXTRA_INC_DIR /home/ext)

INCLUDE_DIRECTORIES( 
					/usr/local/include
					
					)


				


LINK_DIRECTORIES(
				/usr/local/lib 
				/usr/local/lib64
				/usr/lib64/mysql/
				/usr/lib/x86_64-linux-gnu

				)
				
				
file(GLOB ALL_CXX_SRCS
                       ./*.cpp  ./*.cc
)

add_executable(${PROJECT_NAME} ${ALL_CXX_SRCS})


set(ALL_LIB  	pthread
				)


target_link_libraries(${PROJECT_NAME} ${ALL_LIB})