# lift life
# http://www.cs.colby.edu/maxwell/courses/tutorials/maketutor/makefile.4
CC=gcc
CFLAGS=-I. -pthread -Wall
DEPS=
OBJ=
MAIN_OBJ=main.o
TEST_OBJ=core.test.o

%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

main: $(OBJ) $(MAIN_OBJ)
	$(CC) -o $@ $^ $(CFLAGS)

test-bin: $(OBJ) $(TEST_OBJ)
	$(CC) -o $@ $^ $(CFLAGS)

.PHONY: test
test:
	make test-bin && ./test-bin

.PHONY: clean
clean:
	rm -rf *.o

