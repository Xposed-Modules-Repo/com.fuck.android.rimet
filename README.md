<div align="center">

# 锤锤 Smartison

钉钉的好朋友，支持模拟位置！

[![Stars](https://img.shields.io/github/stars/Xposed-Modules-Repo/com.fuck.android.rimet?label=stars)](https://github.com/Xposed-Modules-Repo/com.fuck.android.rimet)
[![Release](https://img.shields.io/github/v/release/Xposed-Modules-Repo/com.fuck.android.rimet?include_prereleases)](https://github.com/Xposed-Modules-Repo/com.fuck.android.rimet/releases/latest)
[![Download](https://img.shields.io/github/downloads/Xposed-Modules-Repo/com.fuck.android.rimet/total)](https://github.com/Xposed-Modules-Repo/com.fuck.android.rimet/releases)
[![Telegram](https://img.shields.io/badge/%E9%94%A4%E9%94%A4-10000+%20users-green?logo=telegram)](https://t.me/+m2sDh0iN8y41MjM1)

</div>

## 注意事项

- 环境采集数据存储路径
    0.3版本 ```/sdcard/Download/SmartisonProfile```
    0.2版本 ```/data/system/hammer_profiles```

- 各版本间数据互不兼容需重新采集


## 功能

- 已支持:
    支持Android 8-13
    支持root类框架如LSPosed/太极阳（其他框架自行测试）
    支持rootless类框架如LSPatch/太极阴（其他框架自行测试）
    支持模拟GPS+WIFI定位

- 待支持:
    模拟蓝牙设备定位

## 使用方法

1. 在对应的模块管理器中激活模块

2. 打开“锤锤”点击+号采集环境数据

3. 在”锤锤“列表中选择一个模拟位置

4. 打开目标应用的文件访问权限 **（重要）**

5. 强制停止目标应用 **（重要）**

## 问题排查

1. 模块是否生效？

    检查模块日志输出是否包含以下内容
    ```
    Smartison handleLoadPackage:com.fuck.android.rimet
    ```
    包含跳转至[问题排查-2](#问题排查)，不包含请自行确认模块是否正确激活
    
2. 允许宿主应用访问环境数据？

    检查模块日志输出是否包含以下内容
    ```
    [ERROR] The host application external storage permission not grant.
    ```
    包含请参考[使用方法4-5](#使用方法)，不包含跳转至[问题排查-2](#问题排查)

3. 环境数据是否加载成功？

    检查模块日志输出是否包含以下内容
    ```
    [WORKING] current profile:{xxx}
    ```
    包含则在锤锤列表中确认采集并应用了相关环境信息，如仍不成功加入[TG讨论组](https://t.me/+m2sDh0iN8y41MjM1)反馈bug。



## 完全卸载

卸载模块后删除对应的数据目录