# 黑苹果 OpenCore 配置 for ASUS TUF B550M-WIFI 5600X RX560D

| 更新版本 | 更新时间 | 更新内容       |
| -------- | -------- | -------------- |
| OC0.8.1  | 20220613 | 0.8.0->0.8.1   |
| OC0.8.0  | 20220505 | 0.7.9->0.8.0   |
| OC0.7.7  | 20220118 | 0.7.6 -> 0.7.7 |

![image-20220505191053866](https://cdn.jsdelivr.net/gh/edge-iris/oss@oss/image/png/2022/06/13/20/152716551225271655122527256bSNoa9/2022-06-13_20-15-02.png)

## 硬件配置

- 主板：华硕 ASUS TUF B550M-WIFI
- CPU：AMD 5600X
- 显卡：RX560D
- 内存：美商海盗船(USCORSAIR)DDR4 3600 16GB
- 硬盘：三星 980Pro NVMe PCIe4.0 500G
- 网卡：主板自带 AX201

## BIOS 设置（重要）

#### disable 禁用

- Fast Boot(快速启动)
- CSM(兼容性支持模块)

#### enable 开启

- Above 4G decoding(大于 4G 地址空间解码)
- EHCI/XHCI Hand-off(接手 EHCI/XHCI 控制)
- OS type: other types(操作系统类型: 其他)

## 软件说明

- 操作系统版本：macOS Monterey 12.1(beta2)
- OpenCore 版本：0.7.5(正式版)
- 无线网卡：英特尔 ® Wi-Fi 6 AX200

## 其他

- [OpenCore 实时编译地址](https://github.com/williambj1/OpenCore-Factory/releases)
- [Kexts 下载地址](https://gitee.com/evu/Easy-Kexts)
- [xjn 大佬的博客](https://blog.xjn819.com/?p=543)
- [主题资源文件 OcBinaryData](https://github.com/acidanthera/OcBinaryData)
- [ACPI 定制 USB 端口](https://github.com/daliansky/OC-little/blob/master/15-ACPI%E5%AE%9A%E5%88%B6USB%E7%AB%AF%E5%8F%A3/README.md)
- [Intel 无线网卡](https://github.com/OpenIntelWireless/itlwm/releases)
- [AMD Vanilla OpenCore](https://github.com/AMD-OSX/AMD_Vanilla)

## AMD cpu 配置

- [资源地址](https://github.com/AMD-OSX/AMD_Vanilla)

> 说明:不同的 CPU 根据修改内核参数就可以修改

> 项目根目录有 5800x 配置的 config.plist 文件

## 英特尔 ® Wi-Fi 6 AX200

> 引入 AirportItlwm.kext 并配置 config->Kernel->Add

## 蓝牙 针对 Monterey 需要进行特殊配置

- 1.确保 IntelBluetoothFirmware.kext 最近版本
- 2.删除 IntelBluetoothInjector.kext 并移除 config->Kernel->Add->IntelBluetoothInjector.kext
- 3.引入 BlueToolFixup.kext [地址](https://github.com/acidanthera/BrcmPatchRAM)

![2021-07-22_21-22-13](https://yiqibangface.oss-cn-shenzhen.aliyuncs.com/apanda/uPic/2021-07-22_21-22-13.png)
