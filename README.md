# STM32F103C8T6 霍尔元件测速系统

## 项目描述

本项目基于STM32F103C8T6微控制器，结合霍尔元件、TT减速电机和0.96寸OLED屏幕，实现了一个直流电机转速测量与显示系统。程序通过霍尔元件的数字量输出测量直流电机的转速，并在0.96寸OLED屏幕上实时显示转速的波动曲线、电机报警阈值以及电机的实时转速。

由于STM32的带负载能力有限，无法直接驱动直流电机，因此本项目使用了L298Nmini电机驱动模块来驱动直流电机。通过两个GPIO口输出不同占空比的PWM波，实现对直流电机正反转转速的控制。

## 功能特点

- **转速测量**：通过霍尔元件的数字量输出，精确测量直流电机的转速。
- **OLED显示**：在0.96寸OLED屏幕上显示转速的波动曲线、电机报警阈值和实时转速。
- **电机驱动**：使用L298Nmini电机驱动模块，通过PWM波控制直流电机的正反转和转速。
- **按键控制**：通过四个独立按键实现以下功能：
  - 切换OLED数据显示界面和转速波动曲线界面。
    - 更改电机报警阈值。
      - 切换直流电机的正反转状态。
        - 调节直流电机的转速。

        ## 硬件需求

        - STM32F103C8T6微控制器
        - 霍尔元件
        - TT减速电机
        - 0.96寸OLED屏幕
        - L298Nmini电机驱动模块
        - 四个独立按键

        ## 软件需求

        - STM32 HAL库
        - 适用于STM32的开发环境（如Keil、STM32CubeIDE等）

        ## 使用说明

        1. **硬件连接**：
           - 将霍尔元件连接到STM32的GPIO引脚。
              - 将0.96寸OLED屏幕连接到STM32的I2C接口。
                 - 将L298Nmini电机驱动模块连接到STM32的GPIO引脚，并通过PWM控制电机转速。
                    - 将四个独立按键连接到STM32的GPIO引脚。

                    2. **软件配置**：
                       - 在开发环境中导入本项目的代码。
                          - 根据硬件连接配置STM32的GPIO和I2C接口。
                             - 编译并下载程序到STM32微控制器。

                             3. **操作说明**：
                                - 按下按键1切换OLED数据显示界面和转速波动曲线界面。
                                   - 按下按键2更改电机报警阈值。
                                      - 按下按键3切换直流电机的正反转状态。
                                         - 按下按键4调节直流电机的转速。

                                         ## 注意事项

                                         - 确保硬件连接正确，避免短路或接错线。
                                         - 在更改报警阈值时，注意不要设置过低或过高的值，以免影响系统正常运行。
                                         - 在调节电机转速时，注意观察电机的运行状态，避免电机过载或损坏。

                                         ## 贡献与反馈

                                         欢迎大家提出改进建议或提交代码优化，共同完善本项目。如果有任何问题或疑问，请在项目中提交Issue。

                                         ## 许可证

                                         本项目采用MIT许可证，详情请参阅LICENSE文件。

                                         ## 下载链接
                                         [STM32F103C8T6霍尔元件测速系统](https://pan.quark.cn/s/5897c27c275d) 

                                         (备用: [备用下载](https://pan.baidu.com/s/1KSWzJhGHqCY-BBqYAsijfw?pwd=1234))

                                         ## 说明

                                         该仓库仅用于学习交流，请勿用于商业用途。
