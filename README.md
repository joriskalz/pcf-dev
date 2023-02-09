# PCF Controls Development Environment Template
This repository is a template for developing Power Apps Component Framework (PCF) controls for use in Power Apps and Dynamics 365. It includes a Dockerfile and a devcontainer.json file to set up a development environment using Codespaces.

## Dockerfile
The Dockerfile sets up the base image and installs the necessary tools and dependencies for developing PCF controls. It is based on the .NET SDK 6.0 image from Microsoft Container Registry and installs the following tools:

curl
build-essential
Node.js
Git LFS
The environment PATH is also updated to include the necessary tools for development.

## devcontainer.json
The devcontainer.json file is used by Codespaces to set up the development environment in the cloud. It includes the following configurations:

- The name of the devcontainer is set as "PCF devcontainer"
- The Dockerfile used is the one included in this repository
- The default shell is set to PowerShell
- The necessary Visual Studio Code extensions are specified: PCF Builder, Power Platform Tools, and GitHub Copilot
- The port 8181 is forwarded to enable local debugging
- The environment variable CHOKIDAR_USEPOLLING is set to 1
- The post-create command installs the necessary Power Platform Actions tools if they are not already present in the workspace
Usage
- To use this template, simply fork this repository and open it in Visual Studio Code with the Remote Development extension installed. Then select the "Reopen in Container" option to start the development environment.

Note: If you run into any issues, make sure to check the devcontainer.json file and update it as necessary to match your requirements.
