# Bigbang-theory-lab-2
Bigbang theory - IT16064164


root@kali:~# cd Downloads/bigbangtheory-master/
root@kali:~/Downloads/bigbangtheory-master# ./sheldon1
Welcome to my fiendish little bomb. You have 6 phases with
which to blow yourself up. Have a nice day!
^CSo you think you can stop the bomb with ctrl-c, do you?
Well...OK. :-)
root@kali:~/Downloads/bigbangtheory-master# gdb sheldon1
GNU gdb (Debian 8.1-4+b1) 8.1
Copyright (C) 2018 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.  Type "show copying"
and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<http://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
<http://www.gnu.org/software/gdb/documentation/>.
For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from sheldon1...done.
(gdb) start
Temporary breakpoint 1 at 0x80489b7: file bomb.c, line 36.
Starting program: /root/Downloads/bigbangtheory-master/sheldon1 

Temporary breakpoint 1, main (argc=-134562344, argv=0x0) at bomb.c:36
36	bomb.c: No such file or directory.
(gdb) set disassembly-flavor intel
(gdb) disassemble main 
Dump of assembler code for function main:
   0x080489b0 <+0>:	push   ebp
   0x080489b1 <+1>:	mov    ebp,esp
   0x080489b3 <+3>:	sub    esp,0x14
   0x080489b6 <+6>:	push   ebx
=> 0x080489b7 <+7>:	mov    eax,DWORD PTR [ebp+0x8]
   0x080489ba <+10>:	mov    ebx,DWORD PTR [ebp+0xc]
   0x080489bd <+13>:	cmp    eax,0x1
   0x080489c0 <+16>:	jne    0x80489d0 <main+32>
   0x080489c2 <+18>:	mov    eax,ds:0x804b648
   0x080489c7 <+23>:	mov    ds:0x804b664,eax
   0x080489cc <+28>:	jmp    0x8048a30 <main+128>
   0x080489ce <+30>:	mov    esi,esi
   0x080489d0 <+32>:	cmp    eax,0x2
   0x080489d3 <+35>:	jne    0x8048a10 <main+96>
   0x080489d5 <+37>:	add    esp,0xfffffff8
   0x080489d8 <+40>:	push   0x8049620
   0x080489dd <+45>:	mov    eax,DWORD PTR [ebx+0x4]
   0x080489e0 <+48>:	push   eax
   0x080489e1 <+49>:	call   0x8048880 <fopen@plt>
   0x080489e6 <+54>:	mov    ds:0x804b664,eax
   0x080489eb <+59>:	add    esp,0x10
   0x080489ee <+62>:	test   eax,eax
---Type <return> to continue, or q <return> to quit---return
   0x080489f0 <+64>:	jne    0x8048a30 <main+128>
   0x080489f2 <+66>:	add    esp,0xfffffffc
   0x080489f5 <+69>:	mov    eax,DWORD PTR [ebx+0x4]
   0x080489f8 <+72>:	push   eax
   0x080489f9 <+73>:	mov    eax,DWORD PTR [ebx]
   0x080489fb <+75>:	push   eax
   0x080489fc <+76>:	push   0x8049622
   0x08048a01 <+81>:	call   0x8048810 <printf@plt>
   0x08048a06 <+86>:	add    esp,0xfffffff4
   0x08048a09 <+89>:	push   0x8
   0x08048a0b <+91>:	call   0x8048850 <exit@plt>
   0x08048a10 <+96>:	add    esp,0xfffffff8
   0x08048a13 <+99>:	mov    eax,DWORD PTR [ebx]
   0x08048a15 <+101>:	push   eax
   0x08048a16 <+102>:	push   0x804963f
   0x08048a1b <+107>:	call   0x8048810 <printf@plt>
   0x08048a20 <+112>:	add    esp,0xfffffff4
   0x08048a23 <+115>:	push   0x8
   0x08048a25 <+117>:	call   0x8048850 <exit@plt>
   0x08048a2a <+122>:	lea    esi,[esi+0x0]
   0x08048a30 <+128>:	call   0x8049160 <initialize_bomb>
   0x08048a35 <+133>:	add    esp,0xfffffff4
   0x08048a38 <+136>:	push   0x8049660
---Type <return> to continue, or q <return> to quit---quit
Quit
(gdb) phase1
Undefined command: "phase1".  Try "help".
(gdb) disassemble phase1
No symbol "phase1" in current context.
(gdb) disassemble phase_1
Dump of assembler code for function phase_1:
   0x08048b20 <+0>:	push   ebp
   0x08048b21 <+1>:	mov    ebp,esp
   0x08048b23 <+3>:	sub    esp,0x8
   0x08048b26 <+6>:	mov    eax,DWORD PTR [ebp+0x8]
   0x08048b29 <+9>:	add    esp,0xfffffff8
   0x08048b2c <+12>:	push   0x80497c0
   0x08048b31 <+17>:	push   eax
   0x08048b32 <+18>:	call   0x8049030 <strings_not_equal>
   0x08048b37 <+23>:	add    esp,0x10
   0x08048b3a <+26>:	test   eax,eax
   0x08048b3c <+28>:	je     0x8048b43 <phase_1+35>
   0x08048b3e <+30>:	call   0x80494fc <explode_bomb>
   0x08048b43 <+35>:	mov    esp,ebp
   0x08048b45 <+37>:	pop    ebp
   0x08048b46 <+38>:	ret    
End of assembler dump.
(gdb) p 0x80497c0
$1 = 134518720
(gdb) x/s 0x80497c0
0x80497c0:	"Public speaking is very easy."
(gdb) q
A debugging session is active.

	Inferior 1 [process 2139] will be killed.

Quit anyway? (y or n) n
Not confirmed.
(gdb) y
Undefined command: "y".  Try "help".
(gdb) Quit
(gdb) quit
A debugging session is active.

	Inferior 1 [process 2139] will be killed.

Quit anyway? (y or n) yes
root@kali:~/Downloads/bigbangtheory-master# gdb sheldon1
GNU gdb (Debian 8.1-4+b1) 8.1
Copyright (C) 2018 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.  Type "show copying"
and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<http://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
<http://www.gnu.org/software/gdb/documentation/>.
For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from sheldon1...done.
(gdb) info functions
All defined functions:

File bomb.c:
int main(int, char **);

Non-debugging symbols:
0x080486e0  _init
0x08048720  __register_frame_info
0x08048720  __register_frame_info@plt
0x08048730  close
0x08048730  close@plt
0x08048740  fprintf
0x08048740  fprintf@plt
0x08048750  tmpfile
0x08048750  tmpfile@plt
0x08048760  getenv
0x08048760  getenv@plt
0x08048770  signal
0x08048770  signal@plt
0x08048780  fflush
0x08048780  fflush@plt
0x08048790  bcopy
0x08048790  bcopy@plt
---Type <return> to continue, or q <return> to quit---
