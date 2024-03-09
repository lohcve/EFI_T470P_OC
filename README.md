# EFI_T470P_OC
## T470P黑苹果EFI文件，OpenCore version 0.9.8，支持macOS 14.4 Sonoma
- 机型：Lenovo T470p 20J6A01ACD，CPU：Intel i7 7700HQ，核显：HD 630
- 加装了M.2 2242 SSD 512GB 建兴T11
- 加装了三星8G内存

## 感谢
```
https://github.com/ydongydong/T470P_OC
https://github.com/gxf9988776/efi_t470p_oc
```

## 2020-11-29更新
- 一切看起来正常，未彻底测试验证
- 内置无线网卡驱动正常，原生图标和管理方式

## 2022-1-20更新
- 绝大部分正常工作
- 升级OC 0.7.7
- 各种驱动最新
- 在线自动升级

## 2024-3-9更新

- 升级OC 0.9.8
- 删除不需要的kext
- 风扇转速显示支持
- 蓝牙功能修复
- HDMI输出支持修复
- 睡眠唤醒黑屏修复
- 各种驱动最新
- 在线自动升级
- 支持Sonoma 14.4

## 注意事项

### 关于Sonoma对旧机型的支持问题

由于Sonoma对旧机型，CPU的支持有问题，因此config.plist中添加了`Skip Board ID check<`补丁。

### 关于HDMI输出补丁问题

重新做了帧缓冲补丁，解决了HDMI输出问题，禁用独显时无法输出HDMI的问题，禁用独显时无法调节亮度问题。

### 关于SMBIOS的选择问题

经过反复测试，使用MacBookPro14,3机型，会存在禁用独显时无法输出HDMI的问题，如果不禁用独显，又会存在睡眠后唤醒黑屏的问题，因此机型改为MacBookPro14,1。

### 关于Sonoma使用itlwm无线网卡驱动问题

Sonoma下，AirportItlwm.kext无线网卡驱动存在一些问题，因此改为使用itlwm.kext，需要配合HeliPort使用，并自行将HeliPort设置为开机自启。使用itlwm.kext可以解决iMessage无法使用的问题，不在意的话可以改为使用AirportItlwm.kext（不需要HeliPort）。

### 关于Sonoma自动更新问题

本次更新已修复，Sonoma可自动检查和安装更新，详情自行搜索相关文章。



