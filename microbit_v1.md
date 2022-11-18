<div align="center">
<h1>micro:bit v1</h1>
</div>

## **硬件介绍**

## **官方提供**




<div align = "center">
<iframe src="https://microbit-micropython.readthedocs.io/en/v2-docs/" width="100%" height="400pt" frameborder="1"  scrolling="auto">   
</iframe>
<a href="https://microbit-micropython.readthedocs.io/en/v2-docs/" target="_blank"><button class="button button1">详细查看  <i class='fas fa-search'></i></button></a>
</div>

## **WEEEMAKE扩展API**

### **板载模块**

#### **RGB LED灯**

#### **蜂鸣器模块**

####  **声音传感器**

#### **直流电机**

> [!TIP]
> 使用请先导入microbit模块
> 
> `from microbit import *`

- `motor.init()`
  - 描述：电机驱动前初始化。
  - 参数：无
  - 返回值：无
  
- `motor.runSpeed(index,speed)`
  - 描述：设置电机接口及速度。
  - 参数：
    - `index`：设置电机接口，1为M1，2为2。
    - `speed`：设置电机速度，正速度为顺时针转，负速度为逆时针转,速度范围：-255~255，速度只能为整数。
  - 返回值：无

- 示例：<br>
电机M1、M2正传2s，反转2s。
```python
from microbit import *
import time
 
motor.init()
speed = 255
while True: 
    motor.runSpeed(1,value)
    motor.runSpeed(2,value)
    time.sleep_ms(2000)
    
    motor.runSpeed(1,-value)
    motor.runSpeed(2,-value)
    time.sleep_ms(2000)
```

#### **舵机**

> [!TIP]
> 使用请先导入microbit模块
>
> `from microbit import *`

- `servo.init()`
    - 描述：舵机驱动前初始化。
    - 参数：无
    - 返回值：无

- `servo.angle(index,angle)`
    - 描述：设置舵机接口及角度。
    - 参数：
        - `index`：设置舵机接口，1为Servo1，2为Servo。
        - `angle`：设置舵机旋转角度，范围：0~180，角度只能为整数。
    - 返回值：无

- 示例：<br>
舵机Servo1、Servo2在0和180度之间往回旋转。
```python
from microbit import *
import time
 
servo.init()
 
while True: 
    servo.angle(1,0)
    servo.angle(2,0)
    time.sleep_ms(1000)
    servo.angle(1,180)
    servo.angle(2,180)
    time.sleep_ms(1000)
```


### **RJ11模块**

## **项目示例**

