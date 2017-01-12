CMAKE_MINIMUM_REQUIRED ( VERSION 2.6 )
project( TPAvion )

file( GLOB_RECURSE
source_files
src/*)

set (OSG_LIBRARY "/home/user/Téléchargements/OpenSceneGraph-3.2.1/src")

set(CMAKE_MODULE_PATH "/usr/share/cmake-2.8/Modules")
message("CMAKE_MODULE_PATH=${CMAKE_MODULE_PATH}")

find_package(OpenSceneGraph)
#find_package ( OpenSceneGraph 2.0.0 REQUIRED osgDB osgViewer osgUtil)
set(OPENSCENEGRAPH_INCLUDE_DIRS "/home/user/Téléchargements/OpenSceneGraph-3.2.1/include")
INCLUDE_DIRECTORIES(${OPENSCENEGRAPH_INCLUDE_DIRS})

add_executable ( TPAvion ${source_files} )

TARGET_LINK_LIBRARIES(TPAvion ${OPENSCENEGRAPH_LIBRARIES})

include_directories ( include )
