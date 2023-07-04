# ubuntu 常用软件安装/配置

## 一、 Anaconda 
(1) 下载网址：[https://www.anaconda.com/download/](url)

(2) 在下载好的文件目录中打开终端，运行 `bash 文件名`，跟着提示操作即可
```
bash Anaconda3-2023.03-1-Linux-x86_64.sh
```

(3) 安装完重启终端后可以看到命令行开头有 (base) 即为安装成功

(4) conda常用命令：

i. 创建虚拟环境：
`conda create --name <env_name> [packages] ：创建虚拟环境，例：`

```
conda create --name carla python=3.8
```

ii. 激活环境：`conda activate <env_name>，例如：`
```
conda activate my_env
```

iii. 其他：
```
    conda env list：列出所有可用的Anaconda环境
    conda list：列出当前环境中安装的所有软件包
    conda install <package_name>：在当前环境中安装指定的软件包
    conda update <package_name>：在当前环境中更新指定的软件包
    conda remove <package_name>：从当前环境中卸载指定的软件包
    conda deactivate：退出当前激活的Anaconda环境
```

(5) 注意：在使用Anaconda时，还可以使用标准的Linux命令来管理文件和目录，例如cd、ls、rm等



## 二、 clash for Windows

(1) 下载链接：[https://github.com/Fndroid/clash_for_windows_pkg/releases](url)

(2) 下载文件：Clash.for.Windows-0.20.21-x64-linux

(3) 将文件解压至安装位置，并打开文件找到名为：cfw 的文件

(4) 在终端中打开并输入：`./cfw` 启动 clash

(5) 在 clash 软件的第一页Genera l—— prot 中找到类似：
```
    export https_proxy=http://123.4.5.6:7080/;
    export http_proxy=http://123.4.5.6:7080/;
    export all_proxy=socks5://123.4.5.6:7080/
```
(6) 将` 123.4.5.6 `和` 7080 `填到：系统设置——网络——网络代理（设置为手动）的 HTTP 代理和 HTTPS代理中即可（HTTPS代理和FTP代理不填好像也可以）

(7) 如果clash软件损坏导致无法打开或无法正常使用，可以将网络代理设置为：已禁用，即可正常联网

(8) 在 clash软件的 profiles 中下载代理即可

(9) 代理链接：
```
    [https://mojie.vip/#/login](url)

    [https://portal.724cloud.org/user](url)

    [https://a.xingjiabijichang.com/#/login](url)

    [https://teacat2.com/#/login](url)
```

## 三、 Visual Studio Code

(1) 可以使用一键安装：
```
wget http://fishros.com/install -O fishros && . fishros
```

(2) vscode软件需安装的插件：
```
ROS
Chinese (Simplified) (简体中文) Language Pack for Visual Studio Code
C/C++
CMake tools
python
```

## 四、 terminator
```
sudo apt install terminator
```

## 五、 搜狗输入法：
下载链接：[https://shurufa.sogou.com/?r=mac&t=pinyin](url)

安装参考：[https://shurufa.sogou.com/linux/guide](url)

## 六、 pycharm
(1) 下载链接：[https://www.jetbrains.com/pycharm/download/#section=linux](url)

(2) 将压缩包解压至软件安装位置，打开目录  ~/pycharm-professional-2023.1.1/pycharm-2023.1.1/bin（找到pycharm.sh文件）

(3) 右键，在终端打开，运行` bash pycharm.sh ` 启动pycharm

(4) 专业版软件可以去pycharm官网用学信网信息获得一年激活时长

(5) 打开软件后，点左下角的设置—— create desktop entry，下次启动就不用使用终端启动  

(6) 安装的插件：chinese(simplified) language pack/中文语言包

## 七、 百度网盘
(1) 下载链接：[https://pan.baidu.com/download#linux](url)

(2) 选择下载.deb格式文件

(2) 终端运行：`sudo dpkg -i 下载文件名`



## 八、 zotero
(1) 下载链接：[https://www.zotero.org/download/](url)
(2) 安装教程：https://www.zotero.org/support/installation
(3) 将下载的安装包提取到安装的位置，然后找到set_launcher_icon文件，在终端运行`./set_launcher_icon`，会生成有一个`zotero.desktop` 文件，将这个文件链接到` ~/.local/share/applications/` 例如：

```bash
ln -s /home/mj/software/Zotero-6.0.26_linux-x86_64/Zotero_linux-x86_64/zotero.desktop ~/.local/share/applications/zotero.desktop
```

就能看到zotero的图标了。


## 九、 Typora
https://blog.csdn.net/qq_39779233/article/details/100551757



## 十、Latex

#### 参考链接：

[知乎：Ubuntu20.04下 VsCode + LaTeX 的使用](https://zhuanlan.zhihu.com/p/451420916)

[github: 电子科技大学学位论文模板](https://github.com/tinoryj/UESTC-Thesis-Latex-Template)

[latex工作室](https://www.latexstudio.net/)

#### 1. 安装 LaTeX：

(1) 终端运行：

```
sudo apt-get install texlive        # 安装TeX Live的核心组件，但可能不包括所有的附加扩展和宏包
sudo apt-get install texlive-full   # 安装TeX Live的所有组件，包括核心组件、所有可用的附加扩展、宏包和文档等
```

只运行：`sudo apt-get install texlive-full`应该就可以了，但是[知乎：Ubuntu20.04下 VsCode + LaTeX 的使用](https://zhuanlan.zhihu.com/p/451420916) 写了两个。

#### 2. vscode安装插件 

```
latex workshop
```

```
LaTeX language support
```

#### 3. 设置settings.json

在vscode按`F1`，输入`settings.json`，选择：打开用户设置(JSON)，添加以下内容

> 如果文件已经有内容，则不需要最大的花括号
>
> 记得在已有内容的最后加逗号：`,`

```json
{
    "latex-workshop.latex.tools": [
        {
          "name": "latexmk",
          "command": "latexmk",
          "args": [
          "-synctex=1",
          "-interaction=nonstopmode",
          "-file-line-error",
          "-pdf",
          "%DOCFILE%"
          ]
        },
        {
          "name": "xelatex",
          "command": "xelatex",
          "args": [
          "-synctex=1",
          "-interaction=nonstopmode",
          "-file-line-error",
          "%DOCFILE%"
            ]
        },          
        {
          "name": "pdflatex",
          "command": "pdflatex",
          "args": [
          "-synctex=1",
          "-interaction=nonstopmode",
          "-file-line-error",
          "%DOCFILE%"
          ]
        },
        {
          "name": "bibtex",
          "command": "bibtex",
          "args": [
          "%DOCFILE%"
          ]
        }
      ],
      
      "latex-workshop.latex.recipes": [
      
          {
              "name": "XeLaTeX",
              "tools": [
                  "xelatex"
              ]
          },
          {
              "name": "PDFLaTeX",
              "tools": [
                  "pdflatex"
              ]
          },
          {
              "name": "BibTeX",
              "tools": [
                  "bibtex"
              ]
          },
          {
              "name": "LaTeXmk",
              "tools": [
                  "latexmk"
              ]
          },
          {
              "name": "xelatex -> bibtex -> xelatex*2",
              "tools": [
                  "xelatex",
                  "bibtex",
                  "xelatex",
                  "xelatex"
              ]
          },
          {
              "name": "pdflatex -> bibtex -> pdflatex*2",
              "tools": [
                  "pdflatex",
                  "bibtex",
                  "pdflatex",
                  "pdflatex"
              ]
          }
      ],

}

```


#### 4. 使用

(1) 创建文件，以`.tex`后缀结尾，注意LaTeX的格式，最简单的格式：

```latex
\documentclass{article}
\usepackage[UTF8]{ctex}
\begin{document}

hello world

\end{document}
```

(2) 使用别人的模板
在github(例如：[github: 电子科技大学学位论文模板](https://github.com/tinoryj/UESTC-Thesis-Latex-Template))或[latex工作室](https://www.latexstudio.net/)找到需要使用的模板

在main.tex文件中点右上角的启动按钮（Build Latex Project）即可编译



## 十一、 ROS

#### 1. 使用鱼香ROS的一键安装指令：
```
wget http://fishros.com/install -O fishros && . fishros
```
该指令可以换源、安装ROS、vscode、wechat等

#### 2. 安装完ROS后需要安装的包：
```
sudo apt install ros-noetic-gmapping
sudo apt install ros-noetic-map-server
sudo apt install ros-noetic-navigation
sudo apt install ros-noetic-costmap-2d
sudo apt-get install ros-noetic-nav-core
sudo apt-get install ros-noetic-navigation
# 可能是我这次在（base）环境中装ros，然后在虚拟环境中编译运行等，很多东西都没装
pip install empy
pip install catkin_pkg
pip install rospkg
pip install defusedxml
pip install numpy
```



## 十二、 Nvidia显卡驱动安装

系统：ubuntu20.04.6

电脑：联想r9000p 2021H 3060

问题缘由：笔记本外接显示器异常，可以检测到副屏但无法正常显示，无法正常使用

#### 1. 检查是否已安装nvidia显卡驱动

终端输入： 

```
nvidia-smi
```

没有返回显卡相关信息，即说明安装ubuntu系统时没有安装nvidia显卡驱动（或者说没装好）


#### 2. 解决方案1（未完全解决）：

使用ubuntu系统软件：软件和更新——附加驱动  安装显卡驱动。

驱动安装成功可以解决外接显示器无法正常显示，但内置显示器无法缩放（内置显示器分辨率2560*1600，125%缩放但效果有150%，将分辨率设置为1920*1200则出现一直闪烁的雪花屏）


#### 3. 解决方案2（完全解决）：

```
  sudo apt-get install -f
  sudo add-apt-repository ppa:graphics-drivers/ppa
  sudo mokutil –sb-state
  lshw -C display
  sudo apt-get install linux-generic-hwe-20.04
  reboot
  sudo apt-get purge nvidia*
  sudo apt-get autoremove
  ubuntu-drivers devices
  sudo apt-get install nvidia-driver-530
  sudo prime-select nvidia
  sudo reboot
  nvidia-smi
```

chatGPT对上述指令的解释：

```
  sudo apt-get install -f       # 用于修复可能出现的依赖问题。
  sudo add-apt-repository ppa:graphics-drivers/ppa      
                                # 用于添加 graphics-drivers/ppa 软件源，方便后续安装 Nvidia 显卡驱动。
  sudo mokutil –sb-state        # 用于检查 Secure Boot 的状态。
  lshw -C display               # 用于查看系统中的显示设备。
  sudo apt-get install linux-generic-hwe-20.04  
                                # 用于安装支持最新硬件的内核和驱动程序。
  reboot                        # 重启系统，以使上述更改生效。
  sudo apt-get purge nvidia*    # 用于卸载系统中所有的 Nvidia 显卡驱动。
  sudo apt-get autoremove       # 用于移除已安装但不再需要的软件包和其依赖项。
  ubuntu-drivers devices        # 用于列出可用的显卡驱动。
  sudo apt-get install nvidia-driver-530    
                                # 用于安装 Nvidia 显卡驱动版本 530。
  sudo prime-select nvidia      # 用于将 Nvidia 显卡设置为系统默认显卡。
  sudo reboot                   # 重启系统，以使上述更改生效。
  nvidia-smi                    # 用于检查 Nvidia 显卡的状态和性能信息。
```