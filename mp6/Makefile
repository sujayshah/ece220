CC=gcc
CFLAGS=-g -lm -std=c99 -Wall -Werror 

all: mp6 test

mp6: main.o lodepng.o imageData.o functions.o
	$(CC) $(CFLAGS) main.o lodepng.o imageData.o functions.o -o mp6 -lm

test: test.o lodepng.o imageData.o functions.o solution.o
	$(CC) $(CFLAGS) test.o lodepng.o imageData.o functions.o solution.o -o test -lm

main.o: main.c
	$(CC) $(CFLAGS) -c main.c

lodepng.o: lodepng.c
	$(CC) $(CFLAGS) -c lodepng.c

imageData.o: imageData.c
	$(CC) $(CFLAGS) -c imageData.c

functions.o: functions.c
	$(CC) $(CFLAGS) -c functions.c 

test.o: test.c
	$(CC) $(CFLAGS) -c test.c 

clean:
	rm -f functions.o imageData.o lodepng.o main.o test.o mp6 test
