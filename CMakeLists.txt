project (rope)
cmake_minimum_required (VERSION 3.3)

add_library (rope OBJECT
	src/node.cpp
	src/rope.cpp
)

target_include_directories (rope PUBLIC
	"${CMAKE_CURRENT_SOURCE_DIR}/include"
)

target_compile_features (rope PUBLIC
	cxx_std_14
)

if (BUILD_TESTING)
	enable_testing()
	add_subdirectory (${CMAKE_SOURCE_DIR}/3rdparty 3rdparty)
	add_subdirectory (tests)
endif ()
