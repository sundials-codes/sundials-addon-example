cmake_minimum_required (VERSION 3.10)
project (test-an-addon)

# add_library(my_sundials_nvector myNVector.c)
# target_link_libraries(my_sundials_nvector PUBLIC sundials_core m)

# Create the sundials_nvecserial library
sundials_add_library(my_sundials_nvector
  SOURCES
    myNVector.c
  HEADERS
    myNVector.h
  INCLUDE_SUBDIR
    nvector
  LINK_LIBRARIES
    PUBLIC sundials_core
  OUTPUT_NAME
    my_sundials_nvector
)