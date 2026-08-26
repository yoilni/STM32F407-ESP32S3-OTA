# STM32 APP A v1.0.1

- 目标芯片：STM32F407ZGT6
- APP 起始地址：0x08020000
- 文件：OTA_Application_A.bin
- 大小：22,340 字节
- CRC32：14D2CAD2
- 初始 MSP：0x20020000
- 复位向量：0x080246B1
- 变化：按实际电路将 PC13 高电平定义为 LED 点亮，并改为 500 ms 非阻塞翻转；OLED 显示 APP A V1.0.1 和 LED:HIGH BLINK。
