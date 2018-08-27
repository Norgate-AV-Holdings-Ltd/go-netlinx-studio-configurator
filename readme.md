# NetlinxStudioConfigTool : Go based tool for configuring AMX Netlinx Studio installations

## Overview [![GoDoc](https://godoc.org/bitbucket.org/solo_works/netlinxstudioconfigtool?status.svg)](https://godoc.org/bitbucket.org/solo_works/netlinxstudioconfigtool)

This package produces a tool to allow automatic configuration of various settings for AMX Netlinx Studio. These include setting of default folders for Module, Include and Library files for centralised code.

It was created to automate the process of pointing new installations at our core files.

## Compile and Run

Clone the repo and build using Go Build

## Download PreCompiled

Versioned Binaries are in the near future

## Command Line Settings

Clear all existing Folder settings (Keeps all defaults i.e. with AMXShare in the path)
```console
> NetlinxStudioConfigTool -Clear 
```

Specify a config file for use (Default: config.json)
```console
> NetlinxStudioConfigTool -Config xxx.json 
```

## Configuration File
Sample config file (config.json)
```json
{
  "BasePath": "%USERPROFILE%\\Documents\\BitBucketRepos\\SoloWorksAMX",
  "Modules": [
    "ModulesDuet",
    "ModulesNetlinx",
    "ModulesDuetRms",
    "ModulesNetlinxRms"
  ],
  "Includes": [
    "Includes",
    "IncludesRms"
  ],
  "Libs": [],
  "CompileWithDebug": true,
  "CompileWithSrc": false,
  "SmartTransfer": true,
  "SendSource": false,
  "TabWidth": 3,
  "IndentWidth": 3
}
```

## Windows Registry

The application will update registry keys in thej following locations:
- Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\AMX Corp.\NetLinx Studio\NLXCompiler_Includes
- Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\AMX Corp.\NetLinx Studio\NLXCompiler_Modules
- Computer\HKEY_CURRENT_USER\Software\AMX Corp.\NetLinx Studio\Editor Preferences
- Computer\HKEY_CURRENT_USER\Software\AMX Corp.\NetLinx Studio\NLXCompiler_Options
- Computer\HKEY_CURRENT_USER\Software\AMX Corp.\NetLinx Studio\Batch Transfer User Options

## Author

Created by Sam Shelton for Solo Works London

Find us at https://soloworks.co.uk/