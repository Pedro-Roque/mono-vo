cmake_minimum_required(VERSION 2.8)
project( mono-vo )

find_package(OpenCV 3.4.5 EXACT REQUIRED PATHS /home/roque/Git/opencv/install/share/OpenCV)

file(GLOB viso
    "src/*.h"
    "src/*.cpp"
)
add_executable( vo ${viso} )

target_link_libraries( vo ${OpenCV_LIBS})