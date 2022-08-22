#
# project: fips-zstd
#
cmake_minimum_required(VERSION 2.8)
project(fips-zstd)
# include the fips main cmake file
get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
include("${FIPS_ROOT_DIR}/cmake/fips.cmake")

fips_setup()
fips_begin_lib(zstd)
    fips_dir(src)
    fips_files(zstd.h zstd.c)
fips_end_lib()
fips_finish()


