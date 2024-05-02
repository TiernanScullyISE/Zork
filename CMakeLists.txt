cmake_minimum_required(VERSION 3.5)

project(zorkMaybeActually LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(zorkMaybeActually
    ZorkUL.cpp
    Room.cpp
    Room.h
    Character.cpp
    Command.cpp Command.h CommandWords.cpp CommandWords.h item.cpp item.h main.cpp    Parser.cpp Parser.h Room.cpp Room.h ZorkUL.cpp ZorkUL.h)

include(GNUInstallDirs)
install(TARGETS zorkMaybeActually
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)
