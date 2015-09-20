﻿# WPFSerialAssitan 串口助手
------------------
## 引言
**一款基于C#及WPF的串口助手软件。本串口助手操作方便，UI简洁。软件实现了基本的串口通讯需要的功能，开发者可以基于此添加自定义的功能。此外，可以基于此开发出一些简单的串口控制类软件。本人编写过不少基于串口通讯的软件，希望这个可以对初学者有所帮助。**

## 基本功能
* 串口数据接收
* 串口数据发送，可以手动/间隔自动发送
* 保存串口接收到显示区的数据
* 保存/加载软件配置
* 独创的“简洁视图模式”， 便于用户专注于数据的接收和发送

## 使用帮助
**软件操作比较简单，不作过多的介绍。**


## 测试图片
### 启动初始化截图
![启动初始化截图](https://raw.githubusercontent.com/ChrisLeeGit/SerialAssistant/master/DebugPics/1.PNG)

### 打开端口并接收数据
![打开端口并接收数据](https://raw.githubusercontent.com/ChrisLeeGit/SerialAssistant/master/DebugPics/2.PNG)

### 可自由隐藏的设置面板
![可自由隐藏的设置面板1](https://raw.githubusercontent.com/ChrisLeeGit/SerialAssistant/master/DebugPics/3.PNG)
![可自由隐藏的设置面板2](https://raw.githubusercontent.com/ChrisLeeGit/SerialAssistant/master/DebugPics/4.PNG)

### 简洁无干扰的视图
![简洁无干扰的视图](https://raw.githubusercontent.com/ChrisLeeGit/SerialAssistant/master/DebugPics/5.PNG)

## 使用到的开源库
* 本软件使用的一个开源的Json.Net库，可以非常方便地使用它用Json格式存储配置信息或者加载Json格式的配置文件。其主页为：http://www.newtonsoft.com/json。

## 开发
这个是一个完整的Visual Studio工程，直接Clone下来即可。

## 相关开源项目
暑假同时完成了一个基于Arduino的太阳能自动供水系统。当然，这个系统并没有实际使用上，但是设计的功能基本都实现了。这个项目属于比较综合的了。使用了串口通信的方式与PC端的控制软件进行通信。该PC串口控制软件可以给单片机发送自定义的控制指令，并被执行。所以，便涉及到通信用的自定义的协议设计，Arduino指令解析系统的设计和实现。如果感兴趣的话，也同样可以关注，共同学习进步！！谢谢！以下是项目托管地址：
1. Github地址：https://github.com/ChrisLeeGit/AutomaticWaterSupplySystem
2. CSDN Code地址：https://code.csdn.net/u011193957/automaticwatersupplysystem

# 更新日志
## 2015年9月20日 周日 Version 1.1
### Features
* 新增 软件启动后自动查找可用端口号功能
* 新增 保存接受区数据到指定存储路径功能
* 新增 软件退出前自动关闭已开启的端口号；询问是否保存软件的配置功能
* 新增 快捷保存数据功能(左Ctrl+S)
* 新增 快捷进入/退出“简洁视图模式”功能（左Ctrl+Enter)
* 新增 恢复通过菜单项进入或者退出“简洁视图模式”功能

### Bug Fix
* 修复 软件启动后没有恢复到配置保存的上次关闭的位置
* 修复 退出菜单项无效的问题
* 修复 某种特别情况下，从简洁视图模式恢复时出现崩溃的现象

### Other
* 移除菜单项“保存（S）”，该菜单项功能与面板中保存数据按钮功能重复
* 添加“关于”窗体
* 版本号升级到Version 1.1


## 2015年9月15日 周二 Version 1.0
### Features
* 新增 配置信息保存功能，目前保存的配置信息有：
 * 波特率
 * 奇偶校验位
 * 数据位
 * 停止位
 * 字节编码
 * 发送区文本内容
 * 自动发送时间间隔
 * 窗口状态：最大化|高度+宽度
 * 面板显示状态

* 新增 软件启动后自动加载配置信息功能

### Other
* 移除菜单“加载配置(L)”，改为软件启动后自动查找配置并加载
* 移除菜单“简洁模式”，当手动将三个面板全部隐藏后自动进入“简洁模式”，暂时去除一键进入“简洁模式”功能菜单

### Bug fix
* 加载面板显示配置信息后，面板状态与对应菜单项显示不一致的问题 

