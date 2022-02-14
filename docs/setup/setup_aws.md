# Getting started - AWS

## First steps

The following sections describe the **setup** process for the [AWS IoT Framework](https://github.com/ECE-IoT/aws-iot-framework) repository. For more information head over to:

* [AWS](https://ece-iot.github.io/aws-iot-framework/aws/cli/configuration-basics/)
* [Alexa](https://ece-iot.github.io/aws-iot-framework/alexa/)

### Introduction 

The setup for the [AWS IoT Framework](https://github.com/ECE-IoT/aws-iot-framework/tree/master) is based around a [Docker](https://www.docker.com/products/docker-desktop) image which builds a capable development environment. In addition this **Docker** image can directly be hooked to a **VS Code** project, which enables an automatic work-space creation. This functionality is made possible through the [Devcontainer](https://code.visualstudio.com/docs/remote/create-dev-container) capabilities of **VS Code**. 

### Setup process 

* Make sure that [Docker Desktop](https://www.docker.com/products/docker-desktop) is installed on your system 
* This repository is built around [VS Code](https://code.visualstudio.com/Download) therefore make sure that it's installed on your system.
* Clone this repository and open it with **VS Code**
    * Make sure that **Docker Desktop** is running 
    * **VS Code** should automatically detect that this repository contains a **Dockerfile** and launches the **Docker container** via the running **Docker Desktop** instance.

### What's inside the container?

The image contains a fully capable [Linux Debian](https://hub.docker.com/_/debian/) distribution which has all the essential build tools for `C++` and `Python 3.9` pre-installed. In addition the stock [BASH](https://www.gnu.org/software/bash/) is replaced by a [ZSH](https://www.zsh.org). The **ZSH** is then configured with the [Oh My Zsh](https://ohmyz.sh) framework which enables a highly customizable shell environment. 

Next the **Dockerfile** installs all necessary requirements for the development of [AWS Lambdas](https://aws.amazon.com/de/lambda/) and other `Python` projects. The following modules are going to be installed: 

* [boto3](https://pypi.org/project/boto3/)
* [awscli](https://pypi.org/project/awscli/)
* [aws-sam-cli](https://pypi.org/project/aws-sam-cli/)
* [cfn-lint](https://pypi.org/project/cfn-lint/)
* [pandas](https://pypi.org/project/pandas/)
* [matplotlib](https://pypi.org/project/matplotlib/)
* [mkdocs-material](https://pypi.org/project/mkdocs-material/)
* [mkdocs-plugin-mermaid](https://pypi.org/project/mkdocs-mermaid-plugin/)
* [mkdocs_pymdownx_material_extras](https://pypi.org/project/mkdocs-pymdownx-material-extras/)
* [mkdocs-git-revision-date-plugin](https://pypi.org/project/mkdocs-git-revision-date-plugin/)
* [mkdocstrings](https://pypi.org/project/mkdocstrings/)

Last but not least the `devconatainer.json` settings and extensions are executed in order to install all necessary **VS Code extensions** within the **Devcontainer**. 