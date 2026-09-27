# 神码再现 v3.7.10 Android App

## 项目结构

```
ShenMaApp/
├── build.gradle
├── settings.gradle
├── gradle.properties
├── gradle/wrapper/gradle-wrapper.properties
└── app/
    ├── build.gradle
    ├── proguard-rules.pro
    └── src/main/
        ├── AndroidManifest.xml
        ├── assets/index.html          <-- v3.7.10 已内置
        ├── java/com/xinghuishama/shenma/MainActivity.java
        └── res/
            ├── layout/activity_main.xml
            ├── values/strings.xml
            ├── values/themes.xml
            └── xml/network_security_config.xml
```

## 构建说明

推送 main 分支后，GitHub Actions 自动构建 release 版 APK，
使用仓库 Secrets 中的密钥签名（apksigner + zipalign），
产物在 Actions 运行记录的 Artifacts 中下载：`ShenmaAPP-v3.7.10-release`。

签名密钥只存在于仓库 Secrets 中，请妥善保管本地加密备份（如有）。

## 功能特点

- 内置 v3.7.10 HTML，无需网络即可打开
- 全屏沉浸，隐藏状态栏/导航栏
- 硬件加速，粒子特效流畅
- 下拉刷新原生支持
- LocalStorage 数据持久化
