# Functional-spreadsheet

Some years ago (2009-2010) I had the idea of a functional spreadsheet. A spreadsheet where each cell contains a Lisp expression.

I explored the idea and considered several different spreadsheets. Like Resolver One, which was mentioned to me by my friend Luciano Ramalho. This is a spreadsheet which accepts Python programs in the cells. And which converts the spreadsheet in a Python program and vice-versa. Interesting.

There are several other different spreadsheets. References in my blog (December 10, 2010):

  http://fimdosoftware.blogspot.com/2010/12/spreadsheets-looking-around.html

None has exactly my idea.

There is also the spreadsheet example in the SICP book. And the spreadsheet in Emacs. But these are conventional spreadsheets. Work like Excel, but written in Scheme. Or Lisp. Or a different language.

The difference is that if each cells contains a Lisp expression, the execution of the spreadsheet is extremely simple. It consits of simply eval(cell). That is it! No parser, no difference between numbers and formulas and strings.

The complete Lisp program (minus two dimensions visualization) for a spreadsheet is:

  (mapcar (function eval) spreadsheet)

I mentioned this idea in my personal blog (March 7, 2010).

The strenght of this idea come from the basic idea of a universal machine: program and data are the same. Which is preserved in Lisp.

From this we can think of complete system built starting with a spreadshhet, we can think of multi-processing where each cell of a spreadsheet starts a process, and so on.

# REPL

What is the machine behind the idea of a spreadsheet? REPL. Read-Evaluate-Print-Loop

An how do we use Lisp, Scheme and also Python? REPL again. As far as I know, the first use of REPL was the LISP interpreter, by Steve Russell.

And what about a CLI? It's again a REPL. Plus a scripting language like Bash.

The REPL is the engine of a universal machine.

So, why not generalize: use a language like Python as the CLI language. Or Lisp (or Scheme, or ...). Convert the CLI commands in functions of the language. This should be easy. Et voilá!

The occasional user of the CLI will not even notice he is using a complete programming language. And the programmer has a complete and unified environment. Also can use the CLI commands as functions in his programs.

It can be noticed that the CLI REPL works with one command per use. We can consider this to be a spreadsheet with only one cell. And we can generalize to a CLI as a spreadsheet with a two-dimensional user interface.

We can put multiprocessing in that spreadsheet, where each cell starts a program (LISP expression). All programs run in parallel.

# UI
The Windows-GUi has proven to be impractical for the user. Frequently he asks "how can i do xxx?". The command line model is more clear to the occasional, non-computer familiar, or old user. The browser is a more intuitive interface.

Why not let the user work with the CLI?

# The Project
Unified CLI. Programming language(s) as the scrip language. CLI commands are functions of the language. REPL as a spreadsheet input/ouput tool.

# The Plan
A. the CLI
B. Implement the REPL as a language: Scheme? Python?
  CLI commands as as functions of the language 
C. Concurrent Processing + two-dimensional interface
D. Memory management
E. Implement more CLI commands
F. Libraries, libraries, libraries: more functions


# My references
(some in Portuguese)

https://sites.google.com/site/gcoendeposito/sicp-discussao-ideias-planilh

http://fimdosoftware.blogspot.com/2010/12/spreadsheets-looking-around.html


