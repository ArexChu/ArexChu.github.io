---
layout: post
title: Classroom intelligent lighting control system
subtitle: Control strategy
author: Arex
catalog: true
tags:
    - Group meeting
    - IPv6
---

## 背景

上位机、**底层**

### 灯光控制系统

智慧照明

全球照明用电占到总用电量的19%，我国照明用电占全社会用电量的13%左右

#### 控制对象

* 白炽灯

![incandescent](/img/in-post/incandescent-light-bulb.png)

* 荧光灯[节能灯(紧凑型荧光灯)]

![fluorescent](/img/in-post/fluorescent-lamps-artistic.jpg)

需要增加调光电路，可调光的范围小

* LED(light-emitting diode)

![LED](/img/in-post/LED.jpg)

不含有毒的汞

PWM(Pulse-width modulation)调光

![PWM](/img/in-post/led-pwm.png)

* 传递信息
* 供电控制

频率->肉眼无法看到的频率：50HZ
开的时间越多（占空比）->提供的电能越多

PWM -> cc2530节点

调光范围0％－100％

|灯|发光能效|使用寿命|
|---|---|---|
|白炽灯|16流明/瓦|1000|
|荧光灯|60流明/瓦|10000|
|LED|150流明/瓦|30000|

#### 控制环境

![classroom](/img/in-post/classroom-reality.jpg)

#### 控制策略

##### 控制环境

* 时间段控制
* 人存在
* 利用日光
* 分区域控制

  	* 教室区
  	* 学生区

![PIR](/img/in-post/pir-motor-module.jpeg)

##### 控制对象

###### 荧光灯 

开、关->开环控制->教室暗，且有人->开灯

![2 step control](/img/in-post/2-step-control.png)

###### LED 

PWM调光->**闭环控制**->利用PWM调光，通过光照度传感器获得反馈，最终达到预设的光照值

![closed loop control](/img/in-post/closed-loop-control.gif)

##### 传感器

* 光照强度，光强传感器

	* TSL2561

![light](/img/in-post/tsl2561-1.jpg)

* 人存在，热释电红外传感器

  	* 配合微波，成本高
	* PIR01A-JSTN

![PIR](/img/in-post/pir-sensor.jpg)

* 配合舵机产生相对运动，克服不能感应禁止的人的缺陷

![PIR](/img/in-post/pir-motor.jpeg)

* 不稳定 

![PIR](/img/in-post/pir-motor-black.jpeg)

* 缩小范围

![PIR](/img/in-post/pir-motor-mask.jpeg)
