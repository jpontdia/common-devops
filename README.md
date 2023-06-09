# mulesoft-pipeline
The Pipeline Repository is a centralized hub that provides reusable workflows and actions for building and deploying software services within our organization

## Table of contents
1. [Description](#description)
1. [Workflows](#workflows) 
1. [Actions](#actions) 

## Description
The Pipeline Repository is a centralized hub for building and deploying software services in our organization. It offers reusable workflows and actions that streamline development processes and adhere to best practices. The repository aims to enhance efficiency, reliability, and collaboration throughout the software development lifecycle.

Teams can access meticulously crafted workflows and actions covering various aspects of software delivery. These automate tasks such as building, testing, and deploying services, saving time and ensuring reproducibility. The workflows are customizable to fit specific requirements, allowing teams to integrate preferred tools, testing frameworks, and coding standards.

Collaboration is encouraged, with teams contributing insights and improvements to foster innovation. The repository empowers developers to make choices that best suit their services while maintaining overall coherence in software delivery. With the Pipeline Repository, we can revolutionize our development cycles and deliver exceptional software experiences.

## Workflows

Github reusable workflows in directory: .github/workflow

| Workflow    | Description |
| ----------- | ----------- |
| mulesoft.yml | Build and deploy Mulesoft services to cloud (Cloudhub/GovCloud). The same workflow helps to deploy other kind of assets to Anypoint Exchange like parent poms, library projects, custom connectors, etc. |

## Actions

Github composite actions in directory: packages

| Action               | Description |
| -------------------- | ----------- |
| cloudhub-anypoint-cli | Anypoint CLI to deploy a service to CloudHub/GovCloud.|
| cloudhub-deployment | Deploys a service to CloudHub/GovCloud.|
| code-coverage | Prints a job summary with the code coverage report.|
| configuration-file | Get the configuration data for a mulesoft asset.|
| secrets | Get the default secrets for the pipeline and the service to build.|
| install-anypoint-cli | Install Mulesoft anypoint-cli. The Anypoint CLI (Command Line Interface) is a tool provided by MuleSoft that allows you to interact with the Anypoint Platform from the command line, and enables you to manage and deploy applications, APIs, and other integration assets using scripts or automated workflows.|
| install-mulesoft-java | Install and configurtes Java JDK for Mulesoft applications.|
| service-info | Get the basic information for the service like the name from the pom.xml file |
| settings-maven | Get the settings.xml file required for Maven to compile and package the Mulesoft/Java service or asset. |

# Mulesoft Github CICD Pipeline

## Table of contents
1. [Pipeline resource](#pipeline-resource)
1. [Azure KeyVault](#workflows) 
1. [Repository: mulesoft-configurations](#repository-mulesoft-configurations) 

## Pipeline resources

Next is the list with the resources required by the pipeline:

- Azure Keyvault: A KeyVualt to store all secrets required by services and pipeline
- Github respository: mulesoft-configurations
- Github respository: mulesoft-pipeline
- Github Gist: A Gist to store to code badges: code coverage, test unit, etc.
- Github repository secrets: Tokens to access configuration resources like Azure Keyvault

## Azure KeyVault

Mandatory secrets
| Secret               | Description |
| -------------------- | ----------- |
| github-configurations-accesstoken | Personal access token for repository: mulesoft-configurations.|
| github-gist-accesstoken | Personal access token for gist access.|

## Repository mulesoft-configurations

Repository with the configuration for the pipeline and services. The mandatory files are:

| File                 | Description |
| -------------------- | ----------- |
| secrets-map.txt | Personal access token for repository: mulesoft-configurations.|
| settings.xml | Personal access token for gist access.|

## Github repository secrets

Github repository secrets to connect the system resources:

| Secret                 | Value |
| -------------------- | ----------- |
| AZURE_CREDENTIALS | Configuration token to access Azure Keyvault.|
| GIST_ACCESSTOKEN | Personal access token with write gist access.|

