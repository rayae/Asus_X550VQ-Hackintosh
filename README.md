# 华硕 X550VQ 黑苹果EFI
Hackintosh for Asus X550VQ (HM170)

### 兼容性

此 EFI 适用于华硕 X550VQ，且只在该平台测试使用。

### 笔记本配置

| 规格     | 详细信息                                                |
| -------- | ----------------------------------------------------- |
| 电脑型号 | Asus X550VQ(HM170)                                  |
| 操作系统 | macOS Catalina 10.15.4                                 |
| 处理器   | Intel Core i5-6300HQ, 2.9 GHz, 4 核心                  |
| 内存     | 8 GB 2400 MHz DDR4                        |
| 硬盘     | GALAX KA1D0128A  (119 GB)                     |
| 显卡     | Intel HD Graphics 530 2048 MB    |
| 网卡     | 已更换 DW1510/BMC4322                     |
| 声卡     | Realtek ALC255                                |
|SMBIOS | MacBookPro13,3     |


### 正常工作的功能

- CPU 睿频、变频
- 核显
- 亮度调节
- 有线网卡
- 无线网卡
- 声卡
- 原生电源管理
- 电池状态
- USB 3.0x2 USB 2.0x1
- 睡眠唤醒
- Fn 快捷键
- 触摸板
- 读卡器
- 摄像头
- Facetime/iMessage 等白苹果功能 (自行注入五码进行洗白)

### DW1510/BMC4322

某宝18元包邮，仅支持 2.4Ghz/5Ghz 300 Mbps，无蓝牙功能，实测速度在 230 Mbps 左右，一分钱一分货。

10.15 需要安装 10.14 的 `IO80211Family.kext` 到 SLE：
```bash
sudo mount -uw / && killall Finder
sudo rm -r /System/Library/Extensions/IO80211Family.kext
sudo cp -r /path/to/your/EFI/CLOVER/kexts/10.15/IO80211Family.kext /System/Library/Extensions/
sudo kextcache -i /
sudo reboot
```

### 未测试的功能

- HDMI 无显示器无法测试

### 无法使用

- nVIDIA GeForce 940MX 独立显卡 (没有任何解决方案)
- 蓝牙

### 截图一览

![desktop.jpg](https://github.com/bavelee/Asus_X550VQ-Hackintosh/raw/master/Screenshots/desktop.jpg)

![usb.jpg](https://github.com/bavelee/Asus_X550VQ-Hackintosh/raw/master/Screenshots/usb.jpg)

![facetime.jpg](https://github.com/bavelee/Asus_X550VQ-Hackintosh/raw/master/Screenshots/facetime.jpg)

![wifi.jpg](https://github.com/bavelee/Asus_X550VQ-Hackintosh/raw/master/Screenshots/wifi.jpg)

![speedtest.jpg](https://github.com/bavelee/Asus_X550VQ-Hackintosh/raw/master/Screenshots/speedtest.jpg)

# 如果我的辛勤工作对您有所帮助的话，感谢您的捐赠鼓励

![alipay.png](https://github.com/bavelee/Asus_X550VQ-Hackintosh/raw/master/Screenshots/alipay_250x250.png)

![wechat.png](https://github.com/bavelee/Asus_X550VQ-Hackintosh/raw/master/Screenshots/wechat_250x250.png)

