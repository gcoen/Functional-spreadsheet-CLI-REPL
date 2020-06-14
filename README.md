This project is based on the convergence of three themes: Functional Spreadsheet, REPL, CLI

## Functional Spreadsheet
Spreadsheet are frequently considered functional programming. Some even say spreadsheet is Turing-complete. However, the idea of having a spreadsheet use a funciontal language in the cells expressions has not be explored. There are few papers and projects on this idea. This is strange since functional programming can be used for a spreadsheet engine. And use of functional expressions in the cells lead to a very simple engine. Here is a one-liner for a functional spreadsheet:

    (mapcar (function eval) spreadsheet)

The idea here is to develop a complete functional spreadsheet: both engine and cell expressions will be functional.

A review of the reference shows that this idea has been partially applied. Python Resolver/one, SIAG, and more.

## REPL
A spreadsheet can be view as a REPL: you write a formula, hit Enter, the spreadsheet recalculate all the formulas and show the results. We can think the spreadsheet as a bi-dimensional REPL. A generalization of the one-liner REPL.

## CLI
CLI is a REPL. Commands are read and executed. Frequently the CLI accepts a scrip language. It's a generalization of the REPL. Here again, a functional language could be used as the script language. Remembering that the first REPL was the McCarthy Lisp. Commands would be functions of the language.

So, we can put together the ideas of functional spreadsheet, executing functional expressions, acting as a REPL, useful as a bi-dimensional CLI. 

We can find similar ideas in, eg. Jupyter.

## Theory
The generalizations suggested here come from the fundament of computing, the idea that program and data are the same thing. Coming from Godel, Turing, Church, Von Neumann.

## Practical applications
The main driver of this project is to explore applications of Functional Spreadsheets, their performance (speed, memory used, practical funcionalities).

Some first applications:
- Conversion of a spreadsheet to a progam
- Use of spreadsheet as input or output of a program
	- note here the need of this due to the widespread  use of spreadsheets in offices

## Multiprocessing and more to explore
An evolution of the functional spreadsheet could be applying multiprocessing for the calculation of the cells value. Each cell acting as an independent process. This could speed the calculation but the dependencies of the formula has to be carefully managed.

A functional spreadsheet can also be an IDE for functional program development.
