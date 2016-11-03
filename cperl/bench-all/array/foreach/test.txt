#!perl

# Name: Array assignment
# Require: 4
# Desc: aelem and aelem_u, not aelemfast_lex
#

require 'benchlib.pl';

my @a = (1..30);

&runtest(45, <<'ENDTEST');

   foreach (@a) {
       $a[$_] = $_;
   }
   foreach my $i (0..$#a) {
       $a[$i] = 0; # set element with possible uoob optimization
   }

ENDTEST
