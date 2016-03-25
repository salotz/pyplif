## Overview ##

PyPLIF is a program/script written in Python to analyze protein-ligand interaction from the molecular docking result. It relies on [Open Babel](http://openbabel.org/wiki/Main_Page) library to read and process the molecule files from the molecular docking output.

The current version only support the _Sybil mol2_ format, but it is planned to support other format in the future release such as _pdbqt_ & _dlg_ from Autodock and Autodock Vina.

So far this program has only been tested against the output from [PLANTS](http://www.tcd.uni-konstanz.de/research/plants.php), but you can request for other kind of output support simply by entering new issue [here](http://code.google.com/p/pyplif/issues/entry?template=Review%20request) and attaching the output example.

## About PLIF ##

PLIF is stand for Protein-Ligand Interaction Fingerprinting, it is also known as SIFt (Structural Interaction Fingerprinting) or IFP (Interaction Fingerprinting). PLIF is a method to interpret protein ligand interaction (3D) into bit array form (1D), later this bit array can be used to compare how similar two interaction (with the same protein but different ligand) is using Tanimoto Coefficient.

![http://img710.imageshack.us/img710/7127/ifph1.png](http://img710.imageshack.us/img710/7127/ifph1.png)
_**Output example from the latest SVN version. The 1st line is the residue of choice, the 2nd line is ligand reference, the 2nd column is the docking score, the 3rd column is the Tanimoto coefficient, and the last one is the bit array.**_

The algorithm used in this program is based on [FingerPrintLib](http://bioinfo-pharma.u-strasbg.fr/labwebsite/download.html) by [Marcou and Rognan](http://dx.doi.org/10.1021/ci600342e). While FingerPrintLib is written in C++ this program is written in Python. Hopefully by rewriting the code in Python will help researchers in improving/developing Protein-Ligand Interaction Fingerprinting algorithm since Python is a high-level programming language that any people can learn.

Note that this work rely heavily on Open Babel library, and the molecular recognition in Open Babel is (usually) different from version to version. Several tests against many kind of ligand using several different Open Babel version have shown that **different Open Babel library version may give different result**.

## How To Use ##

Instruction on how to install and how to use included in INSTALL.txt and README.txt

## How To Cite ##

If you use this program for your work please include the following reference:

Radifar, M.; Yuniarti, N.; Istyastono, E. P. _Bioinformation_. **2013**, 9, 325.

## Author ##
Muhammad Radifar