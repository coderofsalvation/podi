> remove layers of complexity.

![](./doc/intro.svg)

## Usage

```
$ cd myapp 
$ wget "https://raw.githubusercontent.com/coderofsalvation/podi/master/podi"
$ chmod 755 podi
```

> PROFIT! now init your (ssh)server to enable a heroku-ish workflow:

![](./doc/workflow.jpg)

## Features

* fully hackable PaaS & Gitops-designer (embedded in your repo)
* multitenant: multi-branch and multi-sshuser deployments 
* `podi ls`: gitops templates for containerizing, autosuspending services on baremetal etc
* hookable (`on build callmyfunction arg1`)
* podi weighs ~7k, just needs ssh+git installed
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
