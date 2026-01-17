# Acer-Nitro-5-AN515-55-Linux-Kernel-Config
Linux Kernel config file Optimized for Acer Nitro 5 AN515-55

(This is not a complete list)
- Ran `localmodconfig`
- Disabled all network drivers except intel
- Disabled all graphics driver support(I use nvidia proprietary)
- Disabled a lot of Debug stuff
- Only supports ext4 file system
- Disabled Virtual Machine guest support
- Enabled LTOThin
- Disabled everything related to AMD
- Compiled using `make -j$(nproc) LLVM=1 KCFLAGS="-march=native -O3 -pipe" bindeb-pkg`


This is not the best config file but these are some optimizations that has worked for me. Do suggest further changes.

The compile time decreased significantly. The vmlinuz file size went from 12MB to 9MB and the boottime dropped by 2 seconds.
