Description
===========

SequentProver is a theorem prover for Propositional Minimal Logic. In current development it implements only the implication connective. 

Installation
============

SequentProver depends on the following libraries:

* love (0.7.2 or superior)
* luasocket (2.0.2-5 or superior)
* lpeg (0.11-2 or superor)

Löve is a canvas for Lua game development that we use to build the prover user interface. It can be downloaded from [the project website](https://love2d.org/).

Luasocket is a library for socket communication in Lua. It can be installed using [luarocks](http://luarocks.org/), a package manager for Lua.

Lpeg is a pattern-matching library for Lua. We use lpeg to parse input formulae in our prover. It also can be installed using [luarocks](http://luarocks.org/).

Usage
=====

Inside SequentProver directory:

1. Run the prover graphical interface

`love .`

2. Run the input terminal

`lua inputServer.lua`

3. Follow commands in the graphical interface

Input formula example
=====================

Formulae only support implication (`imp`). Parentheses are required to the right side of every subformula. 

The formula A &rarr; (B &rarr; A) has to be entered as:

`A imp (B imp (A))`