# Text Editor

This project was built based on [FLTk Tutorial](https://www.fltk.org/doc-1.1/editor.html).

### How to build

**Requirements**
  - [FLTK Liberie](https://www.fltk.org/)
  - [CMake](https://cmake.org/)

**Windows version**</br>
In the root folder run:</br>
```
    cmake --preset=default
```
Before that run:
```
  cmake --build build
```
Go to `\build\Debug` then open `text_editor.exe`

**Linux version**</br>
In the root folder run:
```
  g++ -I. -I./jpeg -I/usr/include/uuid -I/usr/include/freetype2 -I/usr/include/libpng16 -D_LARGEFILE_SOURCE -D_LARGEFILE64_SOURCE -D_THREAD_SAFE -D_REENTRANT -o './build/release/text_editor' './text_editor.cpp' /usr/local/lib/libfltk.a -lXrender -lXft -lfontconfig -lpthread -lm -lX11
```
  
  
