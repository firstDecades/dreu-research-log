# Week 6

**Dates:** 07-27 to 07-31

## Goals
* Initiated LangGraph Workflow: Begin constructing LangGraph agentic workflow with two nodes, NQS and Exact Oracle
* Integrate Sub-Cluster Diagonalization: Add sub-cluster diagonalization to enable exact diagonalization for large-site Kagome models
* Create Code Repository: Migrate code repository from Google Drive to GitHub
* Resolve MPS and ED Discrepancies: Balance Matrix Product State (TeNPy) and Exact Diagonalization (QuSpin) to yield same ground state energies and quantum property observables
## Approach and Implementation
* LangGraph Workflow: By using LangGraph in Python, I created a preliminary agentic workflow. After designing the initial workflow, the next task was to create the tools the AI agent can use for its task. There are two nodes in the workflow, the first being the NQS neural network and the second being an Exact Oracle for verification. Currently, only the Exact Oracle is an AI Agent, a node which can either parse through a dataset of already-calculated models for testing the NQS results, solve for the solutions not in the dataset through exact diagonalization, and possible solve for larger-site models using Sub-Cluster diagonalization (not yet implemented).
* Code Repository: Initially, the code written for the project was small enough to be stored in a formatted Google Docs for scripts. However, as the files and scripts grow more numerous and the scripts become more finalized, it seemed important to create a true repository for code. As such, I added the Jupyter Notebook folder to my GitHub repository, with an exclusion to the datasets generated from the TeNPy scripts (already in a second GitHub repository).
* Model Observable Discrepancy: While I was able to synchronize the ground state energies from MPS and ED, I noticed that the quantum properties did not match. Initially, I wanted to standardize the end results for both MPS and ED, but after a conversation with our mentor, I chose to pivot to attempting to have the Exact Diagonalization give a similar response as opposed to editing the response. Standardizing the end result would have reduced the geometric frustration that defines the Kagome lattice. If I can align the initial configurations/parameters for QuSpin and TeNPY so that they have the same conventions, I may be able to have the end results by similar/within a certain error without reducing the value.
## Results
* LangGraph: Created initial layout for the LangGraph workflow
* LangGraph Tools: Working on the Exact Oracle tool and TeNPy dataset
## Notes
* I still need to test the LangGraph workflow, but I do need to finish the tools first. To finish the tools, I need to balance TeNPy and QuSpin generations.
* [https://github.com/firstDecades/dreu-code-repo](https://github.com/firstDecades/dreu-code-repo) 
