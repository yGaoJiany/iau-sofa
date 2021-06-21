cmake_minimum_required(VERSION 3.4)

set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS YES CACHE BOOL "Export all symbols")
project (sofa)

include_directories(src)

FILE(GLOB SC_FILES "src/*.c" "src/*.h")

add_library(${PROJECT_NAME} SHARED ${SC_FILES})

# package information
set (CPACK_PACKAGE_VERSION_MAJOR    1)
set (CPACK_PACKAGE_VERSION_MINOR    1)
set (CPACK_PACKAGE_VERSION_PATCH    1)
