cmake_minimum_required(VERSION 3.10)
project(RayTracingProject)

# Establece la versión del estándar C++
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Agrega el archivo fuente principal que se encuentra en la carpeta scr
add_executable(${PROJECT_NAME} src/main.cpp)

# Busca y enlaza la librería Vulkan
find_package(Vulkan REQUIRED)
target_link_libraries(${PROJECT_NAME} Vulkan::Vulkan)
