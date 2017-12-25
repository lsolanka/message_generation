cmake_minimum_required(VERSION 2.8.3)

include(cmake/HunterGate.cmake)
HunterGate(
    URL "https://github.com/lsolanka/hunter/archive/v0.19.210-4.tar.gz"
    SHA1 "2b18594936d8faded8c59b0a33567af47f50bdb4"
)

project(message_generation)

hunter_add_package(ros-catkin)
hunter_add_package(ros-gencpp)
hunter_add_package(ros-geneus)
hunter_add_package(ros-gennodejs)
hunter_add_package(ros-genlisp)
hunter_add_package(ros-genmsg)
hunter_add_package(ros-genpy)

find_package(catkin REQUIRED)

catkin_package(CATKIN_DEPENDS gencpp geneus gennodejs genlisp genmsg genpy)
