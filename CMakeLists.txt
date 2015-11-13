# Author: Prez Cannady <revprez@opencorrelate.org>
# Date: 11 November 2015

cmake_minimum_required(VERSION 3.3.2)
project (pam_ignore)

set(CMAKE_BUILD_TYPE Release)

file(GLOB SOURCES "src/*.c")

#Generate the shared library from the sources
add_library(testStudent MODULE ${SOURCES})

#Set the location for library installation -- i.e., /usr/lib in this case
# not really necessary in this example. Use "sudo make install" to apply
install(TARGETS testStudent DESTINATION /usr/local/lib)