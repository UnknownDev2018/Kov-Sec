# Kov-Sec — 리버스 엔지니어링 방지 APK 보호

**Website:** https://kov-sec.com | **[메인](README.md)**

## 한국어

Kov-Sec은 전문가급 Android 앱 보호 플랫폼입니다. 앱의 바이트코드를 내부 가상 머신 (VM)으로 변환하고 리버스 엔지니어링, 변조, 해킹을 극도로 어렵게 만드는 여러 보호 계층을 적용합니다. 앱은 Google Play 스토어에서 100% 기능을 유지합니다 — Play 스토어 요구사항, App Bundle (AAB), APK 배포와 완벽 호환. APK 및 AAB, 모든 서명 방식 (V1/V2/V3), Android 7.0+ (API 21+), 모든 아키텍처 지원.

## 보호 옵션

### 1) 안티 후크

**보호 내용:** Detects and blocks hooking frameworks that try to modify your app's behavior.

**대상:** Frida, Xposed, LSPosed, EdXposed, Zygisk, Substrate, Cydia.

**동작:** Scans the running process for any sign of hooking. If something suspicious is detected, it stops the app.

### 2) 안티 디버그

**보호 내용:** Prevents dynamic debugging of the app.

**대상:** gdb, lldb, Android Studio debugger, ptrace.

**동작:** Detects debug flag (). Detects ptrace. Kills the app if a debugger is found.

### 3) 안티 에뮬레이터

**보호 내용:** Detects that the app is NOT running on an emulator.

**대상:** BlueStacks, Nox, LDPlayer, MEmu, Genymotion.

**동작:** Detects emulator properties, files (), fake sensors. Kills the app if detected.

### 4) 루트 감지

**보호 내용:** Detects devices with root (superuser) permissions.

**대상:** Magisk, KernelSU, APatch, SuSFS, Shamiko.

**동작:** Searches for su, , magisk. Detects mounts, , s. Kills the app if root.

### 5) VM 무결성

**보호 내용:** Protects the virtual machine (VM) that interprets your protected code.

**대상:** Code modification, VM modification, hooks that redirect VM functions.

**동작:** Converts code to VM bytecode. Verifies with checksums. Kills the app if patched.

### 6) 서명 확인

**보호 내용:** Verifies the APK signature against repackaging.

**대상:** Repackaging with a fake key, malware pretending to be your app.

**동작:** Calculates the V1+V2/V3 signature hash and compares it with the expected signature. Stops the app if mismatched.

### 7) DEX 주입 감지

**보호 내용:** Detects DEX loaded that don't come from the APK.

**대상:** Dex injection at runtime, malicious classes loaded on the fly.

**동작:** Lists ClassLoaders and DexFiles. Compares against legitimate dex. Kills the app if extra DEX.

### 8) ADB 가드

**보호 내용:** Blocks ADB shell access on the device.

**대상:** ADB to view logs, extract files, inject commands.

**동작:** Detects if ADB is enabled or USB debugging is connected. Kills the app if active.

### 9) 라이브러리 주입 감지

**보호 내용:** Detects libraries injected into the process.

**대상:** , ptrace inject, hooking libraries, malware.

**동작:** Scans /self/maps. Verifies all .so come from the app. Kills the app if strange.

### 10) 로그 제거

**보호 내용:** Removes all Log.* calls from the DEX files.

**대상:** Hackers reading logs, malware reading logs, easier debugging.

**동작:** Removes Log.v/d/i/w/e calls. Reduces size. Removes attacker info.

## 선택 보호

### 11) 화면 공유 차단

화면 공유 차단 — 화면 녹화 및 공유 방지. 캡처 감지. 선택.

### 12) 키로거 차단

키로거 차단 — 키로거 및 입력 캡처 차단. 오버레이 감지. 선택.

### 13) 가짜 GPS 차단

가짜 GPS 차단 — GPS 스푸핑 방지. 모의 위치 감지. 선택.

### 14) VPN / 프록시 차단

VPN / 프록시 차단 — VPN 및 MITM 프록시 감지. tun0/wg0 감지. 선택.

### 15) SSL 핀닝

SSL 핀닝 — MITM 방지를 위해 인증서 고정. 선택.

## 빠른 요약

VM Integrity, Signature Check, Lib Injection, Remove Logs — always recommended. Anti-Hook, Anti-Debug, Anti-Emulator, Root Detection, DEX Injection, ADB Guard — anti-fraud. Screen Share, Keylogger, Fake GPS, VPN/Proxy, SSL Pinning — optional.

---

© Kov-Sec. All rights reserved. https://kov-sec.com
<!-- Last update: 2026-08-31 08:30 UTC -->
