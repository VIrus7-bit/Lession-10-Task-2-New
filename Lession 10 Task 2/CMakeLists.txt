﻿# CMakeList.txt: проект CMake для Lession 10 Task 2; включите исходный код и определения,
# укажите здесь логику для конкретного проекта.
#
cmake_minimum_required (VERSION 3.8)

# Включение горячей перезагрузки для компиляторов MSVC, если поддерживается.
if (POLICY CMP0141)
  cmake_policy(SET CMP0141 NEW)
  set(CMAKE_MSVC_DEBUG_INFORMATION_FORMAT "$<IF:$<AND:$<C_COMPILER_ID:MSVC>,$<CXX_COMPILER_ID:MSVC>>,$<$<CONFIG:Debug,RelWithDebInfo>:EditAndContinue>,$<$<CONFIG:Debug,RelWithDebInfo>:ProgramDatabase>>")
endif()

project ("Lession 10 Task 2")

# Добавьте источник в исполняемый файл этого проекта.
add_executable (CMakeTarget "Lession 10 Task 2.cpp" "Parallelogram.cpp" "Quadrilateral.h" "Quadrilateral.cpp" "Rectangle.cpp" "Rectangle.h" "Rhomb.cpp" "Rhomb.h" "Triangle.cpp" "equilateralTriangle.h" "equilateralTriangle.cpp" "isoscelesTriangle.cpp" "isoscelesTriangle.h" "printFigure.cpp" "printFigure.h" "rightTriangle.cpp" "rightTriangle.h" "Square.h" "Triangle.cpp" "Triangle.h" "Square.cpp" "Figure.cpp" "Figure.h")

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET CMakeTarget PROPERTY CXX_STANDARD 20)

endif()

# TODO: Добавьте тесты и целевые объекты, если это необходимо.
