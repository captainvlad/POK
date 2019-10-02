CC = gcc
OB = obj
FILE_1 = example
FILE_2 = minigzip


all: library $(FILE_1) $(FILE_2)
	$(CC) obj/$(FILE_1).o -o bin/prog_1 -L../library/dynamic_lib. -lfunctions
	$(CC) obj/$(FILE_2).o -o bin/prog_2 -L../library/dynamic_lib. -lfunctions

library:
	mkdir obj
	mkdir bin

$(FILE_1): $(FILE_1).c
	$(CC) -c $(FILE_1).c -o $(OB)/$(FILE_1).o

$(FILE_2): $(FILE_2).c
	$(CC) -c $(FILE_2).c -o $(OB)/$(FILE_2).o






.PHONY : clean
clean:
	rm -rf $(OB)/*.o

