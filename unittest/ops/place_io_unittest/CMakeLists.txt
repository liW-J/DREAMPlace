set(OP_NAME place_io_unittest)

file(GLOB INSTALL_SRCS "${CMAKE_CURRENT_SOURCE_DIR}/*.py")
install(
    FILES ${INSTALL_SRCS} DESTINATION thirdparty/DREAMPlace/unittest/ops/${OP_NAME}
    )
install(
    DIRECTORY simple DESTINATION thirdparty/DREAMPlace/unittest/ops/${OP_NAME}
    )
install(
    FILES simple.golden DESTINATION thirdparty/DREAMPlace/unittest/ops/${OP_NAME}
    )
