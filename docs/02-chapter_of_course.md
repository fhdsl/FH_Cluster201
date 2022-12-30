
# Computing Modes
There are many ways to leverage a local cluster and cloud resources for computing.  


## Interactive Modes

### Rhino (Login Nodes)


- see what software you can use that's already installed
- do small, interactive jobs using software not installed on your local computer
- test small jobs prior to scaling up
- can run cronjobs from here to schedule things to happen regularly


### `Grabnode`

- runs one big job with limited configuration options

## Non-Interactive Modes

### SLURM (S-commands)

SLURM job submission to gizmo:

- making jobs resilient to connectivity issues (grabnode sessions end your job if you lose connectivity)
- no need to babysit the job this way
- generates job logs for troubleshooting
- uses the SLURM scheduler and better lab job allocation (helps you get resources sooner and in coordination with the rest of your lab and the Hutch users more broadly)
- srun, sbatch, etc. gives you more control and options for configuration that let your jobs run better in many ways

- SLURM array jobs


### Workflow managers

- good when you have multi-step processes that need to occur together
- when your multi-step processes have dependencies that conflict: allows task isolation and management 
- good when you're working on multiple different workflows at the same time
- want to leverage the cluster allocation very efficiently by breaking jobs up
- want to prepare a workflow for better reproducibility, sharing, and expanding to the cloud

#### Cromwell

#### Nextflow

### Cloud computing

- once a workflow has been optimized (likely using a workflow manager above), leveraging the cloud for large, production workflows can help your lab's usage of the cluster while also encouraging reproducibility
- Workflows can ideally be run by others, not just those with access to the Hutch resources

- great when you do not have access to a local cluster or when you want to use a commercial platform for running computational work. 


## Sharing and Collaboration

Issues like sharable code, sharable software environments and compute resource optimization become more important when you want to share and collaborate. 


- GitHub
- Dockerhub/Quay.io 
- Dockstore 

- Terra
- DNA Nexus
- other people's resources (like their non-SLURM cluster or maybe they use Azure or Google or AWS primarily?)
