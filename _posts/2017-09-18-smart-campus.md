---
layout: post
title: 基于IPv6和物联网的“绿色校园”
subtitle: 项目介绍
author: Arex
catalog: true
tags:
    - Project
---

## Why 

### 需求分析

大学作为人口密集区域，是资源消耗大户，目前有些资源的利用率不高，在节能减排方面还有待提高。
构建智慧校园，实现“一物一地址，万物皆在线”，需要大量的IP地址资源，而IPv4地址早已枯竭，IPv6作为下一代互联网技术，可为世界每一粒沙子编上一个网址。满足端到端的通信和管理需求。
考虑到校园现状，为了解决校园能源浪费现象，为广大学生和老师提供一流的学习、工作、科研环境和各类行政辅助功能。同时结合IPv6技术和物联网技术，提出了基于IPv6技术和物联网技术的绿色校园方案。

## How

### 总体目标

本项目的目的是搭建一个智慧校园平台，从而推进智慧校园建设，提高高校管理的智能化、信息化和网络化水平，实现节能减排的目标。

### 基本思路

1. 实现IPv6网络节点与IP网络设备之间的通信。
2. 感知层通过传感器采集信息。
3. 实现智能设备到终端设备的控制。
4. 实现对校园设备信息的查看。
4. 实现对校园能源设备的智能控制。

### 技术方案

项目立足于IPv6技术与物联网技术来构建绿色校园，主要涉及底层技术与上层应用两大块。
1. 打造基于IPv6技术和物联网技术的绿色校园，首先要解决感知层和网络层之间的通讯问题。但IP网络与无线传感网络并不兼容，利用6LoWPAN技术解决IPv6数据包在IEEE802.15.4网络中的传输问题。
2. 华东理工大学“校园网IPv6技术升级”项目于2012年完成，实现了校园网用户的IPv6普遍访问和校园网信息资源的IPv6普遍服务。借助这一平台，实现“绿色校园”应用层的开发。
打造智慧校园平台，首先实现教室灯控系统。一方面实现其自动控制，通过采集环境信息，尽可能利用日光以及避免“长明灯”现象；另一方面实现其智能手机控制，通过智能手机app在线灯控。

### 总体架构

![architecture](/img/in-post/architecture.jpg)


## What

### 视频介绍

<script src="http://vjs.zencdn.net/4.0/video.js"></script>

<video id="ipv6" class="video-js vjs-default-skin" controls
preload="auto" width="417" height="424" poster="/img/in-post/classroom.jpg"
data-setup="{}">
<source src="/video/smart-campus.mp4" type='video/mp4'>
</video>

### 智慧校园APP

* 在线控制

![light](/img/in-post/light.gif)

* 在线选座

![seat](/img/in-post/seat.gif)
