# GLFW
set(GLFW_LIB_NAME "glfw")
set(GLFW_INC_PATH ${GLFW_LIB_NAME}/include)

set(GLFW_BUILD_DOCS     OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS    OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL        OFF CACHE BOOL "" FORCE)

add_subdirectory(${GLFW_LIB_NAME})

#GLAD
add_subdirectory(../external/glad ${CMAKE_CURRENT_BINARY_DIR}/glad)

# GLM
set(GLM_LIB_NAME "glm")
set(GLM_MASTER_PROJECT OFF CACHE BOOL "" FORCE)
add_subdirectory(${GLM_LIB_NAME})
