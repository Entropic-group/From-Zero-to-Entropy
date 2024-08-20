# Operating Systems: Three Easy Pieces

## Introduction

Learning operating systems can be tricky, and this separate page helps address this issue. It contains more guidance, resources, and two tracks to assist you with this huge topic. Let's get some sense for the two available approaches:

- `Base`: a more basic approach that provides all the fundamental knowledge about operating systems.
- `Extended`: more intensive and detailed approach, ideal for those who plan on specializing in systems programming and low-level coding.

## Base Approach

To begin strong, read the free online book `Operating Systems: Three Easy Pieces`

You also will need a Unix/Linux system, command line tools, and a C compiler (such as GCC or Clang). On Windows, you can install Ubuntu in a virtual machine, or use WSL (Windows Subsystem for Linux). Mac OS is Unix-like, so it should be OK to use.

### Course Links

* [Book](https://pages.cs.wisc.edu/~remzi/OSTEP/)
* [Homework](https://pages.cs.wisc.edu/~remzi/OSTEP/Homework/homework.html)
* [Homework Source Code Repo](https://github.com/remzi-arpacidusseau/ostep-homework)
* [Homework Solutions](https://github.com/xxyzz/ostep-hw)

A common language to work with operating systems is C (which is sometimes called a "system-level language"), and you will need some knowledge of it. The free book [Modern C](https://hal.inria.fr/hal-02383654/file/ModernC.pdf) by [Jen Gustadt](https://gustedt.gitlabpages.inria.fr/modern-c/) and the [CS50 Manual pages](https://manual.cs50.io) are helpful resources. Another useful resource is this list of [solutions](https://github.com/xxyzz/ostep-hw).

## Extended Approach

If you choose this path, be prepared to dig into the world of operating systems! It is challenging but highly interesting and useful. But first,  prerequisites:
- C. You'll need more advanced knowledge of C for this path, more than one would need for the base approach above. Refer to the resource list on this page for learning materials.
- I would recommend finishing both parts of Nand2Tetris, it'll give you some useful knowledge.

### Learning Materials

* [Course website](https://pages.cs.wisc.edu/~remzi/Classes/537/Spring2018/)
* [Book](https://pages.cs.wisc.edu/~remzi/OSTEP/)
* [Lecture videos](https://pages.cs.wisc.edu/~remzi/Classes/537/Spring2018/Discussion/videos.html)
* [Homework](https://pages.cs.wisc.edu/~remzi/OSTEP/Homework/homework.html)
* [Homework Source Code Repo](https://github.com/remzi-arpacidusseau/ostep-homework)
* [Homework Solutions](https://github.com/xxyzz/ostep-hw)
* [Projects](https://github.com/remzi-arpacidusseau/ostep-projects)
* [xv6](https://github.com/mit-pdos/xv6-public)

### Running the Projects

This course was originally taught as CS 537 at the University of Wisconsin by the author of the OSTEP textbook, which means that the homework and projects were written with those students as a target audience and designed to be run on UWisconsin lab computers with specific software versions pre-installed for students. 
In order to run the homework and projects on Linux or macOS, you'll need to have all of the following programs installed:

* `gcc`
* `gas`
* `ld`
* `gdb`
* `make`
* `objcopy`
* `objdump`
* `dd`
* `python`
* `perl`
* `gawk`
* `expect`
* `git`

You will also need to install `qemu`, but it is recommended using the patched version provided by the xv6 authors; see [this link](https://pdos.csail.mit.edu/6.828/2018/tools.html) for details.

On macOS, you'll need to install a cross-compiler `gcc` suite capable of producing x86 ELF binaries; see the link above for details as well.

On Windows, you can use a Linux virtual machine for the homework and projects. Some of these packages are not yet supported on Apple M1 computers, and virtual machine software has not yet been ported to the new processor architecture; some students have used a VPS to do the homework and projects instead.

Next, clone the `ostep-homework` and `ostep-projects` repositories:
```sh
git clone https://github.com/remzi-arpacidusseau/ostep-homework/
git clone https://github.com/remzi-arpacidusseau/ostep-projects/
cd ostep-projects
```

You'll have to clone [the `xv6-public` repository](https://github.com/mit-pdos/xv6-public) into the directory for each xv6-related OSTEP project. You could use the same copy for all the projects, but we recommend using separate copies to avoid previous projects causing bugs for later ones. Run the following commands in *each* of the `initial-xv6`, `scheduling-xv6-lottery`, `vm-xv6-intro`, `concurrency-xv6-threads`, and `filesystems-checker` directories.

```sh
mkdir src
git clone https://github.com/mit-pdos/xv6-public src
```

### Resources

#### C

A great book to learn C is Jens Gustedt's *Modern C*, which is [freely available online](https://hal.inria.fr/hal-02383654/file/ModernC.pdf). it is not long and will set you up very solidly with C knowledge. Also, make sure to do the exercises! 

Additional resources (optional):
* [CS 50 Manual Pages](https://manual.cs50.io): a great reference for looking up C library functions; most functions include both the usual manual as well as a beginner-friendly "less comfortable" option.
* [cdecl](https://cdecl.org): a tool to translate C gibberish into English.
* [C track on exercism.org](https://exercism.org/tracks/C): additional practice exercises.
* [Secure Coding Practices in C and C++](https://www.amazon.com/dp/0321822137): if you want to understand why other C resources are so unsafe.

#### x86 Architecture and Assembly Language

Nand2Tetris has already introduced most of the concepts you'll need to understand systems and computer architectures, so now you just need to port that knowledge to the real-world (32-bit) x86 architecture.

The easiest way to do that is by watching a subset of the lectures from the *Computer Systems: A Programmer's Perspective* course (or reading the matching chapters in the [textbook](https://www.amazon.com/dp/013409266X) of the same name). Take a look at those lectures:

* [Machine-Level Programming I: Basics](https://scs.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=6e410255-3858-4e85-89c7-812c5845d197)
* [Machine-Level Programming II: Control](https://scs.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=fc93c499-8fc9-4652-9a99-711058054afb)
* [Machine-Level Programming III: Procedures](https://scs.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=2994255f-923b-4ad4-8fb4-5def7fd802cd)
* [Machine-Level Programming IV: Data](https://scs.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=03308c94-fc20-40d8-8978-1a9b81c344ed)
* [Machine-Level Programming V: Advanced Topics](https://scs.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=3f0bf9ca-d640-4798-b91a-73aed656a10a)
* [Linking](https://scs.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=0aef84fc-a53b-49c6-bb43-14cb2b175249)

Some other resources (optional):
* [CPU Registers x86](https://wiki.osdev.org/CPU_Registers_x86): good for looking up specific registers.
* [*PC Assembly Language*](https://pdos.csail.mit.edu/6.828/2018/readings/pcasm-book.pdf): a short book on x86 assembly.
* [GCC Inline Assembly HOWTO](https://www.ibiblio.org/gferg/ldp/GCC-Inline-Assembly-HOWTO.html): a guide to writing assembly code inside a C program.
* [*Intel 80386 Programmer's Reference Manual*](https://pdos.csail.mit.edu/6.828/2018/readings/i386.pdf): the official (and huge) resourcefrom Intel.

#### xv6

The xv6 authors provide a [book](https://pdos.csail.mit.edu/6.828/2018/xv6/book-rev11.pdf) that you can read alongside the source code. There's also a handy line-numbered [PDF version](https://pdos.csail.mit.edu/6.828/2018/xv6/xv6-rev11.pdf) of the code with an index to see exactly where each function or constant gets used.

[Here](https://github.com/YehudaShapira/xv6-explained) you can find an in-depth explanation of the xv6 code.

Also [here](https://www.youtube.com/playlist?list=PLbtzT1TYeoMhTPzyTZboW_j7TPAnjv9XB) is an excellent video series walking through much of the xv6 code.

#### Some extra stuff

You'll need a general sense of how Makefiles work in order to use the Makefile for xv6. [This tutorial](https://makefiletutorial.com) covers much more than you need; just read the "Getting Started" and "Targets" sections.

