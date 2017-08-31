cmake_minimum_required(VERSION 2.8.3)
project(radio_services)

find_package(catkin REQUIRED COMPONENTS
	roscpp
	rospy
	std_msgs
	message_generation
)

add_service_files(
	FILES
	InstructionWithAnswer.srv
        InstructionAndStringWithAnswer.srv
)

generate_messages(
	DEPENDENCIES
	std_msgs
)

catkin_package()
