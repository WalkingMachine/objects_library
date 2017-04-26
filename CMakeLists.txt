cmake_minimum_required(VERSION 2.8)
project(object_library)

find_package(catkin REQUIRED ecto)

catkin_package()

# build the docs
ecto_sphinx(${CMAKE_CURRENT_SOURCE_DIR}/doc/source doc)

# install the data
install(DIRECTORY data
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
