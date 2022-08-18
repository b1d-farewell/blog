+++ 
date = 2022-08-19 04:27:43
title = "c++ - Compiling a Qt5.2 project on OsX 10.9 with gcc4.2? - Stack Overflow"
description = "I have a QT project that works perfectly under my current configuration ( OsX 10.8.5, QT4.8.5 and compiler i686-apple-darwin11-llvm-gcc-4.2 (GCC) 4.2.1 (Based on Apple Inc. build 5658) (LLVM build ..."
slug = ""
authors = []
tags = []
categories = []
externalLink = "https://stackoverflow.com/questions/21952340/compiling-a-qt5-2-project-on-osx-10-9-with-gcc4-2?rq=1"
series = []
+++
![](https://www.gravatar.com/avatar/a4f260f32d1d020a7f83adc0d809b3fe?s=32&d=identicon&r=PG&f=1)

Bailin Lu

I have a QT project that works perfectly under my current configuration (OsX 10.8.5, QT4.8.5 and compiler i686-apple-darwin11-llvm-gcc-4.2 (GCC) 4.2.1 (Based on Apple Inc. build 5658) (LLVM build 2336.11.00)

The problem is I am switching to a new laptop that has OsX 10.9 installed. As known problem there is only CLang. Using CLang the project gives a lot of **compilation errors on some libraries** that I cannot change. (errors that are not given under the current configuration).

Hence I have installed **apple-GCC4.2.1** using brew and with `gcc --version` I get: `i686-apple-darwin11-llvm-gcc-4.2.1 (GCC) 4.2.1 (Apple Inc. build 5666) (dot 3)`.

Now I get "no such file or directory" for files `<stdarg.h>` and `<float.h>`, under the directory `/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX10.9.sdk/usr/include/c++/4.2.1`

For what I have understood it is like it is including the basic c++ headers from the `Xcode compiler` and they do not match with the ones that gcc4.2.1 wants.

Can someone help me? thank you in advance.

![](https://lh3.googleusercontent.com/-XdUIqdMkCWA/AAAAAAAAAAI/AAAAAAAAAAA/4252rscbv5M/photo.jpg?sz=64)

Fr.Usai

All of the C++ code (Qt, your application, any C++ libraries that you use) must be compiled with the same C++ compiler.

![](https://www.gravatar.com/avatar/2046905520ff348721f4e6e6d6394c57?s=64&d=identicon&r=PG)

Kuba hasn't forgotten Monica

I have solved.

**I have to say that the following procedure worked for my case, but I cannot be sure that this can work for you and/or if this procedure can be dangerous for your system configuration.**

For me, worked this procedure.

*   Install command_line_tools_os_x_mavericks_for_xcode_late_october_2013 (not sure if it is necessary, but i think so)
*   Install Qt4.8.5 and set it up on QtCreator
*   install [homebrew](http://brew.sh/)
*   install apple-gcc42 and gdb using brew:
    
    brew tap homebrew/dupes
    
    brew install apple-gcc42
    
    brew install gdb
    

set up the compiler and GDB on QtCreator and then create your kit.

*   codesign gdb following [this](http://panks.me/blog/2013/11/install-gdb-on-os-x-mavericks-from-source/) guide (scroll until you find "Generate Certificate for signing".

have fun.

in my case it was necessary to modify the makefile in order to set for CFLAGS, CXXFLAGS and LFLAGS the value -mmacosx-version-min=10.6.