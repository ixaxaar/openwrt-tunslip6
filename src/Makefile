
# Tunslip6 Makefile

# Include files
INCLUDES = -I ./ \
	-I .

# Libraries being linked to:
# libcurl
# libpthread
# librt (part of pthreads)
LIBS =

CC = $(CC)
LFLAGS = $(LDFLAGS)

# For debugging
DEBUG += -g -ggdb -DDEBUG

# For production, uncomment this
# DEBUG = --strip-all -DPRODUCTION

LFLAGS += -Wall $(DEBUG) -O0
CFLAGS += -Wall -c $(DEBUG)


SOURCES = ./tunslip6.c

HEADERS = 

OBJ = $(SOURCES:.c=.o)

EXE = tunslip6


all: tunslip6

$(EXE):	$(OBJ)
	$(CC) -o $(EXE) $(OBJ) $(LFLAGS) $(LIBS)	

.cpp.o:
	$(CC) $(CFLAGS) $(INCLUDES) $< -o $@

tar:
	tar -czf $(EXE).tar.gz $(SOURCES) $(HEADERS) Makefile

clean:
	rm -f $(OBJ)
	rm -f $(EXE)

