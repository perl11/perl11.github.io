#!perl

# Name: for (@ary) loop
# Require: 4
# Desc:
#

my @ary = (1 .. 10_000);

require 'benchlib.pl';

&runtest(70, <<'ENDTEST');

    for (@ary) {
	$foo = $_;
    }

ENDTEST
