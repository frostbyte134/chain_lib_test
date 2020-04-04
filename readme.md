 1. cd print1
 2. gcc -c print1.c -o print1.o
 3. gcc ar libprint1.a print1.o
 2. cd ../print2
 2. gcc -c print2.c -o print2.o -L/home/nailbrainz/Documents/chain_lib_test/print1 -I/home/nailbrainz/Documents/chain_lib_test/print1
 3. gcc ar libprint2.a print2.o
 4. ar rc libprint2.a print2.o
 5. cd ..
 5. gcc -o main main.c -I/home/nailbrainz/Documents/chain_lib_test/print2 -L/home/nailbrainz/Documents/chain_lib_test/print2 -I/home/nailbrainz/Documents/chain_lib_test/print1 -L/home/nailbrainz/Documents/chain_lib_test/print1 -lprint2 -lprint1
 6. ./main 