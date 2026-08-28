# About BareMetal PLC's
## Devices 

- [[BareMetal PLC M]]
- [[BareMetal PLC XL]]
## Overview

Bare-metal PLC's Controllers has various powerful features and can service a wide range of applications. Software programming, and commissioning are achieved with the Cmake and C++ languages. To speed up development, you can use the **RLibs** from [here](https://github.com/RoboticsHardwareSolutions/.github/tree/main/profile#rlibs) . **RLibs** are libraries that provide a higher level of abstraction than HAL (Hardware Abstraction Layers). **Rlibs** it is PAL (Platform Abstraction Layer), they solve the most common problems when programming automation, robots, and more. 
## Main benefits 

The key advantage of BareMetal PLC's over standard PLC's is the flexibility and convenience of software development. To create software, you can use ready-made project templates in which all the necessary libraries are connected. The controller is also equipped with step-by-step debugging and programming tools. Development can be carried out using a convenient operating system for you: Linux, macOS, Windows. For development, you can use the C/C++ languages. All development tools are cross-platform. You can also take advantage of CI/CD when developing your products, unlike standard PLCs.
## Programming Languages and Tools

For creating your application you can use next languages:
- C 
- C++

To build your applications, we offer:
- Cmake - [link](https://cmake.org/cmake/help/latest/manual/cmake-language.7.html)

Operating systems used for development:
- freeRTOS - [link](https://www.freertos.org)
- ThreadX - [link](https://threadx.io)
- Zephyr - [link](https://zephyrproject.org)

You can also use the following IDEs:
- Clion - [link](https://www.jetbrains.com/clion/)
- VSCode - [link](https://code.visualstudio.com)
- CubeIDE - [link](https://www.st.com/en/development-tools/stm32cubeide.html)

All BareMetal PLC supports **RLibs**:

## Quick Start Guide 

### Installation
#### Installation Windows 

1) Download and install Visual Studio Code - [Visual Studio Code](https://code.visualstudio.com/)
2) Download and install Github Desktop - [link](https://desktop.github.com/download/)
or:
2) Download and install Git and Enable SSH on Github:
- [Git - Downloads](https://git-scm.com/downloads???windows)  [YouTube Man RU](https://youtu.be/GsG5roSGha0?si=gLXZ9XRwuIu_4bxO)[YouTube Man EN](https://youtu.be/iYkLrXobBbA?si=cfZSbxH9yn8IQFo-)
- Generating a new SSH key and adding it to the ssh-agent - [Github Man](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=windows)
- Auto-launching `ssh-agent` on Git for Windows [Github Man](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/working-with-ssh-key-passphrases#auto-launching-ssh-agent-on-git-for-windows)
- Perhaps this link will also be useful - [Installing OpenSSH Server on Windows 11](https://gbeifuss.github.io/p/installing-openssh-server-on-windows-11/)
- Download and install SourceTree - [link](https://www.sourcetreeapp.com/)
- Add in SourceTree App your Github account and add your SSH key 

#### Installation Mac 
1) `$ brew install git`
2) `$ brew install cmake`
3) `$ brew install homebrew/cask/gcc-arm-embedded` - install **GCC ARM Embedded** 
4) Download and install Visual Studio Code - [Visual Studio Code](https://code.visualstudio.com/)

#### Installation Linux 
1) in process ...  

---

### VSCode Setup for BareMetal PLC Development

#### 1) Recommended Extensions

The `.vscode/extensions.json` file provides automatic tool recommendations when opening the project:

```json
{
	"recommendations": [
		"ms-python.black-formatter",  // Python formatter
		"amiralizadeh9480.cpp-helper",  // C++ assistance
		"marus25.cortex-debug",  // ARM Cortex debugging
		"mcu-debug.rtos-views",  // RTOS visualization
		"twxs.cmake",  // CMake language support
		"ms-vscode.cmake-tools",  // CMake integration
		"zixuanwang.link"  // Symbolic link helper
	],
	"unwantedRecommendations": [
		"ms-vscode.cpptools",  // Conflicts with cortex-debug
		"llvm-vs-code-extensions.vscode-clangd"  // Alternative C++ extension
	]
}
```

#### 2) Debug Configuration

The `.vscode/launch.json` is automatically generated during build via CMake. The template is located in:
- [rhs_core/launch.json.in](https://github.com/RoboticsHardwareSolutions/RHS-BareMetalCore/blob/main/launch.json.in)

> **Note**: Requires Cortex-Debug extension for ARM microcontroller debugging.

---
### Project Setup Guide

#### Option 1: Basic Clone (For End Users)
```sh
git clone  https://github.com/RoboticsHardwareSolutions/RPLC_Quick_Project
cd RPLC_Quick_Project
git submodule update --init --recursive
```
#### Option 2: Fork & Clone (For Contributors)

1. Fork the repository:
    - Navigate to [RPLC_Quick_Project](https://github.com/RoboticsHardwareSolutions/RPLC_Quick_Project)
    - Click "Fork" (creates `github.com/your-username/RPLC_Quick_Project`)
2. Clone your fork:
```sh
git clone https://github.com/your-username/RPLC_Quick_Project
cd RPLC_Quick_Project
git submodule update --init --recursive
git remote add upstream https://github.com/RoboticsHardwareSolutions/RPLC_Quick_Project
```
#### Hardware Target Selection
In `CMakeLists.txt`, specify your PLC model by uncommenting one of:
```cmake
set(RPLC_M)  # Basic model
# set(RPLC_XL)  # Advanced model
```

This automatically configures:
- Compiler flags
- Peripheral libraries
- Memory mapping
- Hardware-specific drivers


