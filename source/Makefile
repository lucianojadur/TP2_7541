PROGRAM=tp
CC=g++
CFLAGS=-Wall -pedantic -g
LDFLAGS=-lm


all:$(PROGRAM)

$(PROGRAM): main.o menu.o parser.o personaje.o agua.o fuego.o tierra.o aire.o
	$(CC) $(CFLAGS) -o $(PROGRAM) main.o menu.o parser.o personaje.o agua.o fuego.o tierra.o aire.o $(LDFLAGS) 

main.o: main.cpp list.h node.h personaje.h agua.h fuego.h tierra.h aire.h
	$(CC) $(CFLAGS) -c main.cpp 

menu.o: menu.cpp menu.h parser.h personaje.h agua.h fuego.h tierra.h aire.h list.h utils.h
	$(CC) $(CFLAGS) -c menu.cpp

parser.o: parser.cpp parser.h utils.h
	$(CC) $(CFLAGS) -c parser.cpp

personaje.o: personaje.cpp personaje.h utils.h
	$(CC) $(CFLAGS) -c personaje.cpp

agua.o: agua.cpp agua.h personaje.h
	$(CC) $(CFLAGS) -c agua.cpp

fuego.o: fuego.cpp fuego.h personaje.h
	$(CC) $(CFLAGS) -c fuego.cpp

tierra.o: tierra.cpp tierra.h personaje.h
	$(CC) $(CFLAGS) -c tierra.cpp

aire.o: aire.cpp aire.h personaje.h
	$(CC) $(CFLAGS) -c aire.cpp
	
clean:
	rm -vf  *.o $(PROGRAM)