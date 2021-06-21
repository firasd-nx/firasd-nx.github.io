
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

## Experiment :
Now we can run the ML experience in our workspace, on the set compute environment using the loaded dataset.

### train
```bash
nxml train --script path/to/training/script.py --config path/to/experiment/config.json
```
### Options :
* `--script (-s)` : path to the training script
* `--config (-cf)` : path to the experiment configuration file

### Example of an experiment configuration file :
**(To be added)**

### exp-list 
This command will list created experiments
```bash
nxml exp-list
```

## Model :
This section details the commands dealing with the trained model from the experiment.

### model-register 
This command will help you register a trained model to your workspace.
```bash
nxml model-register --model my_model --path path/to/register/model
```
### Options :
* `--model (-m)` : model name
* `--path (-p)` : path to register the model in 

### model-download
This command will help you download a trained model to your local machine.
```bash
nxml model-download --model my_model --path path/to/download/directory
```
### Options :
* `--model (-m)` : model name
* `--path (-p)` : path to the download directory

## Prediction :

### predict 
Use a trained model to predict on a new dataset and output the predictions
```bash
nxml predict --model my_model --data my_data --output path/to/output/predictions
```

### Options :
* `--model (-m)` : trained model name
* `--data (-d)` : path to the data to be predicted on
* `--output (-o)` : Output prediction file

## Deployment :
**(Still Under Construction)**

