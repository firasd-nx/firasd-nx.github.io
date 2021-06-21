---
title: "Commands"
draft: false
type: docs
layout: single

menu:
  docs:
    weight: 30
---


# Commands
(Temporary measure) In order to use the `nxml` command in your command line interface, you first need to create an alias by :
```bash
alias nxml = "python3 path-to-nxml_api-repo/nxml_api/src/nxml_api/nxml.py"
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
nxml workspace --create --provider "azure" --config "path/to/config/file"
```
or to load an exisiting workspace
```bash
nxml workspace --load --provider "azure" --config "path/to/config/file"
```
### Options : 
 `-p`, `--provider` : Cloud provider  [required]
 `-cf`, `--config` : Path to the workspace configuration file  [required]
 `--create`/`--load` : Create a new workspace or load an existing one
 
