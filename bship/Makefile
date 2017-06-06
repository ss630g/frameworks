CFLAGS = -pthread
##LIB    = ./libggfonts.so
LFLAGS = -lrt -lX11 -lGLU -lGL -pthread -lm #-lXrandr

all: bship

bship: bship.o ppm.o log.o
	gcc bship.o ppm.o log.o libggfonts.a $(LFLAGS) -o bship

bship.o: bship.c
	gcc -c $(CFLAGS) bship.c libggfonts.a

ppm.o: ppm.c
	gcc -c $(CFLAGS) ppm.c

#cfonts.o: cfonts.c
#	gcc -c $(CFLAGS) cfonts.c
#
#fonttex.o: fonttex.c
#	gcc -c $(CFLAGS) fonttex.c

log.o: log.c
	gcc -c $(CFLAGS) log.c

clean:
	rm -f bship
	rm -f *.o

