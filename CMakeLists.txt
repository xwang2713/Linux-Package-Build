project (Linux_Package)
cmake_minimum_required (VERSION 2.8)
 
set(VERSION "1.0.0")

set (BIN_DIR "bin")
set (UTILS_DIR "utils")
set (INSTALL_DIR "/opt/LP")

add_subdirectory ( bin )
add_subdirectory ( utils )

set(CPACK_PACKAGE_VERSION ${VERSION})
set(CPACK_GENERATOR "RPM")
set(CPACK_PACKAGE_NAME "Linux_package")
set(CPACK_PACKAGE_RELEASE 1)
set(CPACK_PACKAGE_CONTACT "Xiaoming Wang")
set(CPACK_PACKAGE_VENDOR "LexisNexis")
set(CPACK_INSTALL_PREFIX "${INSTALL_DIR}")
set(CPACK_PACKAGING_INSTALL_PREFIX "${CPACK_INSTALL_PREFIX}")
set(CPACK_PACKAGE_FILE_NAME "${CPACK_PACKAGE_NAME}-${CPACK_PACKAGE_VERSION}-${CPACK_PACKAGE_RELEASE}.${CMAKE_SYSTEM_PROCESSOR}")
include(CPack)

