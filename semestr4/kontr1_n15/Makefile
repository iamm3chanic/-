CC = g++
CFLAGS = -W -Wall -Wfloat-equal -Wpointer-arith -Wwrite-strings -Wcast-align \
-Wformat-security -Wmissing-format-attribute -Wformat=1 \
-Wno-long-long -Wcast-align -Winline -Werror -pedantic -pedantic-errors \
-Wunused -Wuninitialized -fno-elide-constructors \
--param inline-unit-growth=1000000 --param max-inline-insns-single=10000000 \
--param large-function-growth=10000000 -fPIC -O2

m: CFunctions.o Main.o Makefile
	$(CC) $(CFLAGS) -o m CFunctions.o Main.o
CFunctions.o: CFunctions.cpp CIntN.h Makefile
	$(CC) $(CFLAGS) -c -g -O2 CFunctions.cpp
Main.o: Main.cpp CIntN.h Makefile
	$(CC) $(CFLAGS) -c -g -O2 Main.cpp
clean:
	rm -f m CFunctions.o Main.o vgcore* out*.txt
