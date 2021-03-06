﻿================================================================================
                                样例使用说明
================================================================================
版本历史
日期        版本    负责人         IAR     MDK     GCC     描述
2019-06-20  1.0     Wuze           7.70    5.16    8.3.1   first version
================================================================================
平台说明
================================================================================
GCC工程，由Eclipse IDE外挂GNU-ARM Toolchain，再结合pyOCD GDB Server实现工程的编译、
链接和调试。在用Eclipse导入工程后，请将xxxx_PyOCDDebug中pyocd-gdbserver和SVD文件
设置为正确的路径；请将xxxx_PyOCDDownload中pyocd设置为正确的路径。注意，这些路径不
能包含非英文字符。


功能描述
================================================================================
本例程展示了TIMER2作为简单计数器的配置和用法。

说明：本例程可设置TRIGA（P30）的上升沿（下降沿）或外部中断事件2（EVT_PORT_EIRQ2，按键
     SW1，Pin P22）作为同步计数时钟。选择TRIGA的上升沿时，当上升沿（下降沿）产生时，寄
     存器CNTAR加1；当选择事件EVT_PORT_EIRQ2时，按下SW1，寄存器CNTAR加1。应用时，可指
     定上升沿（下降沿）或事件发生的次数，结合TIMER2中断，当指定次数的上升沿（下降沿）或
     事件产生后，会产生相应的中断；也可以直接读取寄存器CNTAR，获取上升沿（下降沿）或事件
     发生的次数。

================================================================================
测试环境
================================================================================
测试用板:
---------------------
STK_HC32M120_LQFP48_050_V11

辅助工具:
---------------------
无

辅助软件:
---------------------
无

================================================================================
使用步骤
================================================================================
1）打开工程并重新编译；
2）启动IDE的调试功能，将断点设置在中断回调函数Timer2GCmp_IrqHandler中；
3）如果同步时钟选择的是事件EVT_PORT_EIRQ2，那么按下5次SW1后，程序会停留在断点处；
3）如果同步时钟选择的是TRIGA的上升沿，那么5次上升沿后，程序会停留在断点处。

================================================================================
注意
================================================================================
无

================================================================================
