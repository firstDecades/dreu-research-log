# Week 1

**Dates:** 06-22 to 06-26

## Goals

* Establish Stage 0 foundations: begin to set-up the validation suite for Exact Diagonalization Oracle 
* Find a valid dataset for Fermi-Hubbard models: explore different datasets available for creating a bank of training data and testing data of Hubbard models
* Research quantum properties: research and compute physical quantum properties that can be extracted from Hubbard model

## Approach and Implementation
* Dataset appropriation: what is required to simulate a Hubbard model? We utilized Google Gemini and Google Scholars Lab to locate an appropriate source of data for the Hubbard models. We settled on using Pennylane's Data set for rectangular, closed-periodicity 2x2 Fermi-Hubbard Hamiltonians, which provided us with 100 Hamiltonians.
* Exact Diagonalization Oracle: to calculate Exact Diagonalization from the Hamiltonians, we used Python libraries, specifically NumPy and SciPy. At first, we used Numpy to create a full, dense matrix from the Hamiltonians and extracting the full set of eigenvalues and eigenvectors for each of the Hamiltonians.
* Data verification: once we could calculate the eigenvalues, we compared the data given from the Pennylane dataset, specifically the ground state energies for each Hamiltonian, and the data calculated from Numpy's functions to ensure our calculations were accurate. Though I only check up to the seventh decimal, the ground state energies matched.
* Quantum properties research: after some research into the properties calculable from the Hamiltonian, we decided to focus on Double Occupancy, Charge Correlation, and Spin-Spin Correlation. These were all calculable from the ground state eigenvector, meaning that we did not need to store all of the eigenvalues and eigenvectors, just the ground states. As such, we pivoted to SciPy, its sparse matrices, and its Linear Algebra functions capable of computing just the ground states. 
* QuSpin potential: As an alternative to having a ready-made dataset of Hamiltonians, we attempted to create our own dataset through QuSpin. More research is required, though it seems that it may be too complicated to add.
## Results

* Pennylane ED Oracle: we have an initial ED Oracle set up to compute the quantum properties: Ground State Energy and Eigenvector, Double Occupancy, Charge Correlation, Spin-Spin Correlation for 2x2 Hubbard models from Pennylane.
* Dataset Limitation: We have discovered that Pennylane's dataset is not very malleable; we would need to be able to quickly edit the Hamiltonian to generate more variations. However, there is little variation in the Pennylane dataset and would be difficult to alter.
* Stage 0 Foundation: After a final meeting with Joel and Shafayat, we have set the validation benchmarks for the ED Oracle:
	1. Ground State Energy and Eigenvector + Quantum Properties
	2. Heisenberg scale and model
	3. Finite changes via Twisted Average Boundary Conditions and Pairing Vertex Corrections

## Notes

* Knowledge:  we need to research more into the Heisenberg scale and model in comparison to our work as well as TABC and pairing vertex corrections.
* Dataset: after identifying Pennylane's dataset problem, can we pivot to QuSpin for generation? Additionally, what other frameworks exist that we can use for Hubbard generation? Can we introduce TABC without breaking the model?
* Resources: Gemini transcripts and daily journal stored in CRA-DREU shared folder.
