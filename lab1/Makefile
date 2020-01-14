#Makefile for CSCI 161 Lab1

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

all: greetcsci160 greetcsci161

greetcsci160: main.o greetings_csci160.o
	${CC} ${WFLAG} ${DFLAG} ${IFLAG} ${INCLUDE} ${OFLAG} ${BINARY}/greetcsci160 ${OBJECTS}/main.o ${OBJECTS}/greetings_csci160.o

greetcsci161: main.o greetings_csci161.o
	${CC} ${WFLAG} ${DFLAG} ${IFLAG} ${INCLUDE} ${OFLAG} ${BINARY}/greetcsci161 ${OBJECTS}/main.o ${OBJECTS}/greetings_csci161.o

main.o: ${SOURCE}/main.cpp ${INCLUDE}/greetings.h
	${CC} ${WFLAG} ${CFLAG} ${DFLAG} ${IFLAG} ${INCLUDE} ${OFLAG} ${OBJECTS}/main.o ${SOURCE}/main.cpp

greetings_csci160.o: ${SOURCE}/greetings_csci160.cpp ${INCLUDE}/greetings.h
	${CC} ${WFLAG} ${CFLAG} ${DFLAG} ${IFLAG} ${INCLUDE} ${OFLAG} ${OBJECTS}/greetings_csci160.o ${SOURCE}/greetings_csci160.cpp

greetings_csci161.o: ${SOURCE}/greetings_csci161.cpp ${INCLUDE}/greetings.h
	${CC} ${WFLAG} ${CFLAG} ${DFLAG} ${IFLAG} ${INCLUDE} ${OFLAG} ${OBJECTS}/greetings_csci161.o ${SOURCE}/greetings_csci161.cpp

.PHONY: clean

clean:
	rm -rf ${OBJECTS}/* ${BINARY}/*
