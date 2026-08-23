<div align="center">

# 🛡️ Kov-Sec — 反逆向工程 APK 保护

### 🇨🇳 中文

---

| 🏠 [Main / Principal](README.md) |

---

## 🌐 Website / Sitio web

### [👉 https://kov-sec.com](https://kov-sec.com)

---

## ✨ Introduction

**Kov-Sec** 是一个专业的 Android 应用保护平台。它将应用程序的字节码转换为**内部虚拟机 (VM)**，并应用多层加固，使逆向工程、篡改和黑客攻击变得极其困难。

---

## ✅ Google Play Store Compatibility

您的应用在**Google Play Store 上保持 100% 功能** — 完全兼容 Play Store 要求、App Bundle (AAB) 和 APK 分发。支持 APK 和 AAB、所有签名方案 (V1/V2/V3)、Android 7.0+ (API 21+) 以及所有架构 (arm64-v8a, armeabi-v7a, x86, x86_64)。

---

## 🛡️ Core Features

### 🔐 VM 完整性
关键代码转换为**内部 VM 字节码** — 攻击者无法读取原始逻辑。

### 🪝 反 Hook
阻止 FRIDA、Xposed、LSPosed、EdXposed、Zygisk、Substrate。

### 🐛 反调试
检测 gdb、lldb、Android Studio 调试器和 ptrace。

### 📱 反模拟器
检测 BlueStacks、Nox、LDPlayer、MEmu、Genymotion。

### 👑 Root 检测
检测 Magisk、KernelSU、APatch、SuSFS、Shamiko + 高级内核扫描。

### 🔑 签名验证
防止重新打包和伪造签名攻击 (V1+V2/V3)。

### 🧪 DEX 注入检测
检测运行时从 APK 外部加载的 DEX。

### 🛡️ ADB 防护
阻止 ADB shell 访问。

### 📚 库注入检测
扫描 /proc/self/maps 检测注入的库。

### 🗑️ 移除日志
从 DEX 文件中清除所有 Log.* 调用。

---

## ➕ Optional Protections

屏幕共享阻止 | 键盘记录器阻止 | 虚拟 GPS 阻止 | VPN/代理阻止 | SSL 固定

---

## 📊 Supported Platforms

| Format | Users | | Architecture | Support |
|---|---|---|---|---|
| **APK** | ✅ All | | **arm64-v8a** | ✅ |
| **AAB** | 👑 VIP | | **armeabi-v7a** | ✅ |
| | | | **x86** | ✅ |
| | | | **x86_64** | ✅ |

---

## 🚀 How It Works

```
1. 📤 Upload your APK or AAB
2. ⚙️ Select protection options
3. 🔄 Kov-Sec converts your code to VM bytecode
4. 🛡️ Protection layers are applied
5. 📥 Download your protected app
```

---

## 📄 License

© Kov-Sec. All rights reserved.

[**https://kov-sec.com**](https://kov-sec.com)

</div>
