# Makefile for Proxy Lab 
#
# You may modify this file any way you like (except for the handin
# rule). You instructor will type "make" on your specific Makefile to
# build your proxy from sources.

CC = gcc
CFLAGS = -g -Wall
LDFLAGS = -lpthread

all: echo

csapp.o: ../csapp.c ../csapp.h
	$(CC) $(CFLAGS) -c ../csapp.c

echoserveri.o: echoserveri.c ../csapp.h
	$(CC) $(CFLAGS) -c echoserveri.c

echo.o: echo.c ../csapp.h
	$(CC) $(CFLAGS) -c echo.c

echo: echo.o echoserveri.o csapp.o
	$(CC) $(CFLAGS) echo.o echoserveri.o csapp.o -o echoserver $(LDFLAGS)

# Creates a tarball in ../proxylab-handin.tar that you can then
# hand in. DO NOT MODIFY THIS!
#handin:
#	(make clean; cd ..; tar cvf $(USER)-proxylab-handin.tar proxylab-handout --exclude tiny --exclude nop-server.py --exclude proxy --exclude driver.sh --exclude port-for-user.pl --exclude free-port.sh --exclude ".*")

clean:
	rm -f *~ *.o echo core *.tar *.zip *.gzip *.bzip *.gz

