cmake_minimum_required(VERSION 3.13)

set(PROJECT_NAME cmake_project_example)
set(CMAKE_CXX_STANDARD 17)

project(${PROJECT_NAME})
add_executable(${PROJECT_NAME} src/main.cpp)

include(Dependency.cmake)

# 프로젝트에 include 및 lib 디렉토리 추가
target_include_directories(${PROJECT_NAME} PUBLIC ${DEP_INCLUDE_DIR})
target_link_directories(${PROJECT_NAME} PUBLIC ${DEP_LIB_DIR})
target_link_libraries(${PROJECT_NAME} PUBLIC ${DEP_LIBS})

add_dependencies(${PROJECT_NAME} ${DEP_LIST})
