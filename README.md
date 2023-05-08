# tdps2023
Private repo for TDPS course of Glasgow College

---

## 视觉识别处理Openmv

README: [go to this file](./openmv/README.md)

**TODO**

- [x] 路面识别
- [ ] 箭头识别
- [ ] 箭头方向识别
- [x] 数据传输：UART



## 底盘Arduino

README：[go to this file](./Arduino/README.md)

**TODO**

- [x] 麦轮小车搭建
- [x] PID
- [x] 指令接收和处理



## 3D Design

README：[go to this file](./3d_design/README.md)

**TODO**

- [x] OpenMv 云台固定件
- [x] 超声波固定件
- [x] 机械臂支撑台



## 主控

README：[go to this file](./mcu/README.md)

**TODO**
- [x] 移植Arduino部分代码
- [x] 移植舵机部分代码
- [x] 移植飞控（陀螺仪）代码
- [X] 移植通信模块部分代码
- [ ] 综合编程（是否使用RTOS？）
- [ ] 测试


## PCB

Wiring: [go to this file](./PCB/README.md)
目前统计了所有的接线方式，准备开始制作PCB
## 机械臂

README：[go to this file](./Machine_Arm/README.md)

**TODO**
- [x] 待部件到了连接舵机实现测试
- [x] 第二版 3D 打印建模
- [x] 总体搭建
- [x] 等待实机搭建，固定垫高平台


## 时间和通讯

README：[go to this file](./Timer&Communication/README.md)

**TODO**
- [x] HC12模块之间进行数据传输
- [x] stm32L432KC读取DS3231的当前时间，并返回到电脑上
- [ ] 直接传输时间


## 整体流程

- [ ] 任务1.1需要使用Openmv，对路面进行视觉识别和处理来识别要走的路径。
- [ ] 任务1.2使用一个信标，这个信标是一个箱子，箱子的侧壁与桥平行，通过小车正面的超声波测距感知是否要到桥了，通过小车侧面两个超声波测距来达成与侧壁平行，同时与桥平行，这样就能上桥下桥了，直接莽冲就好。
- [ ] 任务1.3其实和1.1差不多，只需要下桥后让小车转一下，就能直接进入要走的路径
- [ ] 任务2.1要识别箭头和箭头方向，并且撞到对应位置的箭头，目前思路有两个，一个是训练神经网络识别，另一个是直接检测长方形和三角形，判断两个形状连线和连线方向，就知道箭头和箭头朝向
- [ ] 任务2.2要直接走到垃圾桶，这个我们目前想法是通过超声波沿着白色栏杆走
- [ ] 任务2.3是投栏，现在还没想到该怎么检测垃圾桶，投篮方式为正上方 180 度投入框中，会将舵机举高保证能进
- [ ] 任务2.4是返回和传输数据，返回还没想怎么做，反正应该挺简单，传输数据要求传输所有人名字，还有当前时间，时间是做了个外置时钟，可以获取，传输用HC12
