cmake_minimum_required (VERSION 3.10)
project (test-an-addon)

add_library(my_sundials_nvector myNVector.c)
target_link_libraries(my_sundials_nvector PUBLIC sundials_core m)

