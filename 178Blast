#!/usr/bin/perl -w
use strict;

my $dir= "/data1/metagenomics/data/2013_6_3/178";

opendir   DIR,   $dir;
my @dir=readdir   DIR;

foreach (@dir){
    if(/\.uniq/){
        my $file  = $dir."/".$_;
  	my $str = "mpirun -np 16 mpiblast -i $file -p blastx -o $_".".blastx -d nr -e 0.00001 -v 10 -b 10";

        print $str,"\n";
`$str`;
        print "$file blastx finish!\n\n\n";

    }
}
