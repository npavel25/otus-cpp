cmake_minimum_required(VERSION 3.10)

project(helloworld)

#find_package(Boost COMPONENTS unti_test_framework REQUIRED)

configure_file(build_number.h.in build_number.h)

add_executable(helloworld_cli test.cpp)

set_target_properties(helloworld_cli PROPERTIES
    CXX_STANDARD 14
    CXX_STANDARD_REQUIRED ON
)


