## linux shell script

### shell 和 CLI

shell 不是操作系统内核的一部分，而是构建在内核上的一个应用程序，是人与系统交互的介质。

在早期 Linux 系统中，与 Unix 系统进行交互的唯一方式就是借助 shell 所提供的文本命令行（command line interface， CLI）来操作应用程序，管理文件等。

早期亚终端是利用串行电缆链接到 Unix 系统上的一台显示其和键盘，该亚终端是该 Unix 的控制台。现在 Linux 进入 CLI 的方式，可以直接退出图形化模式，进入文本模式，这种模式称作 Linux 控制台，它仿真早期的亚终端。

现代 Linux 启动之后，会自动创建出一些（5-6个）虚拟控制台，其是运行在内存中的终端会话，不要在计算机上硬件连接多个真实的亚终端，当你在图形化 terminal 新建窗口时候，出现的 ttys00x 其实就是连接到已经运行的虚拟控制台-亚终端。

![Image](/blog-2020/images/lss_ttys.jpg)

shell 包含一组内部命令（builtin cmd），用这些命令可以完成诸如设备操作，文件操作，启动停止程序。你也可以将多个 shell 命令放到文件中作为程序串来执行，这些文件被称为 shell 脚本。

在 Linux 系统上，通常有好几种 shell 可用，不同的 shell 有不同的特征。不同 shell 的脚本之间不一定能够移植使用，由于几乎所有 Linux 发行版（除了 Ubuntu）都会以 bash shell 作为默认新 shell，所以写 bash shell 脚本会更加通用和朴素。当前有更加强大的 zsh 弥补了 bash 的不足，并且完全兼容 bash 语法。在日常开发使用 zsh 工具会更加强力和顺手。
  
### shell