# bitwise
Terminal based bitwise calculator in curses

[![Build Status](https://travis-ci.org/mellowcandle/bitwise.svg?branch=master)](https://travis-ci.org/mellowcandle/bitwise)<a href="https://scan.coverity.com/projects/mellowcandle-bitwise">
  <img alt="Coverity Scan Build Status"
       src="https://scan.coverity.com/projects/18170/badge.svg"/>
</a>

## 

## Usage
_bitwise_ can be used both interactivly and in command line mode.

### Command line mode
In command line mode, passing a number in any base (Decimal, Hexedical & Octal) will output the number in all bases including binary representation.

_bitwise_ detects the base by the preface of the input (0x/0X for hexedecimal, leading 0 for octal, and the rest is decimal).

#### Example:

```
$ bitwise 0x12312311
Decimal: 305210129
Hexdecimal: 0x12312311
Octal: 02214221421
Size: 291.07MB
Binary:
0 0 0 0 0 0 0 0 | 0 0 0 0 0 0 0 0 | 0 0 0 0 0 0 0 0 | 0 0 0 0 0 0 0 0 | 0 0 0 1 0 0 1 0 | 0 0 1 1 0 0 0 1 | 0 0 1 0 0 0 1 1 | 0 0 0 1 0 0 0 1 
    63 - 56           55 - 48           47 - 40           39 - 32           31 - 24           23 - 16           15 -  8            7 -  0     
```

### Interactive mode
_bitwise_ starts in interactive mode if no command line parameters are passed or if the _-i | --interactive_ flag is passed.
In this mode, you can input a number and manipulate it and see the other bases change dynamically.
It also allows changing individual bits in the binary.

#### Navigation in interactive mode
To move around use the arrow keys, or use _vi_ key bindings : <kbd> h </kbd> <kbd> j </kbd> <kbd> k </kbd> <kbd> l </kbd>.

You can toggle a bit bit using the <kbd> space </kbd> key.

Leave the program by pressing <kbd> q </kbd>.

## Building from source
1. Clone the source code.
2. ./bootstrap.sh
3. ./configure
4. make
5. sudo make install

