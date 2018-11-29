cmake_minimum_required(VERSION 3.9)
project(sphgeom)

set(CMAKE_MODULE_PATH
	${CMAKE_SOURCE_DIR}/cmake
)

set(MY_INCLUDE_DIRS
	${CMAKE_CURRENT_SOURCE_DIR}/include
)

set(SOURCES_CPP
	src/Angle.cc
	src/AngleInterval.cc
	src/BigInteger.cc
	src/Box3d.cc
	src/Box.cc
	src/Chunker.cc
	src/Circle.cc
	src/ConvexPolygon.cc
	src/ConvexPolygonImpl.h
	src/Ellipse.cc
	src/HtmPixelization.cc
	src/Interval1d.cc
	src/LonLat.cc
	src/Matrix3d.cc
	src/Mq3cPixelization.cc
	src/NormalizedAngle.cc
	src/NormalizedAngleInterval.cc
	src/orientation.cc
	src/PixelFinder.h
	src/Q3cPixelization.cc
	src/Q3cPixelizationImpl.h
	src/RangeSet.cc
	src/Region.cc
	src/UnitVector3d.cc
	src/utils.cc
	src/Vector3d.cc
)

add_library(${PROJECT_NAME} ${SOURCES_CPP})
target_include_directories(${PROJECT_NAME} PUBLIC ${MY_INCLUDE_DIRS})
