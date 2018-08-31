# SDLC Deployment Phase for Front-End Code

## Overview

The deployment phase is the final phase of the software development life cycle (SDLC) and puts the product into production. After the project team tests the product and the product passes each testing phase, the product is ready to go live. This means that the product is ready to be used in a real environment by all end users of the product.

There are various phases of the deployment process the project team must follow to ensure the code and technology deploy appropriately. The phases include deployment preparation and procedures, product deployment, transferring ownership of the product, and closing the deployment phase.

## Preparation and Procedures

### Testing

Before the deployment process can be inititated There are a list of testing prerequisites that need to be complated first.

- [X] First, QA needs to sign off on all critical tickets(p1 - p3) and showstoppers in a QA or UAT Environment.
- [X] Next, The Accessibility team needs to sign off on all Accessibility checks and defect fixes in a QA or UAT Environment
- [X] Next, The package release candidate should be deployed on a PT (Performance Testing) environment for testing by the PT Team

### Code Freeze

After testing is complete, a code freeze should happen a week (Five working days) before a production realease. Only critical code fixes should be entered during this time. 

### IQOQ (Input Queue Output Queue)

The IQOQ is an excel document that mentions what changes will be deployed to the production servers. For all angular changes you will need a webcontent build and for Backend(JAVA/ATG) changes you will need a commmerce build. All changes and procedures that are changing in the release cadidate will have to be outined in this document as well as protocols for rollback if necessary. 

An example of the IQOQ Document can be found here [IQOQ Doc](http://sharepoint)


A tag will be created for production after UAT1 as signed off for QA.

Then the tagged branch will go to the enviromnent team so that it can be merged in as part of the release branch. 

There two ways to get the angular tiles in to the release branch
1. the minified files can be commited to svn 
2. a copy of the jenkins pipeline should be created on the production jenkins server so that it can be incorporated in the build.


### Production Nexus and NPM Packages
Packages need to be uploaded to the production nexus npm repository so that they can be integrated with the build. All packages should be loaded to 
