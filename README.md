# Getting started

This repository contains a Visual Studio Code [.devcontainer](https://code.visualstudio.com/docs/remote/containers) prepared to include many dependencies required to do full stack software development for a range of popular stacks, including:

- Frontend development - NodeJS and NPM
- Backend development - JAVA and .NET
- Cloud development - CLIs for Azure and AWS

In order to use this pre-configured devcontainer, you'll need to

- Install [Visual Studio Code](https://code.visualstudio.com/)
- Install  [Docker](https://www.docker.com/) (specifically: [Docker for Windows](https://docs.docker.com/desktop/windows/install/), when running on Windows, please make sure to use the appropriate licensing in this case)
- Install the `Remote - Containers` extension for Visual Studio Code (extension ID: `ms-vscode-remote.remote-containers`)
- Clone this repository using git or by downling it as a .zip file
- Open the root folder of this repository in Visual Studio Code
- Open the root folder of this repository inside the devcontainer by
  - Hitting `F1`
  - Select the `Remote-Containers: Open folder in container...` command
  - Select this repositories root folder

This will restart Visual Studio Code in a mode running inside a Docker container defined by the [./.devcontainer/Dockerfile](./.devcontainer/Dockerfile), and you'll have all the tools listed above readily installed. Just the AWS and Azure CLIs still need to be configured using your own credentials.

⚠️ Please note: on the very first run, opening the dev container will pull and build Docker images, which will take some time and use up some bandwidth - please plan for this.

💡 Please consider this repository as a starting point - you can anytime extend the [./.devcontainer/Dockerfile](./.devcontainer/Dockerfile) and [./.devcontainer/devcontainer.json](./.devcontainer/devcontainer.json) files to install additional dependencies. The easiest path to do so is by adding one of the already prepackaged [features](https://github.com/microsoft/vscode-dev-containers/tree/main/script-library)