# DELL-OptiPlex-7040-Clover
Clover for DELL OptiPlex 7040 with Skylake CPU & GPU

Only fix the Graphics by Bios hack, Ethernet, USB, and sound card with AppleALC, but, is enough! Less is more.

Test with DELL OptiPlex 7040 which using i7-6700, Intel HD Graphics 530, Intel I219LM2 Ethernet, macOS 10.14.

- I extract the BIOS.rom by AMI Flasher utility.

- I unlock the MSR 0xE2 from here. [https://github.com/acidanthera/AptioFixPkg]
- I modity the DVMT to 96MB by [https://www.firewolf.science/2015/04/guide-intel-hd-graphics-5500-on-os-x-yosemite-10-10-3/]
- For OptiPlex 7040 the CFG lock address is 0xAF, so "setup_var 0xAF 0x0" to Disable CFG lock(MSR 0xE2)
- DVMT Pre-Allocated address is 0x350, so "setup_var 0x350 0x3" to set 96MB [中文教程](https://zhuanlan.zhihu.com/p/39798235)
- Note: the DVMT & CFG lock fixup will lose after set BOIS to factory default!

If you don't want to fix the BIOS, you can just using the WhateverGreen hotpatch by just using CLOVER, see this branch [https://github.com/irelandKen/DELL-OptiPlex-7040-Clover/tree/macOS_10.14] 
