set(OP_NAME gift_init)

set(TARGET_NAME ${OP_NAME})

set(INCLUDE_DIRS 
  ${CMAKE_CURRENT_SOURCE_DIR}/..
  )

set(LINK_LIBS utility_cxx
  OpenMP::OpenMP_CXX
  )

add_pytorch_extension(${TARGET_NAME}_cpp 
  src/adj_matrix.cpp 
  EXTRA_INCLUDE_DIRS ${INCLUDE_DIRS}
  EXTRA_LINK_LIBRARIES ${LINK_LIBS})

install(TARGETS 
  ${TARGET_NAME}_cpp 
  DESTINATION thirdparty/DREAMPlace/dreamplace/ops/${OP_NAME})

file(GLOB INSTALL_SRCS 
  ${CMAKE_CURRENT_SOURCE_DIR}/*.py
  )
install(FILES ${INSTALL_SRCS} DESTINATION thirdparty/DREAMPlace/dreamplace/ops/${OP_NAME})
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/utils_gpu DESTINATION thirdparty/DREAMPlace/dreamplace/ops/${OP_NAME})
