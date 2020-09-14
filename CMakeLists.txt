
CMAKE_MINIMUM_REQUIRED(VERSION 3.10)

PROJECT(mockcpp VERSION 1.0.0)

INCLUDE(ProjectVar.txt)

ADD_SUBDIRECTORY(src)

INSTALL(DIRECTORY include/mockcpp DESTINATION include
        PATTERN ".svn" EXCLUDE)

INSTALL(DIRECTORY 3rdparty/boost DESTINATION include
        PATTERN ".svn" EXCLUDE)

SET(MOCKCPP_XUNIT "testngpp" CACHE STRING "Set to gtest/cpputest/cppunit to use other testframeworks.")


