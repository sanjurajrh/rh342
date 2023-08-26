# rh342
1. Install the gcc package 
# yum -y install gcc
2. Clone the repository to get the application example
# git clone https://github.com/sanjurajrh/rh342.git
3. Once cloned, change to the directory and then complie the c program
# cd rh342
# gcc -o example example.c
4. After compiling, save the example file to /usr/local/bin so that it will be available for everyone
# cp -av example /usr/local/bin
5. Now use the different options with valgrind to check the memory errors (Ensure that the valgrind package is installed)
# valgrind --tool=memcheck example
# valgrind --tool=memcheck --leak-check=full example
# valgrind --tool=memcheck --leak-check=full --show-reachable=yes --log-file=example.memchk example
