cmake_minimum_required(VERSION 3.8)
project(isam_hackathon_2025_main)

if(CMAKE_CXX_COMPILER_ID MATCHES "(GNU|Clang)")
  add_compile_options(-Wall -Wextra -Werror=conversion -Werror=unused-but-set-variable -Werror=return-type -Werror=shadow)
endif()

# Find dependencies
find_package(ament_cmake REQUIRED)

# Install files
install(DIRECTORY
  config
  launch
  models
  # rviz
  worlds
  DESTINATION share/${PROJECT_NAME})

if(BUILD_TESTING)
endif()

ament_package()
