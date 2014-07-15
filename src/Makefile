#!/bin/sh

ALL: libhashab32_wrapper libhashab.so

# Compile the 32 bit wrapper in 32 bit mode
libhashab32_wrapper: libhashab32_wrapper.c
	$(CC) $< -o $@ -ldl -fno-stack-protector -m32

# Build the libhashab.so library
libhashab.o: libhashab.c
	$(CC) $< -o $@ -c -fpic 

libhashab.so: libhashab.o libhashab.c
	$(CC) $< -o $@ -shared
