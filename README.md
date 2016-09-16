# ArmTOS
This project is a simple attempt to create a 68030 Dynamic Recompiling emulator that runs as the OS on the Raspberry Pi 0/B/B+/2B/3B single board computers, and allows running of 680x0 Atari TOS and MiNT compatible OS's with the correct drivers and TSR's.   That is to say that the goal is to implement a simple layer that alows using TOS with MiNT and whatever VDI, AES, and desktop you prefer as the main Operating System on a Raspberry Pi computer.

# Method of implementation:
Needless to say that there are a few things that just can not be done from inside the emulated 68030, such as USB and Ethernet.  for these there is a specialised interface in the XBIOS to allow calling drivers that run ARM native.   For the current versions these ARM native drivers are provided by Ultibo, as well as basic booting.

There is also a simple interface to allow running ARM native applications that can call the 68K operating system through the provided TRAPs (which are mapped to SWIs on the ARM).   You just need to remember that the endianes is backward if calling the 68K OS from ARM Code.
