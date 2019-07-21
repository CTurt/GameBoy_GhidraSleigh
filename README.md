# Game Boy Ghidra Sleigh
Ghidra Processor support for Nintendo Game Boy.

## Game Boy processor
Based on Z80 processor Sleigh that comes with Ghidra, modified to Game Boy CPU according to [this table of differences](https://gbdev.gg8.se/wiki/articles/CPU_Comparision_with_Z80).

## Install
For your convenience, the `.sla` has been prebuilt. Simply copy `GameBoy` directory to `Ghidra\Processors\` and reopen Ghidra.

## Build
If you make modifications to the `.slaspec`, you need to rebuild the `.sla`. This can be done as follows from your Ghidra directory:

    cd support
    sleigh.bat -a ../Ghidra/Processors/GameBoy/data/languages

## Usage
When importing your Game Boy ROM, set `Language` to `GameBoy`, then click `Options`, set `Block Name` to `CART`, and set `Length` to `0x4000`. This will import the first bank of the Game Boy ROM.
