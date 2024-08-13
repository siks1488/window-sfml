cmake_minimum_required(VERSION 3.10)

# Setează numele proiectului
project(MySFMLProject)

# Specifică standardul C++ (opțional)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Adaugă fișierul sursă
add_executable(${PROJECT_NAME} main.cpp)

# Găsește pachetul SFML instalat
find_package(SFML 2.5 COMPONENTS graphics window system REQUIRED)

# Leagă SFML de executabil
target_link_libraries(${PROJECT_NAME} sfml-graphics sfml-window sfml-system)
