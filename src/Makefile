#!/bin/sh

ALL: libhashab32_wrapper libhashab.so

# Compile the 32 bit wrapper in 32 bit mode
libhashab32_wrapper: libhashab32_wrapper.c
	$(CC) -o libhashab32_wrapper libhashab32_wrapper.c -ldl -fno-stack-protector -m32

# Build the libhashab.so library
libhashab.o: libhashab.c
	$(CC) -c -fpic libhashab.c -o libhashab.o

libhashab.so: libhashab.o
	 $(CC) -shared -o libhashab.so libhashab.o
