> remove layers of complexity.

![](./doc/intro.svg)

## Usage

```
$ cd myapp 
$ wget "https://raw.githubusercontent.com/coderofsalvation/podi/master/podi"
$ chmod 755 podi
$ ./podi recipe app/container     # a template container recipe
$ ./podi recipe start/envfile     # cli-cmd to set remote env-vars
```

> PROFIT! now init your (ssh)server to enable a heroku-ish workflow:

![](./doc/workflow.jpg)

## Features

* fully hackable PaaS & Gitops-designer (embedded in your repo)
* per-branch and per-sshuser deployments 
* hookable (`on build callmyfunction arg1`)
* app templates
* autosuspending app templates
* podi weighs 5k, just needs ssh+git installed
* works on raspberry pi zero but also on kubernetes

## Create recipes

![](./doc/extend.svg)

## Install

```bash
$ wget "https://raw.githubusercontent.com/coderofsalvation/podi/master/podi"
$ chmod 755 podi
$ ./podi
usage: 
    init git@server:/dir/to/deploy [branch] [port] [name]   initializes a deployment 
    recipe <name_or_url>                                    installs a recipe from podi repo or url
```

## Docs

* [adding your own recipes](doc/recipes.md)
