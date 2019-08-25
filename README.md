# posh-cli [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![posh-cli](https://img.shields.io/powershellgallery/v/posh-cli.svg?style=flat-square&label=posh-cli)](https://www.powershellgallery.com/packages/posh-cli/)

[![Build Status](https://dev.azure.com/christophbergmeister/posh-cli/_apis/build/status/bergmeister.posh-cli?branchName=master)](https://dev.azure.com/christophbergmeister/posh-cli/_build/latest?definitionId=41&branchName=master)

A meta module to bootstrap CLI tab completion PowerShell modules.

## Usage

```pwsh
Install-Module -Name posh-cli -Repository PSGallery
Install-TabCompletion
```

## Overview

The module analyses the installed CLIs and installs modules from the PSGallery that help with the tab completion. It automatically executes and adds the necessary calls for initialisation of the installed tab completion modules to your `$PROFILE`.

Currently it is aware of the following modules.

| CLI    | PowerShell tab completion module                                                      | Remarks                         |
| ------ | ------------------------------------------------------------------------------------- | ------------------------------- |
| cargo  | [posh-cargo](https://www.powershellgallery.com/packages/posh-cargo)                   |                                 |
| dcos   | [posh-dcos](https://www.powershellgallery.com/packages/posh-dcos)                     |                                 |
| dotnet | [posh-dotnet](https://www.powershellgallery.com/packages/posh-dotnet)                 |                                 |
| docker | [posh-docker](https://www.powershellgallery.com/packages/posh-docker)                 |                                 |
| git    | [posh-git](https://www.powershellgallery.com/packages/posh-git)                       |                                 |
| mvn    | [MavenAutoCompletion](https://www.powershellgallery.com/packages/MavenAutoCompletion) | Minimum PowerShell Version: 6.0 |
| npm    | [npm-completion](https://www.powershellgallery.com/packages/npm-completion)           |                                 |
| scoop  | [scoop-completion](https://www.powershellgallery.com/packages/scoop-completion)       |                                 |
| vsts   | [posh-vsts-cli](https://www.powershellgallery.com/packages/posh-vsts-cli)             |                                 |
| yarn   | [yarn-completion](https://www.powershellgallery.com/packages/yarn-completion)         |                                 |

Should new modules be added to the list, then just calling `Install-TabCompletion` is sufficient as the list is stored remotely and does not require an update of `posh-cli` itself.
