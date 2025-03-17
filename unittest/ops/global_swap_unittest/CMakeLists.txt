
file(GLOB INSTALL_SRCS "${CMAKE_CURRENT_SOURCE_DIR}/*.py")
install(
    FILES ${INSTALL_SRCS} DESTINATION thirdparty/DREAMPlace/unittest/ops/global_swap_unittest
    )
