
# Commands
**(Temporary measure)** In order to use the `nxml` command in your command line interface, you first need to create an alias by :
```bash
alias nxml = "python3 path/to/nxml_api/repo/nxml_api/src/nxml_api/nxml.py"
```
To get help from the command-line, simply call `nxml` to see the complete list of commands,
then `--help` combined with any of those can give you more information.

## Global options

* `--help (-h)` : Display help information.
* `--version (-V)`: Display this application version.

## Workspace : 
In this section we will detail the workspace related commands.

### workspace 
This command will help you load or create a machine learning workspace with the desired cloud provider.
```bash
nxml workspace --create --provider azure --config path/to/config/file.json
```
or to load an exisiting workspace
```bash
nxml workspace --load --provider azure --config path/to/config/file.json
```
### Options : 
* `--provider (-p)` : Cloud provider  [required]
* `--config (-cf)` : Path to the workspace configuration file  [required]
* `--create`/`--load` : Create a new workspace or load an existing one
 
### Example of a config file :
**(To be added)**

### workspace-show
This command will show information about the requested workspace
```bash
nxml workspace-show --name my_workspace
```

### Options :
* `--name (-n)`: Workspace name

### workspace-list 
This command will list the loaded workspaces 
```bash
nxml workspace-list
```

## Datasets : 
In this section, we will detail the dataset related commands

### dataset-attach 
This command will let you attach a dataset to the working environment
```bash
nxml dataset-attach --config path/to/dataset/config.json
```

### Options :
* `--config (-cf)` : path to the dataset configuration file.

### Example of a dataset configuration file :
**(To be added)**

### dataset-show
This command will show information about the requested dataset
```bash
nxml dataset-show --name my_dataset
```

### Options :
* `--name (-n)`: Dataset name

### dataset-list 
This command will list the loaded datasets 
```bash
nxml dataset-list
```

## Compute Environment :
Before running an experiment we need to set up the workspace with a compute environment/cluster.

### compute-env
Create a compute environment from a configuration file :
```bash
nxml compute-env --config path/to/compute_env/config.json
```

### Options :
* `--config (-cf)` : path to the compute environment configuration file.

### Example of a compute environment configuration file :
**(To be added)**

### compute-env-show
This command will show information about the requested compute environment
```bash
nxml compute-env-show --name my_compute_env
```

### Options :
* `--name (-n)`: Compute environment name

### compute-env-list 
This command will list the set compute environments 
```bash
nxml compute-env-list
```
