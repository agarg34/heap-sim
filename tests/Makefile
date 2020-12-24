C_FILES := $(wildcard *.c)
TARGETS := ${C_FILES:.c=}

all: ${TARGETS}

%: %.c
	@gcc -I.. -g -m32 -Xlinker -rpath=.. -o $@ $< -L.. -lheap -std=gnu99

clean:
	@rm -rf ${TARGETS} *.o

run:
	@clear
	@$(MAKE) clean
	@$(MAKE) all
	@# ./mytest1
	@# cat test_alloc1.c
	# PART A: Memory Allocation
	./test_alloc1
	./test_alloc1_nospace
	./test_writeable
	./test_align1
	./test_alloc2
	./test_alloc2_nospace
	./test_align2
	./test_alloc3
	./test_align3
	# PART B: Memory Freeing
	./test_free1
	./test_free2
	./test_coalesce1
	./test_coalesce2
	./test_coalesce3
	./test_coalesce4
	./test_coalesce5
	./test_coalesce6
	
	@$(MAKE) clean
