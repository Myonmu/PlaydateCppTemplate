cmake_minimum_required(VERSION 3.27)
project(PlaydateProj)

set(CMAKE_CXX_STANDARD 20)

set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CONFIGURATION_TYPES "Debug;Release")
set(CMAKE_XCODE_GENERATE_SCHEME TRUE)

# As this is part of the repo, we can't demonstrate this aptly, but for a full
# project, you will want to include this project in order to use the build
# system, which might looks something like this:
#
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/submodules/playdate-cpp)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/submodules/playdate-cpp-extensions)

# Now we can declare our application
add_playdate_application(PlaydateProj)

target_link_libraries(PlaydateProj pdcpp)

# Add its sources, and you're good to go!
file(GLOB_RECURSE PlaydateProj_SRC ${CMAKE_CURRENT_SOURCE_DIR}/cpp/*)
target_sources(PlaydateProj PUBLIC ${PlaydateProj_SRC})
