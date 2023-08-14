<div align="center">

# 锤锤 Smartisan

钉钉的好朋友，支持模拟位置！

[![Stars](https://img.shields.io/github/stars/Xposed-Modules-Repo/com.fuck.android.rimet?label=stars)](https://github.com/Xposed-Modules-Repo/com.fuck.android.rimet)
[![Release](https://img.shields.io/github/v/release/Xposed-Modules-Repo/com.fuck.android.rimet?include_prereleases)](https://github.com/Xposed-Modules-Repo/com.fuck.android.rimet/releases/latest)
[![Download](https://img.shields.io/github/downloads/Xposed-Modules-Repo/com.fuck.android.rimet/total)](https://github.com/Xposed-Modules-Repo/com.fuck.android.rimet/releases)
[![Telegram](https://img.shields.io/badge/%E9%94%A4%E9%94%A4-2k+%20users-green?logo=telegram)](https://t.me/+m2sDh0iN8y41MjM1)

</div>

## 注意事项

- 数据默认存储路径

    | 版本号 | 数据存储位置                                                 |
    | ------ | ------------------------------------------------------------ |
    | 0.4    | /sdcard/Android/data/com.fuck.android.rimet/files/SmartisanProfile |
    | 0.3.1  | /sdcard/Download/SmartisanProfile                            |
    | 0.3    | /sdcard/Download/SmartisonProfile                            |
    | 0.2    | /data/system/hammer_profiles                                 |

- 大版本号之间数据互不兼容，且升级系统后数据可能也不兼容需重新收集


## 功能

- 已支持:

    支持Android 8 - 13

    支持LSPosed/LSPatch

    支持模拟GPS+WIFI定位

    模拟附近随机位置

- 待支持:

    模拟蓝牙设备定位
    
    模拟虚拟相机
    

## 使用方法

1. 打开“锤锤”点击+号收集环境数据
2. 在”锤锤“列表中选择一个模拟位置
3. 在模块管理器中激活模块并勾选推荐应用
4. **强行停止目标应用并重新打开**

## 问题排查

1. 关闭其他模块仅保留锤锤模块开启

2. 检查模块是否生效，以LSPosed管理器为例打开管理器->选择“日志”标签->查看“模块日志”，检查日志是否包含以下内容

    ```
    LoadPackage: pkg=xxx proc=xxx ifa=xxx
    ```

3. 检查模块是否读取到收集到的数据，检查日志是否包含以下内容

    ```
    selected profile: {xxx}
    ```
    如日志都正常可加入[TG讨论组](https://t.me/+m2sDh0iN8y41MjM1)寻求帮助，提问时参考[提问的艺术](#提问的艺术)部分

## 提问的艺术

不欢迎无效的提问

&#10006; ~~我的锤锤为什么用不了！~~

欢迎这样的提问

```
手机型号：小米13 Ultra
MIUI版本：13
Android系统版本：13
使用的框架：LSPosed/LSPatch/太极
问题描述：我已按照使用说明采集了位置信息，并且按照问题排查部分排查了问题，但是打开目标应用位置没有改变。
附上日志文件
```

## FAQ

1. 为什么不支持手动选择位置？

    因为手动选择的位置不准，所以不支持。以后也不会支持！

1. 是否支持xx应用？

    自行测试，理论上来讲使用了高德定位的都支持。
