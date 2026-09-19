hey what's up.
i built unshield.exe so you don't have to like do it haha

how did i build it?
i don't know!
first you go to the unshield source dir
then you mkdir build
then cd build
then run that first line there, IF you have the zlib.dll and other files from https://github.com/OSDVF/zlib-win-x64 extracted to c:\libs\zlib-win-x64
which yoou would do by being in c:\libs and running git clone c:\libs\zlib-win-x64.git
then run the second line from the unshield source directory

cmake -S . -B build-shared -G "Visual Studio 17 2022" -A x64 -DBUILD_SHARED_LIBS=ON -DZLIB_LIBRARY="C:/libs/zlib-win-x64/zdll.lib" -DZLIB_INCLUDE_DIR="C:/libs/zlib-win-x64"

cmake --build build-shared --config Release

yeah at first i built it without -DBUILD_SHARED_LIBS=ON and it didn't build the .dll lol

anyways i hope this helps cause like seriously who can build cmake files why don't they have a build up on the unshield site like lol developers "just build it from source yourself" yeah okay dude im also gonna mine and smelt iron and make my own silverware just gotta read the iron smelting manual and the silverware smelting manual first okay
