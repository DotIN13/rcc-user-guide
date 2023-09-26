# Software packages and compilers 

The best way to view the latest software packages offered on RCC clusters is to check the list of available software modules with the `module avail` command.

All users can install software packages privately in their home and project directories. It is recommended to use **compute nodes** rather than login nodes when compilation and installation processes are time-consuming and require significant resources. Please check our documentation on how to start and use a `sinteractive` session [here](../slurm-sinteractive.md). 

## Using software modules

RCC uses [Environment Modules](http://modules.sourceforge.net) for managing software. The modules system permits us to set up the shell environment to make running and compiling software easier. It also allows us to make available many software packages and libraries that would otherwise conflict with one another.

When you first log into RCC clusters, you will be entered into a basic user environment with minimal software available.  The `module` system is a script-based system used to manage the user environment and to `activate` software packages.  You must first load the corresponding software module to access software packages installed on RCC clusters. 

Basic `module` commands:

| Command  | Description | 
| --------- | --------- | 
| `module avail`          |   lists all available software modules            |    
| `module avail [name]`   |   lists modules matching [name]                   |
| `module load [name]`    |   loads the named module                          |
| `module unload [name]`  |   unloads the named module                        |
| `module list`           |   lists the modules currently loaded for the user |

!!! note "Module dependencies"
    Note that some modules require other specific modules, i.e., dependencies, to be loaded (or unloaded). If there is a conflict, you must explicitly unload the conflicting module (`module unload ...`), then load the desired module again. In certain cases, usually with loading an out-of-date module, you may get an error such as `Error: Requirement...` if a dependency is absent. In those situations, you can try `module load -f <module>` to force the module to load.

!!! note
    If you need software not currently available in the module system and believe that multiple research groups can benefit from installing this software, send a detailed request to our [delpdesk](https://rcc.uchicago.edu/support-and-services/consulting-and-technical-support) providing:
    1. Complete the name of the software package 
    2. Exact version number 
    3. Link to the package website 
    4. Explain in a paragraph how this software is crucial for your research and having it on RCC clusters. 

## Commonly used software packages

This guide contains instructions for some commonly used applications and environments, including:

* [Alphafold](../software/apps_and_envs/alphafold.md)
* [CryoSPARC](../software/apps_and_envs/cryosparc.md)
* [GROMACS](../software/apps_and_envs/gromacs.md)  
* [LAMMPS](../software/apps_and_envs/lammps.md)
* [MATLAB](../software/apps_and_envs/matlab.md)    
* [Mathematica](../software/apps_and_envs/mathematica.md)
* [NAMD](../software/apps_and_envs/namd.md)
* [Perl](../software/apps_and_envs/perl.md)  
* [Python and Jupyter Notebook](../software/apps_and_envs/python.md)
* [R](../software/apps_and_envs/r.md)
* [Singularity](../software/apps_and_envs/singularity.md)
* [Spark](../software/apps_and_envs/spark.md)
* [Stata](../software/apps_and_envs/stata.md)    
* [Tensorflow and PyTorch](../software/apps_and_envs/tf_and_torch.md)  
  

!!! note "Note on software for AMD CPUs" 
    For the `amd` [partitions](../partitions.md) on Midway3, you need the software modules built specifically for AMD CPUs.
```
module use /software/modulefiles-amd
module list
```

