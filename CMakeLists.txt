CMAKE_MINIMUM_REQUIRED(VERSION 3.0.0)
project(SpaceInvaders VERSION 0.1.0)
cmake_policy(SET CMP0072 NEW)

FIND_PACKAGE(OpenGL REQUIRED)

ADD_EXECUTABLE(SpaceInvaders 
    src/main.cpp
    src/glad.h
    src/glad.c
    src/khrplatform.h
    src/stb_image.h
    
    src/cubes.cpp
    src/cubes.h
    src/dRays.cpp
    src/dRays.h
    src/figure.cpp
    src/figure.h
    src/shaderClass.cpp
    src/shaderClass.h

    Headers/AdditionalFunctions.h
    Headers/CubeRepresentation.h
    Headers/Header.h
    Headers/ScrambleSimplifier.h
    Headers/SolvingFunctions.h
    Headers/TestingFunctions.h
)

add_subdirectory(
    /home/angel/Documentos/UCSP/Semestre7/ComputacionGrafica/ArchivosOpenGL/glfw-3.3.8 
    /home/angel/Documentos/UCSP/Semestre7/ComputacionGrafica/ArchivosOpenGL/glfw-3.3.8/src
)

include_directories(
    /home/angel/Documentos/UCSP/Semestre7/ComputacionGrafica/ArchivosOpenGL/glfw-3.3.8
)

TARGET_LINK_LIBRARIES(SpaceInvaders
    glfw
    OpenGL::GL
)