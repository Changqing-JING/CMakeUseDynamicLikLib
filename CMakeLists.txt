cmake_minimum_required(VERSION 3.5)
project(use_dynamic_lib)

find_package(lib1 REQUIRED)


aux_source_directory(./src sourceFiles)


add_executable(${PROJECT_NAME} ${sourceFiles})

message(---------${LIB1_LIBRARIES}----------)
message(----------${LIB1_INCLUDE_DIRS}--------------)

target_link_libraries(${PROJECT_NAME} lib1)