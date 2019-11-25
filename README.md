# Irset-Transcriptomics-Test

##Objectives


The EURION GitHub repository aims to centralize bioinformatics resources used by the EURION cluster’s members to analyze omics data. In order to improve reusability of analysis pipelines and accessibility to the tools and data, each member will be allowed to create new repositories following these guidelines.


##Repositories structure
###Repository Name
Each new repository must use the following nomenclature: 

           {Institut_name}-{Technology}-{Sub-technology} 
           	i.e.: Irset-Transcriptomics-SingleCell
 
###Repository Structure
To improve usability, please use the following structure: 
 
           {Institut_name}-{Technology}-{Sub-technology}
                       | - Docs
                       | 	|- doc.txt
                       | - Data
                       | 	|- Inputs 
                       | 	|     | - Input01_run.XYZ
                       | 	|- Outputs
                       | 	|     | - Output01_run.XYZ 
                       | - Scripts
                       | 	|- ScriptXXX_run.XY
                       | 	|- DOCKERFILE
                       | - README
                       
           
•	Docs is a directory containing all documentation needed to use the pipeline.
•	Data is a directory containing both input and output test data, allowing users to easily test the pipeline. Since repositories should not contain heavy files, please provide a text file with a link to the data if its size is bigger than 50 MB.
•	Scripts is a directory where all pipeline analysis scripts are stored. This folder can be divided into sub-folders to structure each analysis steps or tools.
•	README. A README is a text file that introduces and explains the project. It contains information that is commonly required to understand what the project is about and how to run scripts. Please make sure to include the exact version of each tool you use, and the source if possible.
For more information about how to write a README please see https://www.makeareadme.com/ or https://gist.github.com/PurpleBooth/109311bb0361f32d87a2 
 
Using all these elements, users must be able to easily launch the pipeline on the input test data. The results of the pipeline must be the provided output test data.

##Reproducible analysis
One of the main objectives of this GitHub repository is to allow the reproducibility of the analyzes, especially if you use specific software. For this, two tools are recommended: Docker or Conda. 

###Docker
Docker is an open-source engine that automates the deployment of applications into containers. The main goal is to help users create and share complex work environments with other users. The environment creator must provide a “Dockerfile” (containing all installation instructions) and all the required files. Then, any user will be able to re-create the exact same environment, and thus run any tools required by a pipeline. All containers are isolated from each other, avoiding any conflicts between tools, and work on any OS (Mac, Linux or Windows >7 64 bits).
Docker is especially powerful for molecular biologists, due to the sheer complexity of work environments (high number of tools, complex installations…)
