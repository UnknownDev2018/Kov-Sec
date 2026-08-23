<div align="center">

# 🛡️ Kov-Sec — 리버스 엔지니어링 방지 APK 보호

### 🇰🇷 한국어

---

| 🏠 [Main / Principal](README.md) |

---

## 🌐 Website / Sitio web

### [👉 https://kov-sec.com](https://kov-sec.com)

---

## ✨ Introduction

**Kov-Sec**은 전문가급 Android 앱 보호 플랫폼입니다. 앱의 바이트코드를 **내부 가상 머신 (VM)**으로 변환하고 리버스 엔지니어링, 변조, 해킹을 극도로 어렵게 만드는 여러 보호 계층을 적용합니다.

---

## ✅ Google Play Store Compatibility

앱은 **Google Play 스토어에서 100% 기능**을 유지합니다 — Play 스토어 요구사항, App Bundle (AAB), APK 배포와 완벽 호환. APK 및 AAB, 모든 서명 방식 (V1/V2/V3), Android 7.0+ (API 21+), 모든 아키텍처 (arm64-v8a, armeabi-v7a, x86, x86_64) 지원.

---

## 🛡️ Core Features

### 🔐 VM 무결성
중요 코드를 **내부 VM 바이트코드**로 변환 — 공격자가 원래 로직을 읽을 수 없습니다.

### 🪝 안티 후크
FRIDA, Xposed, LSPosed, EdXposed, Zygisk, Substrate 차단.

### 🐛 안티 디버그
gdb, lldb, Android Studio 디버거 및 ptrace 감지.

### 📱 안티 에뮬레이터
BlueStacks, Nox, LDPlayer, MEmu, Genymotion 감지.

### 👑 루트 감지
Magisk, KernelSU, APatch, SuSFS, Shamiko + 고급 커널 스캔.

### 🔑 서명 확인
재패키징 및 가짜 서명 공격 방지 (V1+V2/V3).

### 🧪 DEX 주입 감지
실행 중 APK 외부에서 로드된 DEX 감지.

### 🛡️ ADB 가드
ADB 셸 액세스 차단.

### 📚 라이브러리 주입 감지
/proc/self/maps 스캔으로 주입된 라이브러리 감지.

### 🗑️ 로그 제거
DEX 파일에서 모든 Log.* 호출 제거.

---

## ➕ Optional Protections

화면 공유 차단 | 키로거 차단 | 가짜 GPS 차단 | VPN/프록시 차단 | SSL 핀닝

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
