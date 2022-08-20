# 开发环境的设想（windows）

## WSl 和 hyper-V

### hyper-V

​	在windows上，以虚拟机的方式运行多个操作系统

* hyper-V 提供硬件虚拟化，这意味着每个虚拟机都在硬件上运行。
* hyper-V 允许你创建虚拟硬盘驱动器、虚拟交互机，以及其他虚拟设备，这些都可以添加到虚拟机中

前提：windows10 64位专业版，企业版，教育版（无法使用家庭版）

#### 安装Hyper-V

1. 使用powershell   

```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All

# 管理员身份安装后，重启
```

2. 通过“设置”启用 Hyper-V 角色

* 右键单击 Windows 按钮并选择“应用和功能”。
* 选择相关设置下右侧的“程序和功能”。
* 选择“打开或关闭 Windows 功能”。
* 选择“Hyper-V”，然后单击“确定”。

#### 创建虚拟机

​	前提：[Windows 10 Fall Creators Update (v1709) 及更高版本](https://docs.microsoft.com/zh-cn/virtualization/hyper-v-on-windows/quick-start/quick-create-virtual-machine#windows-10-fall-creators-update-windows-10-version-1709)

1.  Fall Creators Update 中

* 从“开始”菜单中打开“Hyper-V Quick Create”。
* 选择一个操作系统或者使用本地安装源选择你自己的操作系统。
* 如果你想要使用自己的映像创建虚拟机，请选择 **Local Installation Source**。
* 选择 **Change Installation Source**。
* 选择要转变为新虚拟机的 .iso 或 .vhdx。
* 如果映像为 Linux 映像，请取消选择“安全启动”选项。

#### 技术参考

[微软Hyper-V 官方参考](https://docs.microsoft.com/zh-cn/virtualization/hyper-v-on-windows/quick-start/quick-create-virtual-machine)

### WSl

#### WSl

​	wsl：适用于Linux的windows的子系统，可以让开发人员按原样使用GNU/Linux环境-包括大多数命令行工具，应用程序等。

且不会产生传统虚拟机或双系统设置开销

#### 安装WSl

1. [在 Microsoft Store](https://aka.ms/wslstore) 中选择你偏好的 GNU/Linux 分发版。
2. 使用类似于 Unix 的命令行 shell 调用 Windows 应用程序。
3. 在 Windows 上调用 GNU/Linux 应用程序。

#### WSL2

​	wsl2 是适用于linux的windows子系统体系的一个新版本

1. 支持适用于 Linux 的 Windows 子系统在 Windows 上运行 ELF64 Linux 二进制文件
2. 主要目标是**提高文件系统性能**，以及添加完全的系统调用兼容性

## neovim

## tmux

## vim

## zsh

