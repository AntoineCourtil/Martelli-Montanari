# Martelli-Montanari
Projet LMC M1 INFO


$ prolog
Welcome to SWI-Prolog (Multi-threaded, 64 bits, Version 7.2.3)
Copyright (c) 1990-2015 University of Amsterdam, VU Amsterdam
SWI-Prolog comes with ABSOLUTELY NO WARRANTY. This is free software,
and you are welcome to redistribute it under certain conditions.
Please visit http://www.swi-prolog.org for details.

For help, use ?- help(Topic). or ?- apropos(Word).

?- consult('Martelli_Montanari').
true.

?- unifie([f(X,Y) ?= f(g(Z),h(a)), Z ?= f(Y)]).
system : [f(_G983,_G984)?=f(g(_G986),h(a)),_G986?=f(_G984)]
decompose : f(_G983,_G984)?=f(g(_G986),h(a))
system : [_G984?=h(a),_G983?=g(_G986),_G986?=f(_G984)]
expand : _G984?=h(a)
system : [_G983?=g(_G986),_G986?=f(h(a))]
expand : _G983?=g(_G986)
system : [_G986?=f(h(a))]
expand : _G986?=f(h(a))
X = g(f(h(a))),
Y = h(a),
Z = f(h(a)).

?- unifie([f(X,Y) ?= f(g(Z),h(a)), Z ?= f(X)]).
system : [f(_G983,_G984)?=f(g(_G986),h(a)),_G986?=f(_G983)]
decompose : f(_G983,_G984)?=f(g(_G986),h(a))
system : [_G984?=h(a),_G983?=g(_G986),_G986?=f(_G983)]
expand : _G984?=h(a)
system : [_G983?=g(_G986),_G986?=f(_G983)]
expand : _G983?=g(_G986)
system : [_G986?=f(g(_G986))]
occur check : _G986?=f(g(_G986))
false.
