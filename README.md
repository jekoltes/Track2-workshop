# Track2-workshop- Advanced Functional Genomic applications of livestock regulatory elements
# General Information
All materials (except software) for the Track 2 Advanced Functional Genomics session in the Genomics for Animal Sciences – Summer Workshop host by NRSP8 and the USDA-NIFA Animal Genomics Collective RCN in Madison, WI in July 2026.
https://www.asas.org/meetings/annual-2026/draft-schedule-of-events-and-scientific-program 

Please note, this is not a formal GitHub repository that you would download, but itstead is serving as a place to organize and share information in a simple way.  If you are participating in the tutorial, there are 2 files on this page that you should download: PPTX slides and data/ scripts.  A course agenda is provided as a 3rd file to download if you have not received it previously.  The steps below are how to get started in preparing for this workshop following the instructions also sent to participants via email.



# Items to do before the class day to prepare for the workshop
# Step 1: Setting up your HPC account
If you are using NSF ACCESS computing for tutorials, please sign up for an account here: https://operations.access-ci.org/identity/new-user   After you receive an account, send it to the course coordinator and after your account is active (you will receive an email to create a password), make sure you are able to login on the HPC resource (see the course reference PPTX slides above).

# Step 2: Finding the data and code
Download Data and Code used in Workshop: https://iastate.box.com/s/1jcek1gwvcrrxwmdxacodlo5w92dkcvm 
Please note: you should not have to place these data on the HPC.  Once you are logged into the HPC account on Bridges2, the data is located in storage on the Ocean server here: /ocean/projects/bio260049p/shared
More information on the file contents and how to navigate these folders is provided below.

# Step 3: Download the class slides to brush up before the class day
Download reference slides to follow the tutorial here: https://github.com/jekoltes/Track2-workshop/commit/90661248ecae7cd631de3f9f35f37282695d30ad 

# Step 4: Ensure you have installed all required software on the laptop you will bring to class
Make sure you have installed the required software onto your laptop based on the guidance provided: https://github.com/jekoltes/Track2-workshop/commit/85bd5feaea27a9ec95caeac56a86634d7c8460e7 
Additional sofware used in the HPC section of the course are also listed in this document if you do not have access to HPC resources.



# Background information on the new Ensembl-beta web browswer (replacing the current browser in August 2026)
Website: https://beta.ensembl.org/

Tutorial Video: https://www.youtube.com/watch?v=K7cmwK1ODnc 

Tutorial Slides:https://drive.google.com/file/d/1j1_sbkULCDnlpaeW6jhaDFpdcdt59jHd/view

Note, additional information is provided in the course PPTX presentation file.




# Agenda for the in-person Workshop Day: 
Please find a Word document with the general agenda of topics covered in the workshop here: https://github.com/jekoltes/Track2-workshop/commit/f35f5f10328610907ee8091dc1cd906015e30d10.



# Help during the in-person class:  Navigating to find data and scripts on Bridges2 for the tutorials
Once logged into Bridges2, follow the commands in steps 1 and 2 below to find the data folders.  Below these commands are a description of the files within each folder as well as paths you can copy and paste on class day to help you more quickly navigate to the data during the in-class tutorials.

# Step 1: move to the data and code folder
> cd /ocean/projects/bio260049p/shared

Note: If the data folder is still as a .tar.gz, you will need to uncompress it like this:
> tar -xzvf workshop.tar.gz

# Step 2: move to the data folder
> cd ASAS_workshop/data/workshop

At this step, you should now see the following when you use the ls command:
[userName@bridges2-login012 workshop]$ ls
01_ftp  02_biomaRt  03_api  04_integration  05_atac

The numbers above correspond to the session order in the class.  We will start with 1 and move our way to folder 5 through the day.  Here is some helpful information about these folders.

# 01_ftp (empty)  
/ocean/projects/bio260049p/shared/ASAS_workshop/data/workshop/01_ftp

# 02_biomaRt 
    /ocean/projects/bio260049p/shared/ASAS_workshop/data/workshop/02_biomaRt
    Contains 2 files: biomaRt_script.R  example_result.tsv
    
# 03_api
    /ocean/projects/bio260049p/shared/ASAS_workshop/data/workshop/03_api
    
    Contains 3 files: api_script.R  example_result.tsv  sus_scrofa_regulatory_features_rest_api.tsv
    
# 04_integration
    /ocean/projects/bio260049p/shared/ASAS_workshop/data/workshop/04_integration
   
    Contains 2 folders: 01_vep  02_integ_example

   /ocean/projects/bio260049p/shared/ASAS_workshop/data/workshop/04_integration/01_vep 
    1- contains 7 files: 
      sus_scrofa_1000_2.vep
      sus_scrofa_1000.vcf
      sus_scrofa_1000.vep.vcf_summary.html
      vep_workshop.sh
      sus_scrofa_1000_2.vep_summary.html
      sus_scrofa_1000.vep.vcf
      sus_scrofa.vcf

    #   /ocean/projects/bio260049p/shared/ASAS_workshop/data/workshop/04_integration/02_integ_example
    2- contains 4 files: 
      Animal_QTLdb_release59_pigSS11.bed
      chr15_longissimus_depth_QTL_cCRE_summary.tsv
      Animal_QTLdb_release59_pigSS11.gff
      chr7_longissimus_depth_QTL_cCRE_summary.tsv
                         
# 05_atac
    /ocean/projects/bio260049p/shared/ASAS_workshop/data/workshop/05_atac/
    
    Contains 16 items: 8 files + 8 folders
    
    Files = shell scripts: 
    xx-02-JOB-trim.sh  
    xx-05-JOB-rem.sh   
    xx-08-JOB-filt.sh   
    xx-10-JOB-peak.sh 
    xx-01-JOB-qc.sh    
    xx-04-JOB-sort.sh
    xx-07-JOB-dedup.sh  
    xx-10-JOB-peak-fulldata.sh
    
    Folders within 05_atac/:
    /ocean/projects/bio260049p/shared/ASAS_workshop/data/workshop/05_atac/00_ref
    /ocean/projects/bio260049p/shared/ASAS_workshop/data/workshop/05_atac/01_raw_data
    /ocean/projects/bio260049p/shared/ASAS_workshop/data/workshop/05_atac/03_trimmed
    /ocean/projects/bio260049p/shared/ASAS_workshop/data/workshop/05_atac/04_mapping
    /ocean/projects/bio260049p/shared/ASAS_workshop/data/workshop/05_atac/06_no_mt
    /ocean/projects/bio260049p/shared/ASAS_workshop/data/workshop/05_atac/07_readgroup
    /ocean/projects/bio260049p/shared/ASAS_workshop/data/workshop/05_atac/09_filtered
    /ocean/projects/bio260049p/shared/ASAS_workshop/data/workshop/05_atac/10_shifted            




# Tip for running Job scripts on the SLURM scheduler within the HPC environment
There are several different text editors that can be used to alter files.  Here I will describe how to update a file using nano.

Job scripts: .sh files    (please note, these are sometimes named .job if you prefer for organizational purposes)

To modify a file, for example xx-01-JOB-qc.sh 
> nano xx-01-JOB-qc.sh

#Here is what the file should look like

#!/bin/bash
#SBATCH --job-name=workshop_JOB      # change the name as you prefer
#SBATCH --partition=RM-shared        # do not change - queue used  
#SBATCH --account=bio260049p         # do not change - account
#SBATCH --time=00:10:00              # do not change - run time
#SBATCH --ntasks=1                   # do not change 
#SBATCH --cpus-per-task=1            # do not change - CPU number used
#SBATCH --output=02_qc/JOB_workshop_%j.out    #output file name, automatically configured.  Note, here j should be your job-name
#SBATCH --error=02_qc/JOB_workshop_%j.err     #error file name, automatically configured (as described above)

set -euo pipefail

cd /jet/home/limb/workshop/05_atac                   #CHANGE- use your username here where "limb" is listed

module load FastQC

fastqc \
    01_raw_data/workshop_R1.fastq.gz \
    01_raw_data/workshop_R2.fastq.gz \
    -o 02_qc

To save the chages, type: control+x (command to start the proceedure to close the file), 
                          control+y (saves file name)
                          type: y
                          At this point, you may change the file name, or hit enter to close and save the file as is without a name change.




# How to submit a job file
Note: you need to be in the folder where the job script (.sh in this tutorial) is located
Type
> sbatch  xx-01-JOB-qc.sh

To ensure the file is running, use this command:
> squeue

Better yet, jump to only your job:
> squeue -u userName

If you want to actively monitor a short job, you can use this command (note to leave this command, you must type: Ctrl+C)
> watch squeue -u userName





