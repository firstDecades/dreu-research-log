# Week 3

**Dates:** 07-06 to 07-10

## Goals
* Create Database: Run the script to create Kagome models
* Optimized Data Storage: Update the second script to store the computed quantum properties in the .h5 data
* Deep Learning Research: Look into PyTorch and other possible frameworks
## Approach and Implementation
* Database Scaling: The first attempt at creating the database had us creating 100 random Kagome models of varying site numbers. I noticed that three-site Kagome models generated faster than six-site models, six-site models faster than nine-site models, and nine-site models faster than twelve-site. As such, I separated the generation of the Kagome models by site, producing one hundred each of three-site, six-site, and nine-site Kagome models. Additionally, after a discussion, we plan on changing the generation to be 300 of three-site Kagome models, 200 of six-site Kagome models, 100 of nine-site Kagome models, and 50 each of twelve-site and fifteen-site Kagome models. 
* Database Modifications: We noticed that the computed quantum properties were not stored anywhere. As such, I modified the second script to append the properties to the individuals .h5 files of the Kagome models. Additionally, I noticed that we are not storing the ground state energy in the .h5 files, one of the properties that will be computed by the Agent. As such, we need to modify either the second script or re-run the first script with the addition of the energy in the .h5 file. Since we will be re-running the first script to generate the additional Kagome models, we can edit the first script more easily. Computing the energy would require a lot of additions to the second script.
* Framework: We have selected PyTorch as the framework. We generated the Kagome models through TeNPy and the information is stored in the TeNPy format. However, it will likely not be a problem as we should be able to extract only the model parameters from .h5 format and feed those in as inputs to the deep learning network. Everything being consolidated in the .h5 format will make data transfer and access easier, hopefully. We have not yet implemented a PyTorch Framework. Some research into PyTorch indicates that access to a capable GPU will make the framework more effective, and as such we should wait to get access to the DeltaAI mentioned by the mentor (need BruinCard access, I believe).
## Results
* Database: We now have a standardized database separated by number of sites. It will likely be tweaked and re-created next week.
* Framework: We have selected PyTorch and are currently in the research stage to make sure it will do the job and verify if we have enough resources (database quantity, GPU capabilities)
* University Access: We are still in the process of getting University Access with the ID Cards.
## Notes
* We still need to verify the ED Oracle and if TABC is viable. Since we are likely tweaking the generation again, we can check TABC again.


