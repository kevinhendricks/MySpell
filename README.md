MySpell
=======

*** Note:  MySpell-3.2 has been subsumed by	the Hunspell project
This repo is here just to archive some older software I	once
wrote. ***


MySpell is a simple spell checker that uses affix 
compression and is modelled after the spell checker
ispell.  

MySpell was written to explore how affix compression 
can be implemented. 

The Main features of MySpell are:

1. written in C++ to make it easier to interface with 
   Pspell, OpenOffice, AbiWord, etc

2. it is stateless, uses no static variables and
   should be completely reentrant with almost no 
   ifdefs  

3. it tries to be as compatible with ispell to
   the extent it can.  It can read slightly modified 
   versions of munched ispell dictionaries (and it 
   comes with a munched english wordlist borrowed from 
   Kevin Atkinson's excellent Aspell.

4. it uses a heavily modified aff file format that
   can be derived from ispell aff files but uses
   the iso-8859-X character sets only
 
5. it is simple with *lots* of comments that 
   describes how the affixes are stored
   and tested for (based on the approach used by 
   ispell).

6. it supports improved suggestions with replacement
   tables and ngram-scoring based mechanisms in addition
   to the main suggestion mechanisms

7. like ispell it has a BSD license (and  no 
   advertising clause)

But ... it has *no* support for adding words
to a personal dictionary, *no* support for converting
between various text encodings, and *no* command line
interface (it is purely meant to be a library).

It can not (in any way) replace all of the functionality
of ispell or aspell/pspell.  It is meant as a learning
tool for understanding affix compression and for 
being used by front ends like OpenOffice, Abiword, etc.

MySpell has been tested under Linux and Solaris
and has the world's simplest Makefile and no 
configure support.

It does come with a simple example program that 
spell checks some words and returns suggestions.

To build a static library and an example
program under Linux simply type:

tar -zxvf MySpell-3.2.tar.gz
cd MySpell
make

To run the example program:
./example ./en_US.aff ./en_US.dic checkme.lst

Please play around with it and let me know
what you think.

Please see the file CONTRIBUTORS for more info.

kevin.b.hendricks@icloud.com
(was kevin.hendricks@sympatico.ca)
