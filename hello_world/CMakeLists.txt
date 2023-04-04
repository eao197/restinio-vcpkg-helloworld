set(PRJ hello_world)

project(${PRJ} CXX)

add_executable(${PRJ} main.cpp)
target_link_libraries(${PRJ} PRIVATE restinio::restinio)

if (WIN32)
	target_link_libraries(${PRJ} PRIVATE wsock32 ws2_32)
endif ()

install(
	TARGETS ${PRJ}
	RUNTIME DESTINATION bin
)
