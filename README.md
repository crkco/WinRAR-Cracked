# WinRAR-Cracked
WinRAR.exe without annoying popups when opening.

Only 19 bytes have been changed:

At 0x8b23f:

A call to SetWindowTextW() has been replaced with EndDialog():

Assembler: 
xor rdx, rdx
nop
nop
nop
nop
mov rxc, r15
call EndDialog
(48 31 D2 90 90 90 90 49 8B CF FF 15 D9 9D 08 00)

At 0xa4ec7:

WS_STYLE argument of CreateWindowExW() has been changed to 0x0:

Assembler:
xor r9d, r9d
(45 31 C9)
