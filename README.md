# STM32F407 + ESP32-S3 公网 OTA 固件仓库

本仓库用于托管 ESP32-S3 为 STM32F407ZGT6 下载和转发的公开固件。

- `manifest.json`：当前可用版本、目标芯片、大小、CRC32 和固件 URL；
- `firmware/vX.Y.Z/`：不可覆盖的历史版本固件；
- ESP32 通过 HTTPS 获取清单和 BIN，完成下载 CRC32 与 Flash 读回 CRC32 校验后，再经 UART 写入 STM32；
- STM32 返回升级成功后，ESP32 才在 NVS 中记录已安装版本。

当前通信链路：GitHub HTTPS → ESP32-S3 → UART → STM32F407ZGT6。CAN 传输将在收发器到位后继续联调。

> CRC32 用于发现传输错误，不等同于数字签名。正式部署应增加固件签名验证。
