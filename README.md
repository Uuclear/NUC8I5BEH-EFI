# NUC8I5BEH EFI macOS Mojave

## 更新

### 2019-12-24

    1. 解决休眠秒醒，并且蓝牙不可用的问题（解决方案是：使用 hackintool 禁用板载蓝牙的USB口 HS10 ）

## 硬件配置

| 硬件          | 型号                | 备注                                 |
| ------------- | ------------------- | ------------------------------------ |
| 主机型号      | NUC8I5BEH           |                                      |
| BIOS 版本     | 75                  |                                      |
| 网卡          | 博通 BCM94360CS2    | 转 M.2                               |
| 内存          | 协德 DDR4 2666 16G  | 虽然内存是 2666 德，但只支持 2400    |
| 硬盘          | 东芝 TR200 480G     | SATA 接口，不能开启 TRIM             |
| 显示器 HDMI   | HKC T7000 2K        | 老显示器，接 HDMI 口                 |
| 显示器 USBC-C | 15.6 便携显示器     | 供电和信号都使用 USB-C（简称一线通） |
| 键盘          | Filco Minila air 67 | BT3.0                                |
| 鼠标          | 罗技 Logitech M720  | BT4.0 + USB                          |

## BIOS 设置

1. 禁用内置的蓝牙/WIFI
2. 禁用 Secure Boot
3. 禁用 Legacy Boot
4. 禁用 LAN / WIFI Boot

## Clover Version

Clover r5707

## 支持特性

1. 兼容至 10.14.6
2. 支持 WIFI 和 蓝牙 (BCM94360CS2 转 M.2)
3. 支持 USBC + HDMI 双显示器 (可以随意切换，插拔)
4. 支持 DP HDMI 声音输出
5. USB 正常
6. 声卡驱动正常
7. CPU 变频支持
8. 休眠唤醒正常

## 已知问题

1.  开机有几率卡在进度条，暂时未知
2.  读卡器

    基本不用读卡器，所以也没有刻意去修复，试了 Switch 的 TF 卡，的确用不了

3.  无法使用蓝牙设备唤醒 NUC，只能按电源键或者 USB 设备唤醒

## 补充说明

感谢：[csrutil](https://github.com/csrutil/NUC8I5BEH) 提供 EFI，本 EFI 基于他的版本上修改的。

1. 序列号：请自行更改序列号，可以直接使用 Clover Configurator 生成
2. 其他型号支持：NUC8I7 除了 CPU 以外，其他都一样，所以应该也是能用的
3. Catalina: 10.15 已经测试了无法引导
4. 雷电 3 热插拔未知：我的 TYPE-C 显示器走的是 DP 协议，并不是雷电协议，很多人反应雷电接口不支持热插拔，因为我没有雷电设备，所以目前无法知道是否支持热插拔
