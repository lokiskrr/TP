# TP5 : Le compilateur ton pire meilleur ami

## Sommaire

- [TP5 : Le compilateur ton pire meilleur ami](#tp5--le-compilateur-ton-pire-meilleur-ami)
  - [Sommaire](#sommaire)
- [0. Prérequis](#0-prérequis)
- [I. Programme minimal](#i-programme-minimal)
  - [1. Compilation](#1-compilation)
  - [2. Analyse du programme compilé](#2-analyse-du-programme-compilé)
  - [2. Librairie et compilation dynamique](#2-librairie-et-compilation-dynamique)
    - [A. Intro lib](#a-intro-lib)
    - [B. Intro compilation dynamique](#b-intro-compilation-dynamique)
    - [C. Tracer les appels à des librairies](#c-tracer-les-appels-à-des-librairies)
  - [3. Compilation statique](#3-compilation-statique)
  - [4. Compilation cross-platform](#4-compilation-cross-platform)
- [II. Ptits challenges de cracking](#ii-ptits-challenges-de-cracking)
  - [1. Install Ghidra](#1-install-ghidra)
  - [2. Patch manuel programme simple](#2-patch-manuel-programme-simple)
  - [3. Root-me](#3-root-me)
  - [4. Ptit chall maison](#4-ptit-chall-maison)

# 0. Prérequis

🌞 **Créer un répertoire de travail dans votre répertoire personnel**

```bash 
fata@debian:~$ pwd
/home/fata
fata@debian:~$ mkdir work
fata@debian:~$ ls
 Desktop     Downloads   Music      Public     'udo systemctl list-units -t service -a'   work
 Documents   gameshell   Pictures   Templates   Videos
fata@debian:~$ cd work
fata@debian:~/work$ pwd
/home/fata/work
fata@debian:~/work$
```

# I. Programme minimal

## 1. Compilation

```bash 
done :)
```

## 2. Analyse du programme compilé

🌞 **Retrouvez à l'aide de `readelf` l'architecture pour laquelle le programme est compilé**

```bash 
fata@debian:~/work$ readelf -h hello1
ELF Header:
  Magic:   7f 45 4c 46 01 01 01 00 00 00 00 00 00 00 00 00
  Class:                             ELF32
  Data:                              2's complement, little endian
  Version:                           1 (current)
  OS/ABI:                            UNIX - System V
  ABI Version:                       0
  Type:                              DYN (Position-Independent Executable file)
  Machine:                           Intel 80386
  Version:                           0x1
  Entry point address:               0x1000
  Start of program headers:          52 (bytes into file)
  Start of section headers:          13304 (bytes into file)
  Flags:                             0x0
  Size of this header:               52 (bytes)
  Size of program headers:           32 (bytes)
  Number of program headers:         11
  Size of section headers:           40 (bytes)
  Number of section headers:         21
  Section header string table index: 20
```

🌞 **Afficher la liste des *sections* contenues dans le *programme***

```bash 
fata@debian:~/work$ readelf -S hello1
There are 21 section headers, starting at offset 0x33f8:

Section Headers:
  [Nr] Name              Type            Addr     Off    Size   ES Flg Lk Inf Al
  [ 0]                   NULL            00000000 000000 000000 00      0   0  0
  [ 1] .interp           PROGBITS        00000194 000194 000013 00   A  0   0  1
  [ 2] .note.gnu.bu[...] NOTE            000001a8 0001a8 000024 00   A  0   0  4
  [ 3] .gnu.hash         GNU_HASH        000001cc 0001cc 000018 04   A  4   0  4
  [ 4] .dynsym           DYNSYM          000001e4 0001e4 000010 10   A  5   1  4
  [ 5] .dynstr           STRTAB          000001f4 0001f4 000001 00   A  0   0  1
  [ 6] .text             PROGBITS        00001000 001000 00005d 00  AX  0   0  1
  [ 7] .eh_frame_hdr     PROGBITS        00002000 002000 00001c 00   A  0   0  4
  [ 8] .eh_frame         PROGBITS        0000201c 00201c 000058 00   A  0   0  4
  [ 9] .dynamic          DYNAMIC         00003f8c 002f8c 000068 08  WA  5   0  4
  [10] .got.plt          PROGBITS        00003ff4 002ff4 00000c 04  WA  0   0  4
  [11] .comment          PROGBITS        00000000 003000 00001f 01  MS  0   0  1
  [12] .debug_aranges    PROGBITS        00000000 00301f 000020 00      0   0  1
  [13] .debug_info       PROGBITS        00000000 00303f 000070 00      0   0  1
  [14] .debug_abbrev     PROGBITS        00000000 0030af 000062 00      0   0  1
  [15] .debug_line       PROGBITS        00000000 003111 000054 00      0   0  1
  [16] .debug_str        PROGBITS        00000000 003165 000085 01  MS  0   0  1
  [17] .debug_line_str   PROGBITS        00000000 0031ea 000019 01  MS  0   0  1
  [18] .symtab           SYMTAB          00000000 003204 0000b0 10     19   6  4
  [19] .strtab           STRTAB          00000000 0032b4 00006a 00      0   0  1
  [20] .shstrtab         STRTAB          00000000 00331e 0000d9 00      0   0  1
Key to Flags:
  W (write), A (alloc), X (execute), M (merge), S (strings), I (info),
  L (link order), O (extra OS processing required), G (group), T (TLS),
  C (compressed), x (unknown), o (OS specific), E (exclude),
  D (mbind), p (processor specific)
```

🌞 **Affichez le code *assembleur* de la section `.text` à l'aide d'`objdump`**

```bash 
fata@debian:~/work$ objdump -M intel -j .text -s hello1

hello1:     file format elf32-i386

Contents of section .text:
 1000 5589e557 565383ec 10e84b00 000005e6  U..WVS....K.....
 1010 2f0000c7 45e54865 6c6cc745 e96f2c20  /...E.Hell.E.o,
 1020 57c745ed 6f726c64 c745f064 210a008d  W.E.orld.E.d!...
 1030 75e5bf0e 000000b8 04000000 bb010000  u...............
 1040 0089f189 facd80b8 01000000 31dbcd80  ............1...
 1050 9083c410 5b5e5f5d c38b0424 c3        ....[^_]...$.
```

## 2. Librairie et compilation dynamique

### A. Intro lib

### B. Intro compilation dynamique

### C. Tracer les appels à des librairies

🌞 **Tracez à l'aide de la commande `ldd` les *librairies* appelées par...**

```bash 
fata@debian:~/work$ ldd hello2
        linux-gate.so.1 (0xf7f6b000)
        libc.so.6 => /lib32/libc.so.6 (0xf7d25000)
        /lib/ld-linux.so.2 (0xf7f6d000)

fata@debian:~/work$ ldd ./hello1
        statically linked

fata@debian:~/work$ file hello2
hello2: ELF 32-bit LSB pie executable, Intel 80386, version 1 (SYSV), dynamically linked, interpreter /lib/ld-linux.so.2, BuildID[sha1]=052622b155dba221353280bad72c104d0f0337de, for GNU/Linux 3.2.0, with debug_info, not stripped

fata@debian:~/work$ file hello1
hello1: ELF 32-bit LSB pie executable, Intel 80386, version 1 (SYSV), dynamically linked, interpreter /lib/ld-linux.so.2, BuildID[sha1]=6b4610a23d24f9bc3672e8e6600c919b677eb703, with debug_info, not stripped
```

🌞 **Parmi les *librairies* appelées par *hello2*, déterminer le type du fichier nommé `libc.so.X`**

```bash 
fata@debian:~/work$ ldd ./hello2
        linux-gate.so.1 (0xf7f37000)
        libc.so.6 => /lib32/libc.so.6 (0xf7cf1000)
        /lib/ld-linux.so.2 (0xf7f39000) 


Type de fichier : lib.so.6
```

## 3. Compilation statique

🌞 **Affichez le type des fichiers `hello2` et `hello3`**

```bash 
fata@debian:~/work$ file ./hello2
./hello2: ELF 32-bit LSB pie executable, Intel 80386, version 1 (SYSV), dynamically linked, interpreter /lib/ld-linux.so.2, BuildID[sha1]=052622b155dba221353280bad72c104d0f0337de, for GNU/Linux 3.2.0, with debug_info, not stripped

fata@debian:~/work$ file ./hello3
./hello3: ELF 32-bit LSB executable, Intel 80386, version 1 (GNU/Linux), statically linked, BuildID[sha1]=3d2ea056ab3ccf8a9462794c5b5cf9a1b88f6822, for GNU/Linux 3.2.0, with debug_info, not stripped
```

🌞 **Affichez leurs tailles**

```bash 
fata@debian:~/work$ du -h ./hello2
16K     ./hello2

fata@debian:~/work$ du -h ./hello3
728K    ./hello3
```

## 4. Compilation cross-platform

🌞 **Affichez l'*architecture* de votre *CPU***

```bash 
fata@debian:~/work$ lscpu
Architecture:             x86_64
  CPU op-mode(s):         32-bit, 64-bit
  Address sizes:          39 bits physical, 48 bits virtual
  Byte Order:             Little Endian
CPU(s):                   1
  On-line CPU(s) list:    0
Vendor ID:                GenuineIntel
  Model name:             Intel(R) Core(TM) i5-8265U CPU @ 1.60GHz
    CPU family:           6
    Model:                142
    Thread(s) per core:   1
    Core(s) per socket:   1
    Socket(s):            1
    Stepping:             12
    BogoMIPS:             3599.99
    Flags:                fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse s
                          se2 ht syscall nx rdtscp lm constant_tsc rep_good nopl xtopology nonstop_tsc cpuid tsc_known_f
                          req pni pclmulqdq monitor ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt aes xsave avx
                          f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single fsgsbase bmi1 avx2 bmi2 invpci
                          d rdseed adx clflushopt arat md_clear flush_l1d arch_capabilities
Virtualization features:
  Hypervisor vendor:      KVM
  Virtualization type:    full
Caches (sum of all):
  L1d:                    32 KiB (1 instance)
  L1i:                    32 KiB (1 instance)
  L2:                     256 KiB (1 instance)
  L3:                     6 MiB (1 instance)
NUMA:
  NUMA node(s):           1
  NUMA node0 CPU(s):      0
Vulnerabilities:
  Gather data sampling:   Unknown: Dependent on hypervisor status
  Itlb multihit:          KVM: Mitigation: VMX unsupported
  L1tf:                   Not affected
  Mds:                    Not affected
  Meltdown:               Not affected
  Mmio stale data:        Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
  Reg file data sampling: Not affected
  Retbleed:               Vulnerable
  Spec rstack overflow:   Not affected
  Spec store bypass:      Vulnerable
  Spectre v1:             Mitigation; usercopy/swapgs barriers and __user pointer sanitization
  Spectre v2:             Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Retpoline
  Srbds:                  Unknown: Dependent on hypervisor status
  Tsx async abort:        Not affected
```

🌞 **Vérifiez que vous avez la commande `x86_64-linux-gnu-gcc`**

```bash 
fata@debian:~/work$ which x86_64-linux-gnu-gcc
/usr/bin/x86_64-linux-gnu-gcc
```

🌞 **Compilez votre fichier `hello3.c` dans un fichier cible nommé `hello4` vers une autre *architecture* que la vôtre**

```bash 
fata@debian:/$ su - root
Password:
root@debian:~# sudo apt-get install gcc-arm-linux-gnueabihf

root@debian:~# which arm-linux-gnueabihf-gcc
/usr/bin/arm-linux-gnueabihf-gcc

fata@debian:~$ ls
 Desktop     Downloads   Music      Public     'udo systemctl list-units -t service -a'   work
 Documents   gameshell   Pictures   Templates   Videos
fata@debian:~$ work
-bash: work: command not found
fata@debian:~$ cd work/
fata@debian:~/work$ arm-linux-gnueabihf-gcc -o hello4 hello3.c
fata@debian:~/work$ ls
hello1  hello1.c  hello2  hello2.c  hello3  hello3.c  hello4
```

🌞 **[Désassemblez](../../cours/memo/glossary.md#désassembler) `hello3` et `hello4` à l'aide d'`objdump`**

```bash 

```

🌞 **Essayez d'exécuter le *programme* `hello4`**

```bash 

```

# II. Ptits challenges de cracking

## 1. Install Ghidra

🌞 **Avec une commande `apt search`, déterminez si le paquet `ghidra` est disponible**

```bash 

```

🌞 **Ajouter l'URL des dépôts Kali à vos dépôts existants**

```bash 

```

🌞 **Ajoutez la clé publique des gars de chez Kali**

```bash 

```

🌞 **Mettez à jour la liste des dépôts que votre OS connaît actuellement**

```bash 

```

🌞 **Avec une commande `apt search`, déterminez si le paquet `ghidra` est disponible**

```bash 

```

🌞 **Installez le paquet `ghidra`**

```bash 

```

## 2. Patch manuel programme simple

🌞 **Récupérez le code de [`password_2.c`](../../cours/cracking/code_demo/password_2.c) sur la machine Linux et compilez-le**

```bash 

```

## 3. Root-me

## 4. Ptit chall maison

🌞 **Récupérer le flag du programme [`kaddate_challenge`](./kaddate_challenge)**

```bash 

```
