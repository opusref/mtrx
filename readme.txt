apt-get install opus-tools libopus-dev
find后看到opus.h路径在 /usr/include/opus下
没有find opus的库，但是下面执行成功说明也没问题

Apt install libasound2-dev

需要在编译选项后加 –lasound

gcc -c common.c -I/usr/include/opus -lopus  -lasound -o common.o
gcc -c common.c -I/usr/include/opus -lopus  -lasound -o common.o
gcc -c mrx.c -I/usr/include/opus -lopus  -lasound -o mrx.o
gcc -c mtx.c -I/usr/include/opus -lopus  -lasound -o mtx.o
gcc -c multicall.c -I/usr/include/opus -lopus  -lasound -o multicall.o

