# LR(0) DFA Generator/Renderer

Rendering the DFA requires the Graphviz library: https://pypi.python.org/pypi/graphviz

Users may pass an input grammar as a string with the following format:

N -> prod1 | prod2 | ...
Where N is a nonterminal and prod is a production of N.\
Unique symbols must be separated by whitespace. Aa != A a\
Nullable productions may be represented with λ or the keyword LAMBDA.

E.g.\
grammar=\\\
"""\
S -> A | B\
A -> a b c\
B -> identifier\
"""

Output:\
![alt text](https://github.com/woodleyi/LR0-DFA-Generator/blob/master/DFA.svg)

Pass the grammar to an instance of DFA and the automaton will be constructed!\
Calling DFA.render() produces a GV file and a file of whichever format the user
passes (defaults to SVG).
