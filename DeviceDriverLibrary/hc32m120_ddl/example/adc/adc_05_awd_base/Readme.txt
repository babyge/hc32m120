﻿================================================================================
                                样例使用说明
================================================================================
版本历史
日期        版本    负责人         IAR     MDK   描述
2019-06-17  1.0     Wuze          7.70    5.26  First version
================================================================================
功能描述
================================================================================
本例程用AWD0（模拟看门狗0）和AWD1来监测电位器的输出电压，以检测AWD0和AWD1的工作情况。
程序展示了模拟看门狗的基本配置和使用方法。

说明：
AWD0和ADW1的通道分别为ANI9（P00）和ANI10（P01）。开发板上，只有一个电位器，并只连
接到P00，在测试时可将P01和P00短接，以方便测试。


================================================================================
测试环境
================================================================================
测试用板:
---------------------
STK_HC32M120_LQFP48_050_V11

辅助工具:
---------------------
USB转串口工具

辅助软件:
---------------------
串口调试助手

================================================================================
使用步骤
================================================================================
1）USB转串口工具连接至USART3，并与电脑相连；用MicroUSB将开发板与电脑相连；
2）打开工程，重新编译，下载至开发板并运行；
3）缓慢旋转电位器，可看到串口调试助手显示AWD0和AWD1各自的电压区间、比较方式、电压值以及
   是否满足各自的比较条件；
4）也可用断点调试的方式来观察程序运行情况。


================================================================================
注意
================================================================================
请根据电位器输出电压的范围来设置AWD0和AWD1的比较区间。

================================================================================