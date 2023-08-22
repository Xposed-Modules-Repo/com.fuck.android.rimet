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

    | 版本号 | 数据存储位置                                               |
    | ------ | ---------------------------------------------------------- |
    | 0.4    | /sdcard/Android/data/com.fuck.android.rimet/files/profiles |
    | 0.3.1  | /sdcard/Download/SmartisanProfile                          |
    | 0.3    | /sdcard/Download/SmartisonProfile                          |
    | 0.2    | /data/system/hammer_profiles                               |

    大版本号之间数据互不兼容且升级系统后数据可能也不兼容需重新创建环境快照


## 功能

- 已支持:

    支持快照GPS数据

    支持快照附近WIFI数据

    支持位置漂移功能

## 使用方法

1. 打开“锤锤”点击+号创建环境快照
2. 在”锤锤“列表中选择一个环境快照
3. 在模块管理器中激活模块并勾选推荐应用
4. **强行停止目标应用并重新打开**
5. **国内Android系统需开启锤锤自启动/关联唤醒之类的功能**

## 运行环境

* Android 8 - 14
* LSPosed（推荐）/LSPatch（不推荐）/太极（不推荐）

## 问题排查

1. 关闭其他模块仅保留锤锤模块开启

2. 确认模块是否生效，以LSPosed管理器为例打开管理器->选择“日志”标签->查看“模块日志”，检查日志是否包含以下内容

    ```
    LoadPackage: pkg=xxx proc=xxx ifa=xxx
    ```

3. 确认模块是否加载到环境快照数据，检查日志是否包含以下内容

    ```
    selected profile: {xxx}
    ```
    如日志都正常可加入[TG讨论组](https://t.me/+m2sDh0iN8y41MjM1)寻求帮助，提问时参考[提问的艺术](#提问的艺术)部分

## 提问的艺术

不欢迎无效的提问

&#10006; ~~我的锤锤为什么用不了？~~

欢迎这样的提问

```
手机型号：小米13 Ultra
MIUI版本：14.0.17
Android系统版本：13
钉钉版本：6.0.0
锤锤版本：0.4
框架类型：LSPosed/LSPatch/太极
问题描述：我已按照使用说明创建了环境快照，并且按照文档要求排查了问题，但是打开目标应用位置没有改变。
日志文件：
附上框架导出的日志文件
```

## FAQ

1. 为什么不支持手动选择位置？

    因为手动选择的位置不准，所以不支持。以后也不会支持！

2. 是否支持xx应用？

    自行测试理论上使用高德定位SDK的应用都支持。
    
3. 0.4版本偶尔失效

    从此版本开始更改了存储机制因此需唤醒锤锤读取环境快照数据，但是国内厂商在Android系统上做了一些省电的优化因此可能会导致功能失效，建议开启锤锤自启动/关联唤醒之类的功能。
