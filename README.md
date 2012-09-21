perl11.github.com
=================

5 + 6 = 11

p2 = 1 + 1

Perl 11 is an umbrella name to start separating perl5 into pluggable parsers, 
the AST (currently only the optree, in mem or serialized),
and the vm/runloop.

Then to allow multiple pluggable versions of each of those (concurrently).

This is all doable already without p5p.

The AST might be serialized from/to .pmc (readable by perl already),
.pbc, .class and so on, depending on the used vm.