<!-- markdownlint-disable MD033 MD041 -->
<p align="center">
  <img alt="LOGO" src="assets/resource/image/Ogasawara.png" width="256" height="256" />
</p>

<div align="center">

# Maa-HBR

<!-- prettier-ignore-start -->
<!-- markdownlint-disable-next-line MD036 -->
基于Maa全新架构的HBR自动化小助手
<!-- prettier-ignore-end -->

![GitHub License](https://img.shields.io/github/license/KarylDAZE/Maa-HBR)
![GitHub Repo stars](https://img.shields.io/github/stars/KarylDAZE/Maa-HBR)
![GitHub Downloads (all assets, all releases)](https://img.shields.io/github/downloads/KarylDAZE/Maa-HBR/total)
[![mirrorc](https://img.shields.io/badge/Mirror%E9%85%B1-%239af3f6?logo=countingworkspro&logoColor=4f46e5)](https://mirrorchyan.com/zh/projects)

</div>

## 简介

本项目使用图像识别+模拟控制，用于简化Heaven Burns Red/炽焰天穹/绯染天空/红烧天堂每日流程。

由 [MaaFramework](https://github.com/MaaAssistantArknights/MaaFramework) 和 [MFAWPF](https://github.com/SweetSmellFox/MFAWPF) 强力驱动


## 环境要求
安装[**vc_redist**](https://aka.ms/vs/17/release/vc_redist.x64.exe)运行库

使用MFAWPF GUI需要安装[**.NET8**](https://dotnet.microsoft.com/zh-cn/download)框架


## 快速开始

视频演示：[自动化脚本Maa-HBR正式发布](https://www.bilibili.com/video/BV1xs14Y6ELJ)

下载[Releases](https://github.com/KarylDAZE/Maa-HBR/releases)最新发行版中所用平台对应的压缩包，解压后打开Maa-HBR.exe即可开始使用。

1. 勾选需要进行的任务，并用拖动的方式将任务按执行顺序排好。
2. 搜索并连接到自己的adb设备（模拟器）或Win32窗口，
3. 配置好MFA相关设置，如可以尝试使用多种屏幕捕获方式，选择截图时间相对较短的一种。
4. 启动任务

GUI界面：![GUI](assets/resource/image/GUI.png)


## 注意事项
- **队伍名称需包含队伍序号(01-20),小于10的队伍序号需带前导0。如:03时之修炼场,12宝石棱镜战。**
- 尽量保证模拟器截图时间不要太高，游戏资源加载和网络速度不能过慢，否则可能出现识别出错或超时。
- “启动游戏”任务中加入了从部分场景回到游戏主页的判断，但最好是从游戏未运行的状态，或者游戏主页开始启动任务，否则可能无法识别当前界面。
- 合理安排任务顺序（或者直接按默认顺序执行），如先清体力再领取任务奖励；最后运行剧情迷宫挂机/竞技场/时之修炼场。
- 如需使用相应功能，请提前设置好战斗相关设置、时之修炼场挑战设定、不同战斗场合对应的队伍等。战斗方式仅支持auto，需要设置好AUTO-FULL方式下的攻击技能释放模式以及角色技能的自动配置，如：![攻击技能释放模式](assets/resource/image/FightSettings1.png)
![角色技能自动配置](assets/resource/image/FightSettings2.png)


## Q&A
- Q：为什么竞技场和时之修炼场需要在线挂机？
- A：竞技场和时之修炼场离线挂机的每场战斗耗时分别min(通关时间+20s,50s)和min(通关时间+20s,80s)，而在线挂机每场战斗的“额外消耗时间”（过场和加载时间）约为8s左右（如果设备和网络环境较差，耗时可能更长）（当前游戏版本普遍存在长时间挂机后游戏变得非常卡顿的情况），即每场战斗耗时为通关时间+额外消耗时间=通关时间+8s，收益更高。
- Q：为什么要在剧情迷宫挂机？
- A：1、剧情迷宫刷取斩突打溶液效率远高于竞技场和时之修炼场。2、剧情迷宫战斗可以提升技能等级，而竞技场和时之修炼场不行。
- Q：为什么要在技术模拟战挂机？
- A：技术模拟战可以在竞技场/时之修炼场离线挂机的同时挂机，并且可以升级风格技能，但效率可能低于剧情迷宫挂机。

## TODO

- [ ] 自动炼金
- [ ] 饰品自动洗词条
- [ ] 刷属性回廊
- [ ] 夏日泳装热带庆典挂机
- [ ] BOSS战失败重新挑战？


## 问题反馈
可以直接在[github issues](https://github.com/KarylDAZE/Maa-HBR/issues)发布issue，附上**详细的问题描述，相关截图，以及Maa-HBR目录下debug/maa.log文件**。


## 鸣谢

### 开源库

- [MaaFramework](https://github.com/MaaAssistantArknights/MaaFramework)  
基于图像识别的自动化黑盒测试框架
- [MFAWPF](https://github.com/SweetSmellFox/MFAWPF)  
基于 MAA 全新架构的 通用 GUI。