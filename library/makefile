CC = gcc
OBJ = obj

SOURCES =  $(wildcard *.c)

OBJS = $(patsubst %.c,$(OBJ)/%.o,$(SOURCES))

all: directories static_lib dynamic_lib
	echo $(SOURCES)

directories:
	mkdir obj
	mkdir static_lib
	mkdir dynamic_lib

dynamic_lib: static_lib
	${CC} -shared -Wl,-soname,libfunctions.dll,--out-implib,dynamic_lib/libfunctions.dll.a -o dynamic_lib/libfunctions.dll $(OBJS)

static_lib: $(OBJS)
	ar rcs static_lib/libfunctions.a $(OBJS)

$(OBJ)/%.o: %.c
	$(CC) -c $<  -o $@ -fPIC

.PHONY : clean
clean:
	rm -rf $(OBJ)/*.o


