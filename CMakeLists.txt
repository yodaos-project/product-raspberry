cmake_minimum_required(VERSION 3.0)
project(dev3.3 CXX)
include(ExternalProject)

#install(DIRECTORY ./apps            DESTINATION ${CMAKE_INSTALL_DIR}/opt)
install(DIRECTORY ./res/media       DESTINATION ${CMAKE_INSTALL_DIR}/opt)
install(DIRECTORY ./res/light       DESTINATION ${CMAKE_INSTALL_DIR}/opt)
install(DIRECTORY ./workdir_asr_cn  DESTINATION ${CMAKE_INSTALL_DIR}/system)
