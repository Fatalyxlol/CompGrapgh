cmake_minimum_required(VERSION 3.26)
project(cg6)

set(CMAKE_CXX_STANDARD 20)
find_package(nlohmann_json CONFIG REQUIRED)

add_executable(cg6 main.cpp pixbuf.cpp pixel.cpp polygon.cpp line.cpp
        matrix.h
        camera.cpp
        camera.h
        object.cpp
        object.h
        transform.cpp
        transform.h
        matrix.cpp
        algorithm.cpp
        algorithm.h
        figures.h
        figures.cpp
        gui.cpp
        gui.h
        expressionparser.cpp
        expressionparser.h
        indexpolygon.cpp
        indexpolygon.h
        lightsource.cpp
        lightsource.h
        vertex.cpp
        vertex.h
        indexvertex.cpp
        indexvertex.h
)
target_link_libraries(cg6 sfml-graphics sfml-window sfml-system tgui nlohmann_json::nlohmann_json)
