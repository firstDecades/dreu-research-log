# Week 4

**Dates:** 07-13 to 07-17

## Goals
* TeNPy Consolidation: Merge model generation and quantum property calculation into single script.
* TABC Integration: Integrate Twisted Boundary Conditions (Averaged) into TeNPy generation.
* Verify ED Oracle: Find a base-case or edge case to verify TeNPy generation (ground state energy verification should do)
* Deep Learning Research: Find a framework for training, preferably a pre-trained neural network
* Establish Compute Access: Complete onboarding for UCLA (computer access) and DeltaAI (GPU access)
## Approach and Implementation
* TeNPy Generation: The TeNPy generation works, but it is missing one capability discussed in our pre-research stage: Twisted Average Boundary Conditions. We also decided to increase the size of our database, so we are able to tweak the models before generation. We now have a single script that can calculate: Ground State Energy, Spin-Spin Correlation, Charge Correlation, Double Occupancy, Spin-Spin Structure Factor, Charge Structure Factor, and all of their averages over four phase twists.
* ED Oracle Verification: It was more difficult than expected to search research papers for a basic Kagome model with the structure parameters and matching outputs that I could test our oracle against. I eventually found edge cases, such as open periodicity where U = 0 (no Coulomb interaction), and those tests yielded correct results. While I consider this to hopefully be enough for verification, we can do more checks; our mentor provided us a research paper to parse through that could be helpful.
* UCLA ID: Throughout the past few weeks, we have been coordinating with the management department to get ID cards for the university so that we could get access to the engineering lab buildings and computer clusters. However, we were informed just this week that we are not eligible for the UCLA IDs despite the long process. 
* DeltaAI: We are able to get GPU access through NSF Access and DeltaAI. I have an account for NCSA and DeltaAI but have been unable to verify if I can use their GPU clusters.
* Deep Learning Research: We decided to focus on Neural Networks last week with PyTorch, but before committing, we began looking for other Neural Networks. Our mentor suggested looking at research papers to see if their pre-trained models might be available. These research was promising but we found few models we could repurpose. I was able to encounter a GitHub-like repository of pre-trained AI models on a website called huggingface.co. It seems credible, at least for the neural networks that we were looking for. I found a repository of neural networks for the Hubbard model, which should be useful, once we can verify if it is viable.
## Results
* TeNPy Generation: We have confirmed that our TeNpy generator will produce all values expected.
* ED Oracle Verification: We have now verified* our Oracle is accurate, at least in terms of ground state energies. 
* ACCESS/DeltaAI onboarding: We have access to GPU compute, which will be useful for our Neural Network stage.
* Campus Access Ineligibility: We cannot access our mentor's lab nor the computer clusters on UCLA campus due to not meeting ID requirements (mainly minimum requirement of three months on-campus access and independent contractor access level)
## Notes
* TABC produces a difficulty of a 4x multiplier to time complexity to the generation. All model generation will take four times as long due to the quantum property calculations being performed four times for every model (for averaging).
* Need to prioritize reading the mentor's recommended paper before next meeting.
* CRA: Attended the CRA meeting for the milestone progresses: should I begin prepping for the final presentation?


