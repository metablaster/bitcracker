#!/bin/bash

FLAGS=-DCL_TARGET_OPENCL_VERSION=300 -DCL_USE_DEPRECATED_OPENCL_1_2_APIS
NVIDIA_INCLUDE=-I/usr/local/cuda/include -L/usr/local/cuda/lib64
COMMON_INCLUDE=-I/usr/include -L/usr/lib64 -L/usr/lib
MAKE_INCLUDE=$(COMMON_INCLUDE) $(NVIDIA_INCLUDE) -O3

all:
	gcc $(MAKE_INCLUDE) $(FLAGS) -o bitcracker_opencl main.c opencl_attack.c utils.c w_blocks.c -lOpenCL
#	clang -framework OpenCL -o bitcracker_opencl main.c opencl_attack.c utils.c w_blocks.c


clean:
	rm -rf *.o
	rm -rf bitcracker_opencl
