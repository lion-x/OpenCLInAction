cmake_minimum_required(VERSION 3.8)
project(OpenCLInAction)
find_package(OpenCL REQUIRED)
message(STATUS "OpenCL found: ${OPENCL_FOUND}")


set(CMAKE_CXX_STANDARD 11)

add_executable(map_copy ch03/map_copy/map_copy.c)
target_link_libraries(map_copy ${OpenCL_LIBRARIES})

add_executable(hello_kernel ch04/hello_kernel/hello_kernel.c)
target_link_libraries(hello_kernel ${OpenCL_LIBRARIES})

add_executable(double_test ch04/double_test/double_test.c)
target_link_libraries(double_test ${OpenCL_LIBRARIES})

add_executable(float_config ch04/float_config/float_config.c)
target_link_libraries(float_config ${OpenCL_LIBRARIES})

add_executable(vector_widths ch04/vector_widths/vector_widths.c)
target_link_libraries(vector_widths ${OpenCL_LIBRARIES})

add_executable(vector_bytes ch04/vector_bytes/vector_bytes.c)
target_link_libraries(vector_bytes ${OpenCL_LIBRARIES})

add_executable(op_test ch05/op_test/op_test.c)
target_link_libraries(op_test ${OpenCL_LIBRARIES})

add_executable(id_check ch05/id_check/id_check.c)
target_link_libraries(id_check ${OpenCL_LIBRARIES})

add_executable(mod_round ch05/mod_round/mod_round.c)
target_link_libraries(mod_round ${OpenCL_LIBRARIES})

add_executable(polar_rect ch05/polar_rect/polar_rect.c)
target_link_libraries(polar_rect ${OpenCL_LIBRARIES})

add_executable(mad_test ch05/mad_test/mad_test.c)
target_link_libraries(mad_test ${OpenCL_LIBRARIES})

add_executable(shuffle_test ch05/shuffle_test/shuffle_test.c)
target_link_libraries(shuffle_test ${OpenCL_LIBRARIES})

add_executable(select_test ch05/select_test/select_test.c)
target_link_libraries(select_test ${OpenCL_LIBRARIES})

add_executable(profile_read ch07/profile_read/profile_read.c)
target_link_libraries(profile_read ${OpenCL_LIBRARIES})

add_executable(profile_items ch07/profile_items/profile_items.c)
target_link_libraries(profile_items ${OpenCL_LIBRARIES})

add_executable(atomic ch07/atomic/atomic.c)
target_link_libraries(atomic ${OpenCL_LIBRARIES})

add_executable(wg_test ch10/wg_test/wg_test.c)
target_link_libraries(wg_test ${OpenCL_LIBRARIES})

add_executable(reduction ch10/reduction/reduction.c)
target_link_libraries(reduction ${OpenCL_LIBRARIES})

add_executable(reduction_complete ch10/reduction_complete/reduction_complete.c)
target_link_libraries(reduction_complete ${OpenCL_LIBRARIES})