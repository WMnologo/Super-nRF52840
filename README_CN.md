
## 简介

Super nRF52840搭载了功能强大的Nordic nRF52840 MCU，集成了蓝牙 5.0连接功能，同时拥有小巧精致的外形，可用于可穿戴设备和物联网项目。单面贴片设计和板载蓝牙天线，可以大大方便物联网项目的快速部署。

Super52840 集成了一个充电指示灯和一个三色LED。有11个数字I/O可用作PWM引脚，6个模拟I/O可用做ADC引脚，支持UART、I2C、SPI三种常见的串行接口。板子上含有一根板载2MB内存，可以使用Arduino、Micropython\CircuitPython或者其他编程语言进行编程。

::: tip

- 处理器：Nordic nRF52840，带 FPU 的 ARM® Cortex®-M4 32 位处理器，64 MHz
- 无线  : 蓝牙 5.0/BLE/NFC
- 内存  ： 256KB RAM、 1MB内存、2MB板载内存
- 接口  ： 1XI2C、1XUART、1XSPI
- PWM/模拟引脚： 11/6
- 板载按键 ： 复位按键
- 板载LED ： 充电指示灯、三合一三色LED
- 编程语音 ：Arduino/MicroPython/CircuitPython
:::

### 原理图

![](/assets/img/keyboard/keyboard_controll/super52840/6.png)

### 引脚图

### 尺寸图

![](/assets/img/keyboard/keyboard_controll/super52840/4.png)

## 入门

::: tip

1、如果您使用 Seeed nRF52 Boards 的板载包，串口功能无法编译。解决方法是在代码中添加行 #include "Adafruit_TinyUSB.h"。您可以从以下位置[下载此包](https://github.com/adafruit/Adafruit_TinyUSB_Arduino "")或者直接在Arduino库中搜索==Adafruit_TinyUSB==并下载。


2、如果你喜欢更简单的方法，你可以从一开始就选择 Seeed nRF52 mbed-enabled Boards。它支持编译串行功能，而无需进行额外修改。
::: 

![](/assets/img/keyboard/keyboard_controll/super52840/5.png)

### 硬件设置

### 软件设置

## 电池充电电流

电池充电电流可选择100mA或200mA，其中可以通过设置Pin13为高或低来改变为100mA或200mA。小电流充电电流是在输入模式设置为HIGH 电平时，大电流充电电流是在输出模式设置为LOW 电平时。

低电流充电

```js 
void setup(){
pinMode (P0_13, OUTPUT);
}
void loop() {
digitalWrite(P0_13, HIGH);
}
```

高电流充电

```js 
void setup(){
pinMode (P0_13, OUTPUT);
}
void loop() {
digitalWrite(P0_13, LOW);
}
```

## 使用板载三色LED

## 功耗验证


## 烧录固件

::: tip
Super52840 使用的是 Xiao nRF52840 的固件，如果需要使用Adafruit、Nice！Nano、Arduino Nano33Ble的固件使用Jlink下载固件就可以。

固件下载需要以下：
- Super52840开发板
- Jlink下载器
- Jlink软件
- 需要烧录的固件
:::
第一步：使用Jlink连接以下引脚

![](/assets/img/keyboard/keyboard_controll/super52840/1.png =300x330 )

第二步：启动J-Flash并搜索nRF52840，创建一个新项目：（[Jlink 软件下载](https://www.segger.com/downloads/jlink/ "")）


![](/assets/img/keyboard/keyboard_controll/super52840/3.png)

第三步：单击“目标”，然后选择“连接”。

![](/assets/img/keyboard/keyboard_controll/super52840/2.png =311x158)

第四步：将bin或[hex文件](https://files.seeedstudio.com/wiki/XIAO-BLE/Seeed_XIAO_nRF52840_Sense_bootloader-0.6.1_s140_7.3.0.hex "")拖入软件。然后依次按F4和F5。刷新完成。




## 疑难解答

==更多问题及有趣的应用，请访问[论坛](https://chat.nologo.tech/ "")  或加入QQ技术交流群：==522420541====


## 购买链接
[淘宝购买](https://item.taobao.com/item.htm?spm=a1z10.3-c.w4002-24438210134.12.7b736ea3Eb38Ak&id=729260528560 "")
