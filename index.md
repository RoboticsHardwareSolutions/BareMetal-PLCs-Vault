# About BareMetal PLC's
## Devices 

- [[BareMetal PLC M]]
- [[BareMetal PLC L]]
- [[BareMetal PLC XL]]
## Overview

Bare-metal PLC's Controllers has various powerful features and can service a wide range of applications. Software programming, and commissioning are achieved with the Cmake and C++ languages. To speed up development, you can use the **RLibs** from [here](https://github.com/RoboticsHardwareSolutions/.github/tree/main/profile#rlibs) . **RLibs** are libraries that provide a higher level of abstraction than HAL (Hardware Abstraction Layers). **Rlibs** it is PAL (Platform Abstraction Layer), they solve the most common problems when programming automation, robots, and more. 
## Main benefits 

The key advantage of Bare-metal PLC's over standard PLC's is the flexibility and convenience of software development. To create software, you can use ready-made project templates in which all the necessary libraries are connected. The controller is also equipped with step-by-step debugging and programming tools. Development can be carried out using a convenient operating system for you: Linux, macOS, Windows. For development, you can use the C/C++ languages. All development tools are cross-platform. You can also take advantage of CI/CD when developing your products, unlike standard PLCs.
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

#### Installation Linux 

### VSCode settings

1) Install  Extension - [link](https://marketplace.visualstudio.com/items?itemName=stmicroelectronics.stm32-vscode-extension)
