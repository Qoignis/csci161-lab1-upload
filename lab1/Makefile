#Makefile for CSCI 161 Lab1

#declaring variables
CC = g++
WFLAG = -Wall
CFLAG = -c
OFLAG = -o
DFLAG = -ggdb
IFLAG = -I
SOURCE = src
INCLUDE = include
OBJECTS = build
BINARY = bin

#dependecies are two targets which will ultimately compile and link main with greetings_csci161 and greetings_csci161
#all will compile both of them and produce two exe files in the bin folder
all: greetcsci160 greetcsci161

#dependecies are two targets
#will compile + link main.o with greetings_csci160.o to produce an exe in the bin folder
greetcsci160: main.o greetings_csci160.o
	${CC} ${WFLAG} ${DFLAG} ${IFLAG} ${INCLUDE} ${OFLAG} ${BINARY}/greetcsci160 ${OBJECTS}/main.o ${OBJECTS}/greetings_csci160.o

#dependecies are two targets
#will compile + link main.o with greetings_csci161.o to produce an exe in the bin folder 
greetcsci161: main.o greetings_csci161.o
	${CC} ${WFLAG} ${DFLAG} ${IFLAG} ${INCLUDE} ${OFLAG} ${BINARY}/greetcsci161 ${OBJECTS}/main.o ${OBJECTS}/greetings_csci161.o

#dependencies are files
#will produce an object in build folder called "main.o" used by greetcsci160 and greetcsci161
main.o: ${SOURCE}/main.cpp ${INCLUDE}/greetings.h
	${CC} ${WFLAG} ${CFLAG} ${DFLAG} ${IFLAG} ${INCLUDE} ${OFLAG} ${OBJECTS}/main.o ${SOURCE}/main.cpp
#dependecies are files
#will produce an object in build folder called "greetings_csci160.o" used by greetcsci160
greetings_csci160.o: ${SOURCE}/greetings_csci160.cpp ${INCLUDE}/greetings.h
	${CC} ${WFLAG} ${CFLAG} ${DFLAG} ${IFLAG} ${INCLUDE} ${OFLAG} ${OBJECTS}/greetings_csci160.o ${SOURCE}/greetings_csci160.cpp

#dependecies are files
#will produce an object in build folder called "greetings_csci161.o" used by greetcsci161
greetings_csci161.o: ${SOURCE}/greetings_csci161.cpp ${INCLUDE}/greetings.h
	${CC} ${WFLAG} ${CFLAG} ${DFLAG} ${IFLAG} ${INCLUDE} ${OFLAG} ${OBJECTS}/greetings_csci161.o ${SOURCE}/greetings_csci161.cpp

#naming phony targets
.PHONY: clean

#will delete files from bin and build folders (executables and object files)
clean:
	rm -rf ${OBJECTS}/* ${BINARY}/*
