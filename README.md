#小修改的 putty

## 说明 ##
Windows7 有32位的版本，还有另一个版本不是32位的，那个版本的位数是32位的两倍。但为了避免本网面被封，32位的两倍，我们不用十进制，可以使用十六进制，叫做 Windows7 0x40位或Windows7 0x40位。

Windows7 has two versions, one is 32bit, anther one is twice 32bit. in order to prevent blocking this page in China. We can't call it in decimal, but we can name it in hexadecimal. So I get a Windows7, 0x40 bits version.

## 改动 ##
这是从 putty 原网站下载源代码后做一些小改进。
> 串口默认设置
    * 端口：COM3
    * 波特率：115200
    * 流控制：无
> 右Alt键
    * 在界面上增加了一个选项可以使右Alt键有效
Serial default setting
    * Port: com3
    * Baudrate: 115200
    * Flow Control: NONE
Right Alt key
    * Enable right Alt key by default
    * add a checkbox to control right Alt key.
> > > Terminal -> keyboard ->...

## 下载 ##
putty，跟原网站说的一样，是一个安全产品。所我我做的修改只能以源码的形式提供，而不提供修改后编译生成的 putty.exe。
你可以从原网站下载源码，再下载我修改后的源码，进行对比，以审阅修改的内容重新编译，再决定使用。
Download? For security reason, please build putty yourself.

## 编译 ##
修改后的代码使用 VC2010SP1 来编译，编译方法:
  1. 打开VC2010命令行
  1. 进入 putty\WINDOWS 目录
  1. nmake -f MAKEFILE.VC

Build putty from source, please checkout the original putty's README.

## 相关连接： ##
VC2010SP1 下载地址
  * http://download.microsoft.com/download/E/B/A/EBA0A152-F426-47E6-9E3F-EFB686E3CA20/VS2010SP1dvd1.iso
  * http://download.microsoft.com/download/2/3/0/230C4F4A-2D3C-4D3B-B991-2A9133904E35/VS10sp1-KB983509.exe

原版putty的源代码
  * http://the.earth.li/~sgtatham/putty/latest/putty-src.zip
  * http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html


## 常见问题 ##

  * 中文版 Windows7 0x40位，VC2010 编译，出现0x463错误
```
D:\wo\putty-googlecode\putty\WINDOWS>nmake
Microsoft (R) Program Maintenance Utility Version 10.00.30319.01
Copyright (C) Microsoft Corporation.  All rights reserved.

        link   -out:pageant.exe -map:pageant.map @pageant.rsp
LINK : fatal error LNK1123: failure during conversion to COFF: file invalid or c
orrupt
NMAKE : fatal error U1077: '"C:\Program Files (x86)\Microsoft Visual Studio 10.0
\VC\BIN\link.EXE"' : return code '0x463' Stop.
```
使用VC2010SP1 或者英文版的 Windows7 0x40 ，都没有问题。
  * 中文版 Windows7 0x40位，在 About 对话框里，版权符号乱码(c)
这个应该是字符集的问题，如果使用英文版的 Windows7，就不会出这个问题，所以原版作者应该没遇到这个问题。技术派的解决方法是设置正确的字符集，结果派的解决方法是安个英文版...