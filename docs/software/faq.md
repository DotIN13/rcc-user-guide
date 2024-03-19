# Software FAQ

### What software does RCC offer on its compute systems? 

Software available within RCC is constantly evolving. We regularly install new software, and new versions of existing software. Information about available software and how to use specific software packages can be found in the [Software](../software/index.md) section of the User Guide.

To view the current list of installed software on RCC clusters, run the following command: 

```
module avail
```

To view the list of available versions for a specific software, run the following command: 

``` 
module avail <software>
```
### How do I get help with RCC software? 
Documentation for many programs can be viewed with the following command.

``` 
man <command>
```

Many programs also provide documentation through command-line options such as `--help` or `-h`. For example,


```
module load gcc
``` 

```
gcc --help
```

RCC also maintains supplementary documentation for software specific to our systems. Consult the [Software](../software/index.md) page for more information.

### Why is my favorite command not available? 

Most likely it is because you have not loaded the appropriate software module. Most software packages are only available after first loading the appropriate software module. See [Software](../software/index.md) for more information on how to access pre-installed software on RCC systems.

### Why do I get an error that says a module cannot be loaded due to a conflict? 

Occasionally, modules are incompatible with each other and cannot be loaded simultaneously. The module command typically gives you hints about which previously loaded module conflicts with the one you are trying to load. If you see such an error, try unloading a module with this command:

```
module unload <module-name>
```

### How do I request installation of a new or updated software package? 

Please [contact our Help Desk](https://rcc.uchicago.edu/support-and-services/consulting-and-technical-support) with the details of your software request, including the following informaiton: 

### Why can’t I run Gaussian?
Creators of Gaussian have historically had a strict usage policy, so we have limited its availability on RCC systems. If you need to use Gaussian for your research, please [fill out this from](https://rcc.uchicago.edu/accounts-allocations/general-user-account-request) and for the `Principal Investigator account name (probably pi-CNetID):` type in `gaussian`. Our team will process you request in a few hours. 

## Why can't I run COMSOL?
Creators of Gaussian have historically had a strict usage policy, so we have limited its availability on RCC systems. If you need to use COMSOL for your research, please [fill out this from](https://rcc.uchicago.edu/accounts-allocations/general-user-account-request) and for the `Principal Investigator account name (probably pi-CNetID):` type in `comsol`. Our team will process you request in a few hours. 