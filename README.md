<div align="center">

# 锤锤 Smartisan

钉钉的好朋友，支持模拟位置！

[![Stars](https://img.shields.io/github/stars/Xposed-Modules-Repo/com.fuck.android.rimet?label=stars)](https://github.com/Xposed-Modules-Repo/com.fuck.android.rimet)
[![Release](https://img.shields.io/github/v/release/Xposed-Modules-Repo/com.fuck.android.rimet?include_prereleases)](https://github.com/Xposed-Modules-Repo/com.fuck.android.rimet/releases/latest)
[![Download](https://img.shields.io/github/downloads/Xposed-Modules-Repo/com.fuck.android.rimet/total)](https://github.com/Xposed-Modules-Repo/com.fuck.android.rimet/releases)
[![Telegram](https://img.shields.io/badge/%E9%94%A4%E9%94%A4-10000+%20users-green?logo=telegram)](https://t.me/+m2sDh0iN8y41MjM1)

</div>

## 注意事项

- 环境采集数据默认存储路径

    | 版本号 | 数据存储位置                      |
    | ------ | --------------------------------- |
    | 0.3.1  | /sdcard/Download/SmartisanProfile |
    | 0.3    | /sdcard/Download/SmartisonProfile |
    | 0.2    | /data/system/hammer_profiles      |

- 大版本号之间数据互不兼容

- 不支持选择位置只能采集当前位置


## 功能

- 已支持:

    支持Android 8 - 13

    支持root/rootless框架如LSPosed/LSPatch等

    支持模拟GPS+WIFI定位

- 待支持:

    模拟蓝牙设备定位
    
    模拟虚拟相机
    
    模拟附近随机位置

## 使用方法

1. 打开“锤锤”点击+号采集环境数据

2. 在”锤锤“列表中选择一个模拟位置

3. 在模块管理器中激活模块

4. **打开目标应用文件访问权限**（关闭了存储隔离等类似工具）

5. **强制停止目标应用并重新打开**

## 问题排查

1. 模块是否生效？

    检查模块日志输出是否包含以下内容
    ```
    Smartisan handleLoadPackage:com.fuck.android.rimet
    ```
    包含跳转至[问题排查-2](#问题排查)，不包含请自行确认模块是否正确激活

2. 允许目标应用访问文件权限？

    检查模块日志输出是否包含以下内容
    ```
    [ERROR] The host application external storage permission not grant.
    ```
    包含请参考[使用方法4-5](#使用方法)，不包含跳转至[问题排查-3](#问题排查)

3. 环境数据是否加载成功？

    检查模块日志输出是否包含以下内容
    ```
    [WORKING] current profile:{xxx}
    ```
    包含则在锤锤列表中确认采集并应用了相关环境信息，如过还不成功加入[TG讨论组](https://t.me/+m2sDh0iN8y41MjM1)寻求帮助。

### FAQ

1. 为什么不支持手动选择位置？

    因为手动选择的位置不准，所以不支持！
    
2. 为什么xx应用打开文件访问也不行？

    使用国内版本。

## 完全卸载

卸载模块后删除对应的数据目录