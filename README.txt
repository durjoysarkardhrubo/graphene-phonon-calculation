This directory illustrates the usage of fix-phonon to calculate the dynamical
matrix as well as phonon dispersion curve for Graphene based on a Tersoff potential.

The files under this directory:

 1) Graphene.bin.6000000   : last output binary file by fix-phonon
 2) Graphene.log           : log file for fix-phonon
 3) SiC.tersoff            : Tersoff potential file for SiC
 4) data.pos               : LAMMPS input file
 5) pdisp.dat              : phonon dispersion data from Graphene.bin.6000000
 6) in.disp                : input file to get disp.dat by phana
 7) in.graphene            : LAMMPS input file
 8) log.lammps             : LAMMPS log file
 9) map.in                 : LAMMPS input file for fix-phonon
10) pdisp.eps              : figure of phonon dispersion curves
11) plot.disp              : gnuplot script to generate pdisp.eps
12) pdisp.gnuplot          : gnuplot script to generate pdisp.eps (auto generated)
13) README                 : this file

To run this example, simply invoke: 
-> lmp -in in.graphene -screen none

Once done, one can use the auxiliary analysing code "phana" to obtain "pdisp.dat"
-> phana Graphene.bin.6000000 < in.disp

And then use the gnuplot script file "plot.disp" to generate pdisp.eps:
-> gnuplot plot.pdisp

The resultant ``pdisp.eps'' shows the measured phonon dispersion.

NOTE: the binary file provided here might be unreadable on some computers because of
      incompatibility between different architectures.

Author: Ling-Ti Kong, konglt@sjtu.edu.cn
Nov 2015
