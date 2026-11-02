# 墓界：房间陷落

Unity PICO XR 混合现实游戏的 Android 发布工程。游戏界面使用中文。Android 应用包名为 `com.shanzhasuan.gravehex.roomfall`。

## 构建

使用 JDK 17、Android SDK 36 与 Gradle Wrapper：

```bash
./gradlew :launcher:assembleRelease --no-daemon
```

预构建 ARM64 IL2CPP 库已包含在工程中。`buildIl2Cpp` 被禁用，云端构建不需要安装 Unity Editor；原生库校验清单见 `.vibelab-prebuilt.json`。

Unity 原工程版本为 6000.3.16f1，PICO XR SDK 为 6.1.1。部分原生库使用 4 KB LOAD 对齐，尚未验证16 KB页设备兼容性。

`assets/`、`.vibelab/`、签名密钥、缓存和机器配置保持本地，不作为源码提交。发布配置保存在 `vibelab.yaml`。
