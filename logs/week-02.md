# Week 2

**Dates:** 06-29 to 07-03

## Goals

* Select/Create Database: either select a database similar to Pennylane or create our own bank of Hubbard models through QuSpin or an alternative
* Create ED Functions: compartmentalize the quantum properties calculated in Week 1 into Python functions
* Pivot to Kagome Lattices: switch from standard rectangular lattices to Kagome lattices
* Switch QuSpin framework to TeNPy: check capabilities of TeNPy and utilize Gemini for TeNPy database generation
* ED Oracle: create a second script to take the database information for calculating quantum properties
## Approach and Implementation

* Conda Download: to download TeNPy, I had to install Conda. It took a day to successfully install TeNPy, ending when I found a command to download the program from Pip as opposed to Conda.
* Database Modifications : we began by attempting to modify Pennylane's dataset, but it was too rigid (few data points) and difficult to recreate (locked objects). We pivoted to QuSpin generation, and discovered it required a lot of effort to create a variety of lattices. 
* Database Generation: We finally pivoted to TeNPy and found it to be more malleable. We were able to create a script that could generate around a hundred Kagome models with varying Hopping Terms (t1 and t2), Interaction Term (U), and lattice size (x, y, and number of sites). The model parameters and the resulting ground state energy are saved in a CSV file and the eigenvector (PSI) and waveforms are stored in a .h5 file (TeNPy waveforms format).
## Results

* Database: we now have a standardized database. It seems to work, though it can take a few minutes to calculate a single Kagome model. 
* ED Oracle: the ED Oracle has also been created, but it has not been tested. While we can feed the data to the Oracle and get a result, we do not have a baseline Kagome lattice with known answers to check with

## Notes

* TeNPy works for us! Now we just need to find a benchmark test to verify the ED Oracle.
* Stage 1 Foundation, creating the AI Model for testing and AI gate for constraints, will begin next week.
* We have not incorporated TABC, pairing vertex corrections, nor Heisenberg scale. Can we do so with TeNPy? Does the variety added in the generation have any meaningful impact?
