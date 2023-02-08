# 环境搭建

只讲单文件 C++ 程序编写和编译运行

按照本文的搭建结果应该是：代码编辑器 + 编译器 + 终端 + 一些脚本(optional)。

警告：Mac 网络赛和现场赛都用不了，但是 Mac 是基于 Unix 的，可以参考 Linux 中的内容

## 代码编辑器

首先不采用任何 IDE 的原因是避免依赖，讲更加通用的方法。程序设计竞赛现场赛多是使用提供的机器，不保证IDE的安装。不希望再有任何关于 IDE 使用的问题。

代码编辑器选择有很多，选喜欢的即可，例如：Vim, Vscode(无插件），gedit, sublime, notepad++, 忽略功能按钮的 IDE， 等等...

## 编译器

### Linux

g++，安装后一般无需额外配置

### Windows

如果使用 WSL, 则同 Linux，后续不再强调

第一步，下载按照下列之一，建议装64位的，建议选 TDM-gcc，根据经验编译的会快一点，也比较好装。

1. [TDM-gcc](https://jmeubank.github.io/tdm-gcc/) 也可以下载群文件工具目录中有 `tdm-gcc-10.3.0-2.exe`
2. [Mingw64](https://www.mingw-w64.org/downloads/)
3. [Mingw](https://sourceforge.net/projects/mingw/)

第二步，把 g++.exe 所在路径加入环境变量里

找到安装的路径，应有 bin/g++.exe 把 bin 目录加入 Windows 的环境变量中，
例如 `C:\TDM-GCC-64\bin\g++.exe`, 则应加入 `C:\TDM-GCC-64\bin`。

添加环境变量这里不详细讲了，win10 或以上可以参考[链接](https://jingyan.baidu.com/article/47a29f24610740c0142399ea.html)，win7或以下可以参考[链接](https://jingyan.baidu.com/article/b24f6c82cba6dc86bfe5da9f.html)， 也可以通过百度等所搜引擎学习。

## 终端

如果完成了上述步骤，打开终端输入 `g++ --version` 应该能看到版本号，`gdb --version` 也可以

### Linux

选自己喜欢的即可，现场一定会有 bash

### Windows

cmd 或 git-bash 或 PowerShell 进入后先敲一个 cmd 回车

tip: 在文件夹按住 shift + 右键可以在此打开终端，
git-bash 需要安装的时候配置，vscode 也可以配置终端。

## 编译脚本

IDE 其实就是把编译期提供的信息按它的方式展现出来。这里讲下如何终端进行编译。

假如要编译 main.cpp 文件

```bash
g++ main.cpp -o main
```

在 Linux 下会生成 main 文件，Windows 下会生成 main.exe 文件，如果没有 `-o main` 则会生成 a.out, 复杂一点

```bash
g++ main.cpp -o main -g -Wall -DLOCAL -O0
```

`-g` 表示开启调试符号, `-O0` 关闭所有优化选项，`-Wall` 开启编译警告。

`-DLOCAL` 相当于程序里写了 `#define LOCAL`，多用于调试。

### Linux

例如创建 rc
```bash
#!/bin/bash
g++ $1.cpp -o $1 -g -O0 -Wall -DLOCAL -fsanitize=undefined -fsanitize=address && echo compile_successfully >&2 && ./$1
```

则可以 `./rc A` 编译运行 A.cpp

### Windows

创建 rc.bat

```bat
g++ %1.cpp -o %1 -g -O0 -Wall -DLOCAL && echo compile_successfully && %1.exe
```

则可以 `rc A` 编译运行 A.cpp