# ThinkPad-X13-EFI

## 配置清单

- Machine: ThinkPad X13 Gen1 20T3
- OS: macOS 12.3.1 Monterey
- OpenCore: 0.7.5
- CPU Cooler: Intel® Core™ i5-10210U
- Wi-Fi Card: Intel® AX201
- Sound Card: Realtek ALC257
 
## 2022-08-02

- [ ] 笔记本内屏不亮，bios 关闭内建显示器，使用外接HDMI显示点亮
- [ ] 声卡未驱动


## 2022-08-04

- [x] 点亮笔记本内屏
- [x] 声卡未驱动

> NVRAM 7C436110-AB2A-4BBB-A880-FE41995C9F82  Delete boot-args 禁用nvram缓存

```
boot-args debug=0x100 keepsyms=1 igfxonln=1 igfxrpsc=1 igfxfw=2  alcid=11

igfxfw=2引导参数（和igfxfw属性）强制加载 Apple GuC 固件
igfxonln=1引导参数（force-online设备属性）强制所有显示器上的在线状态。
igfxrpsc=1启动参数（rps-control属性）以启用 RPS 控制补丁（提高 IGPU 性能）。
``` 

## 资源链接

- [occ](https://mackie100projects.altervista.org/occ-changelog-version-2-52-0-1/)
- [hackintool](https://github.com/headkaze/Hackintool/releases)
- [故障排错](https://apple.sqlsec.com/10-%E6%8E%92%E9%94%99/)
- [核显驱动](https://billy233.github.io/post/WhateverGreen) 
- [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools/releases) 

## 感谢

- [shuai132](https://github.com/shuai132)

