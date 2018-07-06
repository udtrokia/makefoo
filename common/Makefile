# Makefile 1
## hellomake: hellomake.c hellofunc.c
##	 gcc -o hellomake hellomake.c hellofunc.c -I.

# Makefile 2
## CC=gcc
## CFLAGS=-I.
## 
## hellomake: hellomake.o hellofunc.o # rules
## 	$(CC) -o hellomake hellomake.o hellofunc.o

# Makefile 3
## CC=gcc
## CFLAGS=-I.
## DEPS = hellomake.h
## 
## %.o: %.c $(DEPS)
## 	$(CC) -c -o $@ $< $(CFLAGS)
## 
## hellomake: hellomake.o hellofunc.o
## 	$(CC) -o hellomake hellomake.o hellofunc.o

# Makefile 4
CC=gcc
CFLAGS=-I.
DEPS = hellomake.h
OBJ = hellomake.o hellofunc.o

%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

hellomake: $(OBJ)
	$(CC) -o $@ $^ $(CFLAGS)

clean:
	rm -rf *o && rm hellomake
