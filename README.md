This repo contains openssl-1.1.1k prebuit binary for Windows x64.

You can get source code from official openssl release page and rebuilt binary your self:
https://ftp.openssl.org/source/old/1.1.1/openssl-1.1.1k.tar.gz

How to compile:

- Download MSYS2 from https://msys2.github.io/. 

- Install make, perl, mingw-w64-x86_64-gcc

pacman -S make
pacman -S perl
pacman -S mingw-w64-x86_64-gcc

- Export path to mingw gcc

export PATH=/mingw64/bin:$PATH

- Configure and build for 64 bit: Goto openssl source directory

perl Configure mingw64 shared --prefix=/C/OpenSSL-x64
make depend
make

- Configure and build for 32 bit (If need build 32 bit sdk): 

perl Configure mingw shared --prefix=/C/OpenSSL-x86
make depend
make

