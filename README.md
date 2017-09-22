# Learning Windows internals
This repo contains tips and cool tools information from sysinternals book.

## You can buy the 7th edition of `Windows Internals, Part 1` from:
https://www.amazon.com/Windows-Internals-Part-architecture-management/dp/0735684189

## Repo for the 7th edition tools:
https://github.com/zodiacon/WindowsInternals

### Tools
  * `tlist.exe` - equivalent of `ps auxf`. Found in the `Debuging tools` package, in Windows ADK.
  * `Sysinternals Desktops` - can create up to four virtual desktops. Download link: https://download.sysinternals.com/files/Desktops.zip
  * `Process Explorer` - Task Manager on steroids. Download link: https://download.sysinternals.com/files/ProcessExplorer.zip
  * Use `Performance Monitor` native Windows tool to see granular information about the OS. Example: how much time the applications spend in user mode or kernel mode.

### Tips
  * `increaseuserva` is a bcdedit option to allow 3GB of process max memory space instead of 2GB on 32bit. More info: https://msdn.microsoft.com/en-us/library/windows/hardware/ff542202(v=vs.85).aspx
  * Windows and Linux use only rings 0 for kernel space and ring 3 for user space. x86 processors implement 4 rings, whereas PowerPC/MIPS only 2. 
  * Windows drivers security:  On x86 arch - a driver has unrestricted access. On x64 arch - Kernel Mode Code Signing (KMCS) policy on x64 (can be disabled byb pressing F8 at the boot time +  Disable Driver Signature Enforcement).
