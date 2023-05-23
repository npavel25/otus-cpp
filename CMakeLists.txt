cmake_minimum_required(VERSION 3.10)


set(BUILD_NUMBER "1" CACHE INTERNAL "Build number")
set(PROJECT_VERSION 0.0.${BUILD_NUMBER})

project(helloworld VERSION ${PROJECT_VERSION})

#find_package(Boost COMPONENTS unti_test_framework REQUIRED)

configure_file(build_number.h.in build_number.h)

add_executable(helloworld_cli test.cpp)

set_target_properties(helloworld_cli PROPERTIES
    CXX_STANDARD 14
    CXX_STANDARD_REQUIRED ON
)


