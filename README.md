# SDLC-Deployment-Phase

## Code Freeze
A code freeze should happen a week (Five working days) before a production realease. Only critical code fixes should be entered during this time. 

## Preparation and Procedures
1. QA sign off
2. Accessibility sign off
3. Performance Testing sign off

All Defects from showstopper to P3 should be resolved for sign off. 
Code should be deployed on a PT (Performance Testing) envoriment 
Release manamgement team conference one week before production

### IQOQ (Input Queue Output Queue)
The IQOQ is an excel sheet that mentions what changes will be deployed to the production servers. For all angular changes you will need a webcontent build and for ATG changes you will need a commmerce build. each POD will have to mention every file that has been changed.

An example of the IQOQ Document can be found here [IQOQ Doc](http://sharepoint)

A tag will be created for production after UAT1 as signed off for QA.

Then the tagged branch will go to the enviromnent team so that it can be merged in as part of the release branch. 

There two ways to get the angular tiles in to the release branch
1. the minified files can be commited to svn 
2. a copy of the jenkins pipeline should be created on the production jenkins server so that it can be incorporated in the build.

### Production Jenkins 

### Production Nexus
Packages need to be uploaded to the production nexus npm repository so that they can be integrated with the build. All packages should be loaded to 
