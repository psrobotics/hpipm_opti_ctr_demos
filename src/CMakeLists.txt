macro(add_example EXAMPLE)
  add_executable(
    ${EXAMPLE} 
    ${EXAMPLE}/${EXAMPLE}.cpp
  )
  target_include_directories(
    ${EXAMPLE} 
    PRIVATE
    ${EIGEN_INCLUDE_DIR}
    ${hpipm-cpp_INCLUDE_DIR}
  )
  target_link_libraries(
    ${EXAMPLE} 
    PRIVATE
    hpipm-cpp::hpipm-cpp
  )
endmacro()

# build all targets
foreach(demos qp_mpc qp_test)

  add_example(${demos})

endforeach()
