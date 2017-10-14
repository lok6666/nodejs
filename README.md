# nodejs

为什么选择 Linux 作为开发环境？
  因为现在很多程序的开发环境和部署环境都是 Linux，这样会方便程序的测试和调试，而且可以创造一个学习和使用 Linux 的场景。  
本课程会学到三种类型的应用程序开发，哪三种？
命令行程序、web 网站、Javascript 库  
node.js 是什么？
是一个基于 chrome V8 引擎的 JavaScript 运行环境。  
node.js 作为 JavaScript 的运行环境，包括两层含义，哪两层含义？
一、JavaScript 通过 node.js 在服务器上运行，这样 node.js 好像是 JavaScript 的虚拟机；
二、node.js 提供大量的 API，使 JavaScript 语言与操作系统互动。  
把 node.js API 分为哪两类？
一个是全局对象，一个是普通模块。  
node.js 架构分几层？分别是什么，画图表示？
分三层。
顶层是 node.js 标准库，例如：fs，stream，等模块；
中间层是 node.js 绑定层；
底层有 V8，libuv 等模块。  
阻塞 I/O 和非阻塞 I/O 的区别是什么？
阻塞 I/O 意味着一个或多个请求在处理时要排队。
而非阻塞 I/O ，采用事件轮询的异步模式。
可以理解成：同学们有问题，阻塞 I/O 相当于课上提问，一个一个的来；
非阻塞 I/O 相当于在线上，所有同学把问题发到 QQ 群里，然后老师解决了哪个，就把答案发给谁。  
node.js 的创始人是谁？
Ryan Dahl  
创建新目录的 linux 命令是什么？
mkdir nodejs-demo  
查看当前目录下的文件或文件夹的 linux 命令是什么？
ls 注意：ll 是  ls -l 命令的别名  
进入到某个子目录的 linux 命令是什么？
cd dir-name    
如何清空命令行的内容？
Ctrl-L  
创建并打开文件的命令是什么？
vi file-name  
JavaScript 语法中，如何在控制台输出信息?
console.log(msg)  
在 node.js 中运行某个脚本文件的命令是什么？
node file-name  
REPL 是什么？如何进入 REPL 模式？
Read-Eval-Print-Loop 四个单词的首字母缩写，意思是：读取-求值-输出-循环。执行 node 命令，进入 REPL 模式。  
如何退出 REPL 模式？
Ctrl+D  
运行 node.js 脚本文件时要省略 node 命令，如何操作？
在脚本代码前面加入#!/usr/bin/node，并对脚本文件增加可执行权限  
增加 linux 文件的可执行权限，如何操作？
chmod u+x file-name  
复制文件的 linux 命令是什么？
cp source-file dest-file  
查看文件内容的 linux 命令是什么？
cat file-name  
二、开发环境搭建

ova 虚拟机文件，ova 是哪三个单词的缩写。
Open Virtualization Archive 三个单词的首字母缩写，是可交换的单一的虚拟机文件  
vmware workstation 默认安装，创建的 vmnet1 和 vmnet8 网卡，分别支持哪种网络协议。
vmnet1 是桥接模式，vmnet8 是 NAT 模式  
NAT 地址模式中，linux 虚拟机中的 IP 地址上网有什么要求，默认网关地址是什么？
linux IP 地址要和 vmnet8 网卡地址的网络地址相同，默认网关的 IP 地址的网络地址是 vmnet8 的网络地址，主机地址是 2  
查看 linux IP 地址的命令是什么？
ifconfig  
如何修改 linux 系统的 IP 地址设置？
vim /etc/sysconfig/network-scripts/ifcfg-ens32  
修改完 IP 地址设置后，如何让 IP 地址立刻生效？
systemctl restart network  
三、vim 编辑器

命令行界面下的文字处理软件主流的是哪三个？
vim, emacs, nano  
vi 缩写于什么？
visual  
vim 是什么的缩写？
visual improved  
怎样启用 vi 和退出 vi？
启动：vi or vi file-name  
退出：:q or :q! or :wq  
如何回到 normal 模式？
ESC  
普通模式中，向左、向右移动一个字符的快捷键分别是什么？向上，向下移动一行的快捷键分别是什么？
h, l, k, j  
普通模式中，移动到当前行首和行尾的快捷键分别是什么？
0, $  
普通模式中，向上翻一页和向下翻一页的快捷键分别是什么？
ctrl-b, ctrl-f  
普通模式中，在当前光标后追加文本的快捷键是什么？在行位追加文本的快捷键是什么？在行首追加文本的快捷键是什么？
a, A, I  
普通模式中，在光标前一行和下一行，添加新行的快捷键分别是什么？
O, o  
怎样删除一个字符？怎样删除一行？怎样删除一个单词？
x, dd, dw  
复制当前行和粘贴的快捷键是什么？
yy, p  
怎样同时打开多个文档？
vi file-name1 file-name2  
怎样实现文档之间的切换？
:n, :N  
在插入模式下如何前、后、上、下，移动光标？
ctrl-f, ctrl-b, ctrl-p, ctrl-n  
在插入模式下快捷键如何删除当前光标前的一个单词？如何删除当前光标到行首？如何删除当前光标到行尾？
ctrl-w, ctrl-u, ctrl-k  
