# 黑苹果 OpenCore配置 for ASUS TUF B550M-WIFI 3900X 6600xt

## 更新日志
- 21年11月18日 opencore 升级到 0.7.5 正式版  

## 硬件配置
- 主板：华硕 ASUS TUF B550M-WIFI
- CPU：AMD 3900X
- 显卡：蓝宝石 6600XT 超白金版
- 内存：美商海盗船(USCORSAIR)DDR4 3200 16GB [京东地址](https://item.jd.com/7706381.html)
- 硬盘：西部数据黑盘 SN750 500G
- 网卡：主板自带AX200

## BIOS设置（重要）
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
- 无线网卡：AX200

## 其他
- [OpenCore 实时编译地址](https://github.com/williambj1/OpenCore-Factory/releases)
- [Kexts 下载地址](https://gitee.com/evu/Easy-Kexts)
- [xjn 大佬的博客](https://blog.xjn819.com/?p=543)
- [主题资源文件 OcBinaryData](https://github.com/acidanthera/OcBinaryData)
- [ACPI定制USB端口](https://github.com/daliansky/OC-little/blob/master/15-ACPI%E5%AE%9A%E5%88%B6USB%E7%AB%AF%E5%8F%A3/README.md)
- [Intel无线网卡](
https://github.com/OpenIntelWireless/itlwm/releases)
- [AMD Vanilla OpenCore](https://github.com/AMD-OSX/AMD_Vanilla)

## AMD cpu 配置
- [资源地址](https://github.com/AMD-OSX/AMD_Vanilla)
 > 说明:不同的CPU根据修改内核参数就可以修改

## 无线网卡 AX 200
 > 引入AirportItlwm.kext 并配置 config->Kernel->Add

## 蓝牙 针对 Monterey 需要进行特殊配置
 > 1.确保IntelBluetoothFirmware.kext 最近版本
 > 2.引入IntelBluetoothInjector.kext 并配置 config->Kernel->Add
 > 3.引入BlueToolFixup.kext [地址](https://github.com/acidanthera/BrcmPatchRAM)
