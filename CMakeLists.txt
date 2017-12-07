cmake_minimum_required(VERSION 2.8.3)

include(cmake/HunterGate.cmake)
HunterGate(
    URL "https://github.com/lsolanka/hunter/archive/4ecf66e071495981031fdfa99aad576405537266.tar.gz"
    SHA1 "727648f578f3cbcb6ea0e644bd8b0111e56688bc"
    LOCAL
)

project(message_generation)

hunter_add_package(catkin)
hunter_add_package(gencpp)
hunter_add_package(geneus)
hunter_add_package(gennodejs)
hunter_add_package(genlisp)
hunter_add_package(genmsg)
hunter_add_package(genpy)

find_package(catkin REQUIRED)

catkin_package(CATKIN_DEPENDS gencpp geneus gennodejs genlisp genmsg genpy)
