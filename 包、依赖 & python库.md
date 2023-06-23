# 包、依赖 & python库
## 1. 包：
通常指软件包，指软件的打包形式，它包含了可执行文件、库文件、配置文件和其他相关的资源文件，是软件在Ubuntu软件仓库中的单位，可以通过包管理工具进行下载、安装、更新和卸载。

## 2. 依赖：
安装或运行某个软件包时，所需要的其他软件包、库、模块或者特定的版本。一些软件包需要其它软件包被安装才能正常运行或运行得更好。

包和依赖的概念可以相互关联。一个包可能依赖于其他的包或库，以提供所需的功能。

## 3. Python库：
指提供了一系列函数、类和模块的代码集合，用于解决特定的问题或提供特定的功能。

Python库可以是官方提供的标准库，也可以是第三方开发者提供的库。它们可以被其他的Python程序引用和使用，以实现特定的功能。
Python库是一种实现特定功能的代码集合，可以作为包或独立的模块存在。

针对包、依赖和python库等，有以下常见的shell命令：

## 4. apt-get：用于安装和管理软件包
```
sudo apt-get update                     # 更新软件包列表，以获取最新的软件包信息
sudo apt-get upgrade                    # 升级系统中已安装的软件包到最新版本
sudo apt-get install <package_name>     # 安装指定的软件包及其依赖项
sudo apt-get remove <package_name>      # 卸载指定的软件包，同时也会删除其相关的配置文件
sudo apt-get autoremove                 # 自动删除不再需要的软件包及其依赖项
sudo apt-get purge <package_name>       # 彻底卸载指定的软件包，包括其配置文件和数据
sudo apt-get clean                      # 清理下载软件包时的缓存文件
sudo apt-get autoclean                  # 自动清理已经过期的软件包缓存文件
```
Python库：
```
sudo dpkg -i <package_file.deb>         # 安装指定的.deb软件包文件到系统中
```
该命令多用于安装在官网下载的以 .deb 为后缀的软件安装包

## 6. pip：
```
# 安装指定的python库或软件包
pip install --upgrade <package_name>    # 升级已安装的软件包
pip uninstall <package_name>            # 卸载指定的软件包
pip list                                # 列出当前环境中已安装的所有软件包
pip show <package_name>                 # 查看指定软件包的详细信息，包括版本号、安装路径等
```
## 7. pip3:
```
pip3 install <package_name>             # 安装指定的python库或软件包
pip3 install --upgrade <package_name>   # 升级已安装的软件包
pip3 uninstall <package_name>           # 卸载指定的软件包
pip3 list                               # 列出当前环境中已安装的所有软件包
pip3 show <package_name>                # 查看指定软件包的详细信息，包括版本号、安装路径等
```
## 8. 注意conda list 和 pip3 list 的区别：
conda list： 用列出通过conda安装的包。它不仅显示与Python相关的包，还包括其他非Python软件包和依赖项

pip3 list：用于列出通过pip安装的Python包。它只显示与Python相关的包

在conda环境中使用conda install安装了一个包，然后使用pip list来查看已安装的包
```
conda list                              # 列出当前环境中已安装的所有包
conda env list                          # 列出所有可用的环境
conda env export > environment.yml      # 将当前环境导出到一个YAML文件中
conda env create -f environment.yml     # 从一个YAML文件中创建环境
```

## 9. pip/pip3、apt-get、apt和dpkg 与conda 虚拟环境的关系
在终端中激活了conda的虚拟环境后，可以直接使用pip或pip3命令来安装、升级或卸载Python库。这些命令将针对当前激活的conda环境进行操作

apt-get、apt和dpkg等命令与系统的软件包管理器相关，并不直接与conda环境关联。









9.1231654655415131565
