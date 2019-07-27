# The project
- Develop a functional spreadsheet.
- Written in a functional language.
- Each cell contains a functional language expression.
- The engine consits of a simple eval of each cell.
- The spreadsheet will be also a CLI/REPL.
- Raw ideas below.

# Research
- Found many similar ideas.
- None exactly the same.

## 2 most important references:
- Resolver One
- Implementing Function Spreadsheets - Peter Sestoft - 10.1.1.1025.7010.pdf [function, not functional]

# Experience
 - 40+ years of software development.
 - Languages, tools, methods, computing science, mathematics.
 - Lessons and ideas. See my blog: [http://fimdosoftware.blogspot.com/ ]
 - My goal here is to use and apply what I learned. To develop a different *user interface and development environment*. Both for developers and for end users.

# First ideas
The project started with some ideas:
 - A spreadsheet written in a funcional language.
 - A functional spreadsheet - each cell contains an executable s-expression.
 - The spreadsheet as an REPL.
 - The spreadsheet as a multiprocessing environment: each cell's s-exressions execute in parallel.
 - The CLI as an REPL, both for the execution of programs, and for the execution of commands.
 - CLI Commands are functions of the CLI language.
 - A CLI running a functional language.
 - Using the concept or universal machine as a model for: CLI, REPL, Spreadsheet, APIs, frameworks.
 - Use the idea of strict programming: no frameworks, only libraries. The program runs on a universal machine and communicate with other machines (universal or not).
 - My experience to bring a language to the interface has been positive. This includes Assembly language. No prejudice against Assembly languages. Or any language.

# Functional-spreadsheet
Some years ago (2009-2010) I had the idea of a functional spreadsheet. A spreadsheet where each cell contains a Lisp expression.

I explored the idea and considered several different spreadsheets. Like Resolver One, which was mentioned to me by my friend Luciano Ramalho (author of Fluent Python). This is a spreadsheet which accepts Python programs in the cells. And which converts the spreadsheet in a Python program and vice-versa. Interesting.

There are several other different spreadsheets. References in my blog (December 10, 2010):

http://fimdosoftware.blogspot.com/2010/12/spreadsheets-looking-around.html

None has exactly my idea.

There is also the spreadsheet example in the SICP book. And the spreadsheet in Emacs. But these are conventional spreadsheets. Work like Excel, but written in Scheme. Or Lisp. Or a different language.

The difference is that if each cell contains a Lisp expression, the execution of the spreadsheet is extremely simple. It consits of simply eval(cell). That is it! No parser, no difference between numbers and formulas and strings.

The complete Lisp program (minus the two dimensional visualization) for my spreadsheet is:

    (mapcar (function eval) spreadsheet)

I mentioned this idea in my personal blog (March 7, 2010).

The strenght of this idea come from the basic idea of a universal machine: program and data are the same. Which is preserved in Lisp.

From this we can think of complete system built starting with a spreadshhet, we can think of multi-processing where each cell of a spreadsheet starts a process, and so on.

## Spreadsheet references
Several cases. See my directory, PSABA, urls in bookmarks, fim do software blog, github, Resolver one and more.

Could be used by the client: https://dzone.com/articles/keikai-spreadsheet-for-big-data

# REPL and CLI
What is the machine behind the idea of a spreadsheet? REPL. Read-Evaluate-Print-Loop

And how do we use Lisp, Scheme and also Python? REPL again. As far as I know, the first use of REPL was the LISP interpreter, by Steve Russell.

And what about a CLI? It's again a REPL. Plus a scripting language like Bash. The REPL is the engine of a universal machine.

So, why not generalize: use a language like Python as the CLI language. Or Lisp (or Scheme, or ...). Convert the CLI commands in functions of the language. This should be easy. Et voilá!

The occasional user of the CLI will not even notice he is using a complete programming language. And the programmer has a complete and unified environment. He can also use the CLI commands as functions in his programs.

It can be noticed that the CLI REPL works with one command per use. We can consider this to be a spreadsheet with only one cell. And we can generalize to a CLI as a spreadsheet with a two-dimensional user interface.

We can put multiprocessing in that spreadsheet, where each cell starts a program (LISP expression). All programs run in parallel.

## CLI References
See ///home/gcoen/Dropbox/CLI project/]

https://blog.heroku.com/open-cli-framework   Heroku secific? To check.

https://dzone.com/articles/why-the-command-line-why-now:

		The Command Line Reinvented for Modern Developers: net-cli-reinvented-june-2017.pdf
		
		Gmail - Learn More about CLI and What's Next in .NET.pdf
		
https://www.quora.com/Why-do-so-many-Linux-users-prefer-the-command-line-to-a-GUI

https://opensource.com/article/18/5/3-python-command-line-tools

https://thoughtbot.com/upcase/videos/lets-build-a-cli

Evaluate / do: https://stormpath.com/blog/building-simple-cli-interfaces-in-python

http://docopt.org/

To relate the CLI language with the CLI (Common Language Infrastruture of .Net)?

Check L#, Lisp#, A#, IronScheme, Algol68? Ada?

https://www.quora.com/Which-programming-language-should-I-use-for-a-command-line-tool

Writing and publishing command-line applications in Node.js is incredibly simple. There are frameworks that help you build fully-functional applications in no time, like Vorpal.js or Commander.js.

https://stackoverflow.com/questions/1891948/what-language-should-i-learn-to-create-command-line-scripts-and-guis

https://superuser.com/questions/349481/command-prompt-in-windows-and-linux-what-is-their-language-called

https://opensource.com/article/18/7/node-js-interactive-cli

https://www.infoq.com/articles/azure-cloud-shell

http://click.pocoo.org/5/   Python libray for CLI

https://www.quora.com/Can-Julia-replace-Common-Lisp-for-non-numerical-computing   *** Lisp parser for the CLI! ***

## REPL references
https://repl.it/

To run in Python? In Webassembly?

https://tomassetti.me/introduction-to-webassembly/

https://dzone.com/articles/introduction-to-java-bytecode

https://www.infoq.com/news/2018/04/webassembly-studio

https://blog.scottlogic.com/2018/04/26/webassembly-by-hand.html

https://www.infoq.com/news/2019/04/wasi-wasm-system-interface   *** important!

https://medium.com/@robaboukhalil/porting-games-to-the-web-with-webassembly-70d598e1a3ec

https://opensource.com/article/19/4/command-line-playgrounds-webassembly

https://www.quora.com/Why-should-I-learn-JavaScript-once-WebAssembly-is-available

https://www.quora.com/Why-do-so-many-developers-think-the-future-of-web-development-is-WebAssembly

https://hacks.mozilla.org/2018/10/webassemblys-post-mvp-future/



In Javascript?

Implement some commands

https://superuser.com/questions/349481/command-prompt-in-windows-and-linux-what-is-their-language-called

Implement usual commands from bash, powershell, etc...

Attention, Python has:   *****

		cmd  	Build line-oriented command interpreters.
		
		code	Facilities to implement read-eval-print loops.
		
		(see https://docs.python.org/3/py-modindex.html)
		
		There is also a csv module
		
# User Interface
The Windows-GUi has proven to be impractical for may users. Frequently someone asks "how can I do xxx?". The command line model is more clear to the occasional, non-computer familiar, or old user. Why not let the user work with the CLI?

Users prefer commands to windows and menus. Let's transform the CLI commands in functions of a language ( (Python, Scheme...). The REPL of the CLi is the interpreter of this language. Commands are input in the same way as a programmer inputs instructions. Users and programmers share the same interface.

The REPL is the engine of this universal machine.

And do not limit this machine to an interpreted language. To compile should be an option.

Note that the browser is a more intuitive interface. Check the possiblity of running this UI in the browser. Perhaps compiling to WebAssembly.

# Implement a Lisp as the CLI language
Picolisp?

Interpreter + compiler?

Python? in Lisp? A Python compiler? To machine code?

https://fr.quora.com/A-quoi-sert-lAST-g%C3%A9n%C3%A9r%C3%A9-par-Clang-Est-ce-%C3%A0-partir-de-ce-nouveau-format-texte-que-le-code-assembleur-est-g%C3%A9n%C3%A9r%C3%A9

(A quoi sert l'AST généré par Clang ? Est-ce à partir de ce nouveau "format texte" que le code assembleur est généré ?)

See above + documentation explaining the Python compiler (CPython), the use of C, etc... Check stackoverflow.

https://www.quora.com/Do-some-Lisp-programmers-desire-modern-Lisp-which-is-considerably-different-than-Clojure   Modern Lisp? ABCL? Use Jvm? Or other VM?

CLI commandes will be functions of the language.

Note: for compiler, see GCC   https://opensource.com/article/18/9/happy-birthday-gnu

Attention: Google project of a Lisp, Schism, which compiles to... WebAssembly

https://www.quora.com/Why-is-there-no-Lisp-by-Google

https://github.com/google/schism

https://norvig.com/python-lisp.html

https://www.quora.com/Is-there-a-Clojure-dialect-targeting-Python   Hy   ****

# No to frameworks, yes to libraries
Frameworks are a pain. See various references in my blog. Make programs loose the linearity, make them difficult to debug, make the programmer user of a pre-defined pattern, not a problem solver.

On the other side, a (Turing) complete language needs only libraries. A lot of them. A strong ecosystem with functions for every need.

So, develop functions. Many.

# Concurrency?
https://stormpath.com/blog/building-simple-cli-interfaces-in-python

See Gnu parallel:  https://opensource.com/article/18/5/gnu-parallel

Using the functional spreadsheet with each cell being a process

Also an advanced editor for the cells. And the cell acting as slides of a presentation.

https://github.com/mleibman/SlickGrid   A lightning fast JavaScript grid/spreadsheet

jpillora/node-edit-google-spreadsheet   A simple API for editing Google Spreadsheets

and more in github and stackoverflow.

https://github.com/arianneg/Spreadsheet

Implement memory management? In WebAssembly? Graphs?

Check Chrome OS.

# Computer Science
My experience is that sticking with rigor to the fundamentals of computer science lead to solid, simple and efficient software.

Have always in mind the concept of Universal Machine. Structure the software not in layers but in machines exchanging messages. This applies to REPL, to function calls, to APIs.

Means to study the concept of Universal Machines. Turing, Von Neuman, Moore, Kolmogorov-Uspensky, lambda calculus. Study functions. Category Theory.

Check also linear algebra applied to programs as a tool to  validate the correctness of a program.

# Learn an teach
At each step and study phase, organize the knowledge as a course. Publish it.

# The Project
Unified CLI. Programming language(s) as the scrip language. CLI commands are functions of the language. REPL as a functional spreadsheet input/ouput tool.
   
# The Method
- Software development.
- Tools (languages, editors): eclectic.
- Use existing software, libraries, tools. Open source.
- Check if the proposed software already existes: compilers, editors. Special note: JupyterLabs seems to have implemented several of these ideas. Like for example the CLI command as a function of the language. Review Jupyter.
- Keep everything *simple*: avoid transpilers, avoid several layers of software. A program should be translated from the language, high or low level, to machine code. OK to check webassembly, ok to try to run in the browser as an alternative. But avoid transpilers. Avoid loss of performance due to running on top of other software. The software should even run on UEFI.

# The Plan
- The functional spreadshhet
- the CLI
- Implement the REPL as a language: Scheme? Python?
- CLI commands as functions of the language 
- Concurrent Processing + two-dimensional interface
- Memory management
- Implement more CLI commands
- Libraries, libraries, libraries: more functions

# References
(some in Portuguese)

## General
https://sites.google.com/site/gcoendeposito/sicp-discussao-ideias-planilh

http://fimdosoftware.blogspot.com/2010/12/spreadsheets-looking-around.html

https://sites.google.com/site/gcoendeposito/sicp-discussao-ideias-planilh

https://docs.google.com/viewer?a=v&pid=sites&srcid=ZGVmYXVsdGRvbWFpbnxnY29lbmRlcG9zaXRvfGd4OjJlYWM0MmZmMTMwOWFhM2M Desunivesalização do software

https://fimdosoftware.blogspot.com/2013/04/spreadsheet-programming-problems.html

https://fimdosoftware.blogspot.com/2013/02/spreadsheet-as-model.html

