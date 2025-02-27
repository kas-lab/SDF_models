cmake_minimum_required(VERSION 3.5)
project(sdf_models)

find_package(ament_cmake QUIET)

if(ament_cmake_FOUND)
  message(STATUS "Ament found." )
else()
  message(FATAL_ERROR "Ament was not found. Unable to build." )
endif()

find_package(gazebo_ros REQUIRED)

install(DIRECTORY 
  food_bread
  food_strawberry
  furniture_table_cafe
  utensil_bottle_beer
  utensil_bottle_beer_blue
  utensil_bottle_beer_green
  utensil_bottle_beer_red
  utensil_bottle_wine
  utensil_bowl_blue
  utensil_bowl_green
  utensil_bowl_red
  utensil_can_coke
  utensil_can_fanta
  utensil_can_pepsi
  utensil_can_sprite
  utensil_cup_blue
  utensil_cup_green
  utensil_cup_red
  utensil_fork_blue
  utensil_fork_green
  utensil_fork_red
  utensil_mat_blue_small
  utensil_mat_red_small
  utensil_plate1_blue
  utensil_plate1_green
  utensil_plate1_red
  utensil_plate2_blue
  utensil_plate2_green
  utensil_plate2_red
  utensil_plate_blue
  utensil_plate_blue_small
  utensil_plate_glass
  utensil_plate_green
  utensil_plate_red
  utensil_spoon_blue
  utensil_spoon_green
  utensil_spoon_red
  DESTINATION share/${PROJECT_NAME})

ament_export_dependencies(gazebo_ros)
ament_package()
