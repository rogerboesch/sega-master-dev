# Development for the SEGA Mega Drive (on macOS)

## Introduction

This repo holds a more straightforward installation guide for macOS, both Intel and M1/M2 machines.
Binaries are pre-built and templates are adapted to use in Visual Studio Code.


## Copyright

The toolchain is built using the [marsdev repo](https://github.com/andwn/marsdev/tree/master).

All copyrights remain at the respective copyright holders. 
I just tried to save some work and make the installation even more flawless for other macOS programmers.


## Installation

### Dependencies

To use the toolchain, your Mac machine needs some tools installed.
I assume some of them you have already if you are a programmer

- Xcode command line tools
- Homebrew

Everything else is described below

### Packages to be installed with Homebrew

``` bash
$ brew install wget
$ brew install java
```
  
### Add to .zshrc

``` bash
$ echo 'export PATH="/usr/local/opt/openjdk/bin:$PATH"' >> ~/.zshrc
$ echo 'export MARSDEV=${HOME}/mars' >> ~/.zshrc
$ echo 'export GDK=${MARSDEV}/m68k-elf' >> ~/.zshrc
$ echo 'export JAVA_HOME=/usr/local/opt/openjdk' >> ~/.zshrc
```

### Download Toolchain

#### For intel based Mac machines

``` bash
$ cd $HOME
$ wget mars-intel.zip
``` 

#### For M1/M2 based Mac machines

``` bash
$ cd $HOME
$ wget mars-m1.zip
``` 

### Visual Studio Code Integration

#### Recommended VS Code Plugins

- C/C++ by Microsoft
- C/C++ Extension Pack by Microsoft
- Genesis Code by zerasul

#### SGDK Template

All you have to [download](mars-sega-vscode-template.zip) now is the visual studio code template.
This template was initially created by xxx and modified by me to work with the marsdev toolchain

**Clean at first the project**

- Open the folder in Visual Studio Code
- Press Command-P
- Enter ```task clean```

In the output window you see something like this

** Now build the project**

- Press Command-P again
- Enter ```task make```

