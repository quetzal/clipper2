
set(INCS    ${CMAKE_CURRENT_SOURCE_DIR}/include/)
set (SRCS   ${CMAKE_CURRENT_SOURCE_DIR}/include/clipper2/clipper.h
			${CMAKE_CURRENT_SOURCE_DIR}/include/clipper2/clipper.core.h
			${CMAKE_CURRENT_SOURCE_DIR}/include/clipper2/clipper.engine.h
			${CMAKE_CURRENT_SOURCE_DIR}/include/clipper2/clipper.export.h
			${CMAKE_CURRENT_SOURCE_DIR}/include/clipper2/clipper.minkowski.h
			${CMAKE_CURRENT_SOURCE_DIR}/include/clipper2/clipper.offset.h
			${CMAKE_CURRENT_SOURCE_DIR}/include/clipper2/clipper.rectclip.h
			${CMAKE_CURRENT_SOURCE_DIR}/src/clipper.engine.cpp
			${CMAKE_CURRENT_SOURCE_DIR}/src/clipper.offset.cpp
			${CMAKE_CURRENT_SOURCE_DIR}/src/clipper.rectclip.cpp
			)
__add_real_target(clipper2 lib SOURCE ${SRCS}
								  INC ${INCS}
								INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include/
								)

if(CC_INSTALL_CLIPPER2)
	__install_directory_specif(${CMAKE_CURRENT_SOURCE_DIR}/include/ clipper2)
endif()
