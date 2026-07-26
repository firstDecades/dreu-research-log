# Week 5

**Dates:** 07-20 to 07-24

## Goals
* Access to DeltaAI Computation: Get access to DeltaAI log-in and GPU capabilities
* Improve Database Generation: Fix issues with TeNPy database generation script
* Resolve Project Continuation Issues: Create a plan for future progress for property prediction framework, whether Neural Networks or Agentic Loop
## Approach and Implementation
* DeltaAI Allocation: Through NCSA Allocations, our mentor created a project to get us access to GPU computation. I now have access to DeltaAI's GPU clusters should I need more processing power. I currently do not need the access, but it will be helpful once we progress further into neural networks and begin building our framework.
* Database Modifications: During my verification process, I noticed that there was a bug where the Twisted-Boundary Condition was omitted from the Hamiltonian constructor, resulting in the twist loops happening without any changes to the Hamiltonian. Additionally, I created two test kagome models (3-site and 12-site) and verified through the Pennylane software that the calculated ground state energies were correct. 
* Database Generation: Before the database modifications, I attempted to test how long it would take to generate the Kagome models. I began to model the three-site generation for 300 models, but I did not notice the parameters were wrong: the model was set to nine sites as opposed to three sites. The generation took eight hours to complete. In comparison, after I verified that the database was generating correctly, I fixed the parameters and ran the generation again, with the 300 models being generated in 50 minutes. 
* Neural Networks: We met with our mentor on Friday, where we decided to pursue two frameworks simultaneously. Previously, we were focusing on creating/repurposing a neural network to able to predict quantum properties. We had found a repository of pre-trained AI models on HuggingFace that we could possibly repurpose, and we are still looking for a viable model. The issue with this course is that there is already existing research in using neural networks to solve the Hubbard model, albeit not for the quantum properties. Our second track is to create an Agentic Loop that can parse through research papers on solving mathematical models and attempt to create its own framework for predicting properties. This is still in planning, but I am looking into LangGraph for programming this loop. It will hopefully be viable.
## Results

* ED Oracle: The database generation has been successfully modified and verified*. We are now able to create our ED Oracle when needed.
* Project Scope: We have split our project course in two and pursuing both Neural Networks and Agentic AI.
## Notes
* I selected LangGraph because it is a free framework to use, and it is capable of strictly defining the expected workflow.
* We have access to DeltaAI through the NAIRR Portal, but we still need to see if we can use it. Most likely, if the neural network path comes to fruition, we can use the GPU clusters.