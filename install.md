### Preface

Before using xv6 on qemu, we need to install them. 

### Enviroment

Operating System: Linux yonglu-syl 3.19.0-73-generic #81-Ubuntu SMP Tue Oct 18 16:03:37 UTC 2016 x86_64 x86_64 x86_64 GNU/Linux

GCC: gcc (Ubuntu 4.9.2-10ubuntu13) 4.9.2

### Qemu

1. Download Qemu source code: `git clone http://web.mit.edu/ccutler/www/qemu.git -b 6.828-2.3.0`

2. On Linux, you may need to install several libraries. We have successfully built 6.828 QEMU on Debian/Ubuntu 16.04 after installing the following packages: libsdl1.2-dev, libtool-bin, libglib2.0-dev, libz-dev, and libpixman-1-dev

3. Compile source code: `Linux: ./configure --disable-kvm [--prefix=PFX] [--target-list="i386-softmmu x86_64-softmmu"]`

4. Install Qemu: `make && make install`

ps: this version of Qemu is patched by mit, with better debugging facilities. I recommend you run `./configure` with option `target-list`, which would save you time.

### Xv6

1. Download Xv6 source code: `git clone git://github.com/mit-pdos/xv6-public.git`

2. Build Xv6: `make`

3. Run Xv6 on Qemu: `make qemu` (*make sure you have installed Qemu*)

