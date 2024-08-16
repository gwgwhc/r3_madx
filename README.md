# R3 MAD-X Workbooks

This is a collection of jupyter notebooks that simulate the Rare-Radioisotope Ring (R3) at RIKEN, Japan using the MAD-X program.
Contained is the sequence file (`.seq`) for construction of the ring and jupyter notebook files for interfacing with MAD-X via [cpymad](https://github.com/hibtc/cpymad) for combined control and analysis. The sequence file and some aspects of the code are adapted from the MAD-8 file by Y. Yamaguchi.

There are three workbooks. `mad_workbook.ipynb` contains a high resolution beta function plot for one turn using the thin-lens approximation `makethin` and geometrical survey of the Ring. `mad_workbook_ptc.ipynb` uses the PTC tracking module to simulate multiple revolutions of the ring using a thick-lens approximation. It observes the behaviour at a tracking point which coincides with the newly planned position-sensitive Schottky detector denoted by `bpm_schottky` in the sequence file.

`r3_ptracker.ipynb` is the current working notebook and is a predecessor to an application catered more towards general users. Particles are started with a random gaussian position and angle. The position and its x projection are plotted.

### Installation of MAD-X and cpymad
An up-to-date MAD-X version is already contained within cpymad, thus installation is easily carried out using `pip install cpymad` if you have an existing python installation. MAD-X can also be controlled via MAD-X files and a separate installation if you don't wish to use python. More information and documentation can be found at the MAD-X site [here](https://MAD-X.web.cern.ch).
