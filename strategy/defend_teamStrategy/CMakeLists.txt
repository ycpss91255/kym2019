
##############################################################################
# Sections
##############################################################################


##############################################################################
# Sources
##############################################################################



##############################################################################
# Binaries
##############################################################################

add_executable(defend_teamStrategy FIRA_teamStrategy.cpp teamStrategy_nodeHandle.cpp main.cpp)
add_dependencies(defend_teamStrategy FIRA_strategy_gencpp)
target_link_libraries(defend_teamStrategy ${catkin_LIBRARIES} BaseNodeLib)
add_dependencies(defend_teamStrategy ${${PROJECT_NAME}_EXPORTED_TARGETS} ${catkin_EXPORTED_TARGETS})
add_dependencies(defend_teamStrategy vision)
#add_dependencies(FIRA_strategy FIRA_strategy_generate_messages_cpp)
#add_dependencies(FIRA_strategy FIRA_Sim_generate_messages_cpp)
#add_dependencies(FIRA_teamStrategy fira_sim_generate_messages_cpp)
