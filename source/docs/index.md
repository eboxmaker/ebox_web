title: 文档
---

欢迎使用 Ebox，本文档将帮助您快速上手。

## 什么是 ebox？

ebox是一个运行在各种单片机平台上的涵盖了驱动层、系统层、标准应用软件层、用户软件层的软件解决方案。它完全屏蔽单片机硬件底层差异性，封装出一套简洁的API共单片机开发者使用。丰富的标准驱动和标准应用，像用Arduino那样方便，性能又远高于arduino。操作系统的支持让eBox满足多任务系统的需求；标准应用提供多种控制算法、通信协议，满足不同应用场所的需求。

ebox寓意简单的盒子，打造单片机开发的软件生态系统，彻底简化单片机编程！！

## 为什么开发ebox开发平台

打造一个单片机软件开发的生态系统，统一不同型号单片机的API接口，为开发者提供一套完整的软件框架，简化单片机的编程。
单片机开发目前存在的几大问题：
* 各大厂家固件库无法统一，编程复杂困难
    官方库在一定程度上降低了编程的复杂度。提供了全面的API接口，可以支持任何一款芯片的任何一个寄存器的读写，正是由于官方需要照顾全面的原因，官方库不能有任何取舍，导致官方库非常庞大。对于用户来说很多功能完全用不上，但是都放在了一起使得用户查阅比较困难，有些函数还比较晦涩，难以理解。官方库最大的缺点就是没有站在用户设计的角度去设计API接口；
* 芯片种类繁多，驱动无法统一
做项目多的人设计过各种各样的电路，其中不乏STM32的电路板，板子到手后，第一件事就调驱动。驱动这一块是比较枯燥无味，而且需要比较细心的一个地方，顺利还好，有了问题既要查软件问题，还要查硬件设计、焊接问题等等，排查起来比较费劲。而且驱动的设计会严重影响整个顶层代码的效率。所以做好一个驱动，难！！！即使这次调节好了，下次设计即使还用到这个芯片但是由于IO引脚变动的原因就要重新修改底层的驱动代码。为了不同的顶层支持，需要添加，删除部分代码。即使最简单化，也还是需要修改IO链接的，仅仅一IO链接也要有好多代码的，各种配置。繁琐，复杂。总之一句话就是驱动重复利用率低！！！
* 标准应用程序库
通信协议：在互联网的时代，设备和设备、设备和人之间的交互越来显得越重要了，标准的通信协议的支持可以让你的硬件瞬间介入互联网。
数学库：工程数学是每一个代码工程师必不可不面对的问题，在工程中经常会用到大量的数学运算来满足系统的控制、数据处理等。网上找到的各种版本的代码的易读性比较差，兼容性不够高。对于不擅长数学建模，数学和程序之间如何转换的工程师就是个一个很头疼的大问题。
## 支持平台

目前ebox支持以下几个系列芯片

- STM32F1xx
- STM32F4xx
- K60

{% note warn 不同平台用户的开发环境 %}
目前各个单片机的开发环境还没有统一，导致不同平台使用的开发环境不一样，但是其API接口几乎完全兼容
- STM32F1xx和STM32F4xx 使用MDK-ARM开发环境
- K60 使用了IAR开发环境
{% endnote %}

### 安装 Git

- Windows：下载并安装 [git](https://git-scm.com/download/win).
- Mac：使用 [Homebrew](http://mxcl.github.com/homebrew/), [MacPorts](http://www.macports.org/) 或下载 [安装程序](http://sourceforge.net/projects/git-osx-installer/) 安装。
- Linux (Ubuntu, Debian)：`sudo apt-get install git-core`
- Linux (Fedora, Red Hat, CentOS)：`sudo yum install git-core`

### 安装 Node.js

安装 Node.js 的最佳方式是使用 [nvm](https://github.com/creationix/nvm)。

cURL:

``` bash
$ curl https://raw.github.com/creationix/nvm/master/install.sh | sh
```

Wget:

``` bash
$ wget -qO- https://raw.github.com/creationix/nvm/master/install.sh | sh
```

安装完成后，重启终端并执行下列命令即可安装 Node.js。

``` bash
$ nvm install 4
```

或者您也可以下载 [安装程序](http://nodejs.org/) 来安装。

### 安装 Hexo

所有必备的应用程序安装完成后，即可使用 npm 安装 Hexo。

``` bash
$ npm install -g hexo-cli
```
