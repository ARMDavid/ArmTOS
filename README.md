# Status Note:
May 2019:  I have gotten a good bit of the core system working.  This includes memory management, task allocation/switching and management, some USB support, some filesystem support, a reasonably complete VDI (about 80%), a usable AES (have a good bit left to do), and some test applications.   I had started off working with a different API, though went back to the TOS/GEM API, as it iw one I know well and is common enough to be of use to others.

I seem to be having trouble uploading files, sorry about that.  And I have a significant amount of code to upload for this project.

# ArmTOS
The target has changed a bit :).

This is a simple ARM based Operating System that is to have an API compatible with that of TOS/GEM as implemented on the Atari 680x0 based computers.  This is a one man project, so it is moving kind of slowly.

Once enough of the system is working, and we have a native C compiler, I will also be adding a simple JIT 68030 emulator to run much original GEM based software, thus instantly increasing the available software library.

# Status:

# Method of implementation:
The system is implemented in a more modular way from traditional TOS.   Each functional type in BIOS, GEMDOS, AES, VDI, etc has its own module for implementation.   This makes it easier to update components, maintain the codebase, and continue development of the project.
