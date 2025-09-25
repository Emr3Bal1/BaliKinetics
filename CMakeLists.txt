cmake_minimum_required(VERSION 3.16)

project(BaliKinetics
    VERSION 0.1.0
    DESCRIPTION "Kinematics + RRT sandbox"
    LANGUAGES CXX
)

# C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# ---- kinematics library ----
add_library(kinematics
    src/kinematics/Robot2D.cpp
)

target_include_directories(kinematics PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)

# ---- demo executable ----
add_executable(kinematics_demo
    src/examples/kinematics_demo.cpp
)
target_link_libraries(kinematics_demo PRIVATE kinematics)


# 6-DOF MANIPULATOR KINEMATIK
TARGET_SOURCES(KINEMATICS PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/SRC/KINEMATICS/SERIAL6DOF.CPP
)

# DEMO
ADD_EXECUTABLE(SERIAL6DOF_DEMO
    ${CMAKE_CURRENT_SOURCE_DIR}/SRC/EXAMPLES/SERIAL6DOF_DEMO.CPP
)
TARGET_LINK_LIBRARIES(SERIAL6DOF_DEMO PRIVATE KINEMATICS)


# Ýleride:
# add_library(planning src/planning/RRT.cpp)
# add_executable(rrt_demo src/examples/rrt_demo.cpp)
