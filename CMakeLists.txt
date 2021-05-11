#
# project: fips_pystring
#
if (NOT FIPS_IMPORT)
    cmake_minimum_required(VERSION 2.8)
    get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
    include("${FIPS_ROOT_DIR}/cmake/fips.cmake")
    fips_setup()
    fips_project(fips-pystring)
endif()

fips_begin_lib(pystring)
    fips_dir(pystring GROUP .)
    fips_files(pystring.cpp pystring.h)
fips_end_lib()
target_include_directories(pystring PUBLIC pystring)

if (NOT FIPS_IMPORT)
    fips_finish()
endif()
