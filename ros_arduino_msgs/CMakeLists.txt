cmake_minimum_required(VERSION 2.8.3)
project(ros_arduino_msgs)

find_package(catkin REQUIRED COMPONENTS genmsg std_msgs message_generation)

add_message_files(FILES
                  AnalogFloat.msg
                  Analog.msg
                  Digital.msg
                  SensorState.msg
                 )

add_service_files(FILES
                  DigitalSetDirection.srv
                  DigitalWrite.srv
                  ServoRead.srv
                  ServoWrite.srv
                 )

generate_messages(DEPENDENCIES std_msgs)

catkin_package(CATKIN_DEPENDS std_msgs message_runtime)

