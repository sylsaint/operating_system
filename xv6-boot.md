## Finding and breaking at an address

`cd /path/to/xv6-public
nm kernel | grep _start`

output:

`
symbol value | symbol type | symbol name
8010a4ac       D             _binary_entryother_start
8010a480       D             _binary_initcode_start
0010000c       T             _start
`

*nm: list the symbols from object files `objectfile`, if no objectfile is present, assumes a.out as the file*
*D stands for the symbol is in the initialized data section, T stands for the symbol is in the text(code) section*
