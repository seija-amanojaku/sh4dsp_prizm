# SH4AL-DSP (Casio Prizm/fx-CG50) Bext codegen

> [!WARNING]
> This codegen is not compatible with the fxSDK/gint (although generated `g3a` files can be edited with it), 
> and doesn't support every instruction yet (for example, DSP instructions are never generated, and asm blocks 
> will not recognise them)

This is a codegen for the [B extended compiler](https://github.com/bext-lang/b), which adds support for building 
native 'add-ins' for the Casio Prizm/fx-CG50 platform (other SuperH-based targets *may* be introduced later).

## Installation
```console
$ git clone https://github.com/bext-lang/b
$ cd b/src/codegen
$ git clone https://github.com/seija-amanojaku/sh4dsp_prizm # TODO!
$ cd ../..
$ make
$ ./build/b -tlist
``` 

## Targets and Dependencies
As written before, we only target fx-CG10/fx-CG20 and fx-CG50 (Graph 90+E) calculators. Monochrome calculators 
may be supported if someone is willing to make a target for them, and fx-CG100/Math+ with MPM are not supported, 
although we consider this an MPM issue, that will hopefully be fixed with syscall support.

No extra dependencies are required (although Casio's _official_ emulator is recommanded if you want to see how it
looks like on an actual display)!
