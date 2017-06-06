CFLAGS = -I ./include
##LIB    = ./lib/fmod/libfmodex64.so
LFLAGS = -lrt -lX11 -lGLU -lGL -pthread -lm #-lXrandr

all: snake

snake: snake.cpp ppm.cpp log.cpp
	g++ $(CFLAGS) snake.cpp ppm.cpp log.cpp libggfonts.a \
	/usr/lib/x86_64-linux-gnu/libopenal.so /usr/lib/libalut.so \
	-Wall -Wextra $(LFLAGS) -o snake

clean:
	rm -f snake
	rm -f *.o

