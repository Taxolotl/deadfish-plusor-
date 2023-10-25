Deadfish-PlusOr-
==============================

# Overview

Deadfish is a joke programming language.  According to the [esoteric programming language wiki](http://www.esolangs.org), a joke programming language is one that

>is not of any interest except for potential humor value. Generally speaking, it is completely unusable for programming even in theory

One such joke language is Deadfish, which got its name from

>Deadfish was originally going to be called fishheads as programming in this language is like eating raw fish heads. However, due to the limiting features of the language, programming in this language became like eating (and having to smell) dead, rotting fish heads, an experience not often generally considered pleasurable.

Nevertheless, the wiki page for Deadfish contains implementations in 65 different languages including C, C#, C++, Chicken, Clever, COBOL, and Commodore 64 BASIC to name just the C's.

Deadfish has been extended to Deadfish-PlusOr-(Pronounced "Deadfish Plus Or Minus"), which is based on the original Deadfish language.  For what is probably a good reason,  Deadfish-PlusOr- remained unimplemented... until today.

# Deadfish Language Features

A Deadfish program has a single integer accumulator variable, which is initialized to zero.  The programming language defines only four operations

|cmd| description                                                                               |
|:-:|:------------------------------------------------------------------------------------------|
| i | This increments the accumulator                                                           |
| d | This decrements the accumulator                                                           |
| s | Squares the value in the accumulator                                                      |
| o | Outputs the accumulator                                                                   |

If the accumulator becomes -1 or 256, it is reset to zero.

# Deadfish~PlusOr- Language Features

Deadfish~ is based on the Deadfish programming language, and inspired by the [BrainF**k](https://github.com/TryItOnline/brainfuck) language.  Programs have the same single integer accumulator variable as for Deadfish, which is initialized to zero, and has the same behavior around values -1 and 256.  The language is defined via MY MIND, which contains the following table of supported commands

|cmd| description                                                                               |
|:-:|:------------------------------------------------------------------------------------------|
| + | This increments the accumulator                                                           |
| - | This decrements the accumulator                                                           |
| . | Makes the accumulator a character                                                         |
| > | Outputs the accumulator                                                                   |
| ^ | Squares the value in the accumulator                                                      |
| / | Square roots the value in the accumulator, and rounds up                                  |
| {}| Instructions inside the curly braces loop for zero to ten times with an increment of one  |
| ()| If the accumulator is not zero then execute the statement inside once                     |
| ! | Stop                                                                                      |
| * | Hello, World! greeting is displayed                                                       |

The code performs no error checking, and invalid commands or incorrectly nested braces are skipped silently, just like the original author of Deadfish would have wanted.

#Usage

The source code is entirely contained in ``deadfishPoM.py``.  Evaluate Deadfish strings with the ``deadfishPoM.deadfish`` method.

```python
>>> import deadfish
>>> deadfish.deadfish("++^++++^{+.}{+.}+.+.+.+.+.+.")
ABCDEFGHIJKLMNOPQRSTUVWXYZ
```

There is also a CLI for Deadfish~, which can be accessed with ``deadfishPoM.deadfish_cli()``

```
>>> deadfish.deadfish_cli()
>> +++>
3
>> *
Hello, World!
```

# Examples

From ``deadfish_cli()``:

```
>> ++^++++^++++++++.++++++++++++++++++++++++++++++++++++++++.+++{.}---------.-------.++++++++++.-------.
Horrrrrrrrrrible
>> >
101
>> h
Hello, World!
```

This example shows the standard queries from the top of the Deadfish wiki page, demonstrating that arithmetic works just as one would 'expect' in Deadfish
```
>>++^^^>++^^+^>
0289
```
