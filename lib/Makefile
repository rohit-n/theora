SRC = $(wildcard *.c)
OBJ = $(patsubst %.c, %.o, $(SRC))

ifndef OGG_INC
$(error OGG_INC directory not set)
endif

CFLAGS= -I $(OGG_INC) -I ../include

libtheora.a: $(OBJ)
	$(AR) rcs libtheora.a $(OBJ)

%.o: %.c
	$(CC) $< -c $(CFLAGS) -o $@

clean:
	rm -f *.o libtheora.a