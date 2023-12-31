# 🌟 pulsar
- An OpenGL space simulation

## 🚀 How to build the project (assuming you have C++ set up)
### 🪟 Windows
- Install [Visual Studio](https://visualstudio.microsoft.com/)
- Within Visual Studio, install Desktop development with C++
- Install [CMake](https://cmake.org/download/), then open it
- Set `Where is the source code` to the `pulsar` folder
- Set `Where to build the binaries` to the `build` folder inside `pulsar`
- Click `Configure`, then `Generate`, then `Open Project` in Visual Studio
- Right-click `main` in Solution Explorer and click `Set as Startup Project`
- Click the `Local Windows Debugger` button in the top bar to test run the project

### 🐧 Linux/WSL
- Install CMake with `sudo apt install cmake`
- cd into `build`
- type `cmake ..`
- type `make`
- type `./main` to test run the project
