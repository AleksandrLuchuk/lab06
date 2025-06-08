cmake_minimum_required(VERSION 3.5)
project(solver_app)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(equation equation.cpp)


target_include_directories(equation PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib
    ${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib
)


target_link_libraries(equation
    formatter_ex
    solver_lib
)

install(TARGETS equation DESTINATION bin)
