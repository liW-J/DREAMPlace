set(OP_NAME nctugr_binary)

set(TARGET_NAME ${OP_NAME})

file(GLOB INSTALL_SRCS "${CMAKE_CURRENT_SOURCE_DIR}/*.py")
install(FILES ${INSTALL_SRCS} DESTINATION thirdparty/DREAMPlace/dreamplace/ops/${TARGET_NAME})
