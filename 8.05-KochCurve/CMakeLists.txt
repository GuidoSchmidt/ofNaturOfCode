project(ofNOC-8.05-KochCurve)
set(APP ofNOC-8.06-KochCurve)

cmake_minimum_required(VERSION 2.8)

# C++ 11 support
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

include(../../of/openFrameworks.cmake)

ofxaddon(ofxGui)

set(SOURCES
    src/main.cpp
    src/ofApp.cpp
    src/KochCurve.cpp
)

add_executable(
    ${APP}
    MACOSX_BUNDLE
    ${SOURCES}
    ${OFXADDONS_SOURCES}
)

target_link_libraries(
    ${APP}
    ${OPENFRAMEWORKS_LIBRARIES}
)

cotire(${APP})
