LD_FLAGS :=
CC_FLAGS := -O3 -Wall

all: count_operations count_operations_norm

count_operations: count_operations.o instrumented.o
	g++ $(LD_FLAGS) -o $@ $^

count_operations_norm: count_operations_normalized.o instrumented.o
	g++ $(LD_FLAGS) -o $@ $^

%.o: %.cpp
	g++ $(CC_FLAGS) -c -o $@ $<

clean:
	rm -rf *o count_operations count_operations_norm 
