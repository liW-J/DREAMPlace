set(OP_NAME pin_weight_sum)

set(TARGET_NAME pws)

set(INCLUDE_DIRS
  ${CMAKE_CURRENT_SOURCE_DIR}/..
  )

set(LINK_LIBS utility_cxx
  OpenMP::OpenMP_CXX
  )

add_pytorch_extension(${TARGET_NAME}_cpp
  src/pws.cpp
  EXTRA_INCLUDE_DIRS ${INCLUDE_DIRS}
  EXTRA_LINK_LIBRARIES ${LINK_LIBS})

install(TARGETS
  ${TARGET_NAME}_cpp
  DESTINATION thirdparty/DREAMPlace/dreamplace/ops/${OP_NAME})

if(TORCH_ENABLE_CUDA)
add_pytorch_extension(${TARGET_NAME}_cuda
  src/pws_cuda.cpp
  src/pws_cuda_kernel.cu
  EXTRA_INCLUDE_DIRS ${INCLUDE_DIRS}
  EXTRA_LINK_LIBRARIES ${LINK_LIBS})

install(TARGETS
  ${TARGET_NAME}_cuda
  DESTINATION thirdparty/DREAMPlace/dreamplace/ops/${OP_NAME})
endif(TORCH_ENABLE_CUDA)

file(GLOB INSTALL_SRCS ${CMAKE_CURRENT_SOURCE_DIR}/*.py)
install(FILES ${INSTALL_SRCS} DESTINATION thirdparty/DREAMPlace/dreamplace/ops/${OP_NAME})
