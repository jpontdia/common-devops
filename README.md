# devops-pipelines
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
| configuration-file | Get the configuration data for a mulesoft asset.|
| get-secrets | Get the default secrets for the pipeline and the service to build.|
| install-anypoint-cli | Install Mulesoft anypoint-cli. The Anypoint CLI (Command Line Interface) is a tool provided by MuleSoft that allows you to interact with the Anypoint Platform from the command line, and enables you to manage and deploy applications, APIs, and other integration assets using scripts or automated workflows.|
| install-mulesoft-java | Install and configurtes Java JDK for Mulesoft applications.|
| service-info | Get the basic information for the service like the name from the pom.xml file |
| settings-maven | Get the settings.xml file required for Maven to compile and package the Mulesoft/Java service or asset. |
