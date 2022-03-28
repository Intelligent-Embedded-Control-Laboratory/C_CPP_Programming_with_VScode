# C++ programming with Visual Studio Code (Using gcc/g++ with MinGW)

To use the GCC (g++) C/C++ compiler and GDB debugger from mingw-w64, this tutorial teach you about how to install the MinGW and C/C++ extension for VS Code. 

## Prerequisites

### Install Visual Studio Code and C/C++ extension for VS Code

1. Install [Visual Studio Code](https://code.visualstudio.com/Download): choose "Windows" to download the installer.

![](https://i.imgur.com/tyiFMzi.png)

2. Choose "I accept" and press "Next".

![](https://i.imgur.com/kVYpvPF.jpg)

3. Set your install path and press "Next".

![](https://i.imgur.com/Q3qWFkZ.jpg)

4. Press "Next".

![](https://i.imgur.com/EvnpvXe.jpg)

5. Tick these two options for "Open with Code" in [**"Create code file and enjoy it"**](https://hackmd.io/ICMRU7uUQuebYsc_LeL-Ug?both#Create-code-file-and-enjoy-it)

![](https://i.imgur.com/UYOyPPl.jpg)

6. Press "Install".

![](https://i.imgur.com/8PrI3xp.jpg)

7. After the installation finish, close the window and open the VScode.

![](https://i.imgur.com/kWYllYg.png)

8. Install the C/C++ extension for VS Code by searching for 'c++' in the Extensions view (`Ctrl+Shift+X`).

![](https://i.imgur.com/lAj5SLM.jpg)


### Install MinGW

1. Install [MinGW - Minimalist GNU for Windows](https://sourceforge.net/projects/mingw/). <span class="red"> Please change the directory path to which you can find easily. </span>

![](https://i.imgur.com/upkZbx4.jpg)

2. Open MinGW Installation Manager, and mark <span class="red"> "mingw32-base" </span> and <span class="red"> "mingw32-gcc-g++" </span> for installation.

![](https://i.imgur.com/ujiimdM.png)

3. Click "Apply Changes" and "Apply". 

![](https://i.imgur.com/FqbuzWO.png)

4. Click "Apply". 

![](https://i.imgur.com/7AU2kE8.jpg)

5. Wait for the installation.

![](https://i.imgur.com/mep8dYL.jpg)

### Add the MinGW path to the Windows `PATH` environment 

1. Open your Windows Settings.

![](https://i.imgur.com/iEXRpae.jpg)

2. Search "Edit environment variables for your account (編輯您的帳戶的環境變數)".

![](https://i.imgur.com/g6PTZ9O.jpg)

3. Choose the "Path" in user variables, and edit it.

![](https://i.imgur.com/ZATRvFU.jpg)

4. Open your MinGW directory path which you select above to the system path, and copy the path of the `bin` folder.

![](https://i.imgur.com/vLdUsEW.jpg)

5. Select "New" to add the path of your `bin` folder under the MinGW directory path.

![](https://i.imgur.com/RSIK4g3.jpg)

6. Select "OK" to save the updated path.

### Check your MinGW installation

1. Search "cmd", and open "Command prompt (命令提示字元)".

![](https://i.imgur.com/fEHa2nE.jpg)


2. Type following command:

```
gcc --version
g++ --version
gdb --version
```

![](https://i.imgur.com/fMzl0PI.jpg)

3. If you don't see the version information or the command is not recognized, please check your "path" of MinGW folder and make sure your installation process correctly.

## Create code file and enjoy it

1. You can open your folder and right-click to <span class="red"> open with code </span>. (Ref: Step.5 in [Install Visual Studio Code and C/C++ extension for VS Code](https://hackmd.io/ICMRU7uUQuebYsc_LeL-Ug?both#Install-Visual-Studio-Code-and-CC-extension-for-VS-Code))

![](https://i.imgur.com/nC2Dnqk.jpg)

2. You can create a `.cpp` file by click the <span class="red"> "New File" </span>, and program your code.

![](https://i.imgur.com/JT7X5ip.jpg)

* For C:
```c=1
#include <stdio.h>
#include <stdlib.h>

int main() {
    printf("Hello\n");
    return 0;
}
```

* For C++:
```cpp=1
#include <iostream>

using namespace std;

int main() {
    cout << "Hello" << endl;
    return 0;
}
```

3. Press `Ctrl+Shift+B` and select "C/C++: gcc.exe" or "C/C++: g++.exe" to build your code.

![](https://i.imgur.com/CXbb588.jpg)

4. You will find the `.exe` file in the workspace.

![](https://i.imgur.com/2hlBu4E.jpg)

5. Press ``` Ctrl+Shift+` ``` to open terminal, and type <span class="red"> `.\FileName.exe` </span> to run the executable file.

![](https://i.imgur.com/u5SiHd2.png)

6. Congratulation! You have completed the basic environment construction. If there is a problem with your compilation step, stay tuned for the next tutorial update. ^_−☆

<!-- ## Build (compile) the program with task.json -->
