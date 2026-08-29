# Kov-Sec — リバースエンジニアリング対策 APK 保護

**Website:** https://kov-sec.com | **[メイン](README.md)**

## 日本語

Kov-Sec はプロ仕様の Android アプリ保護プラットフォームです。アプリのバイトコードを内部仮想マシン (VM) に変換し、リバースエンジニアリング、改ざん、ハッキングを極めて困難にする複数の保護レイヤーを適用します。アプリは Google Play ストアで100%機能したまま — Play ストアの要件、App Bundle (AAB)、APK 配布に完全対応。APK と AAB、すべての署名方式 (V1/V2/V3)、Android 7.0+ (API 21+)、すべてのアーキテクチャをサポート。

## 保護オプション

### 1) アンチフック

**保護するもの:** Detects and blocks hooking frameworks that try to modify your app's behavior.

**対象:** Frida, Xposed, LSPosed, EdXposed, Zygisk, Substrate, Cydia.

**動作:** Scans the running process for any sign of hooking. If something suspicious is detected, it stops the app.

### 2) アンチデバッグ

**保護するもの:** Prevents dynamic debugging of the app.

**対象:** gdb, lldb, Android Studio debugger, ptrace.

**動作:** Detects debug flag (). Detects ptrace. Kills the app if a debugger is found.

### 3) アンチエミュレータ

**保護するもの:** Detects that the app is NOT running on an emulator.

**対象:** BlueStacks, Nox, LDPlayer, MEmu, Genymotion.

**動作:** Detects emulator properties, files (), fake sensors. Kills the app if detected.

### 4) ルート検出

**保護するもの:** Detects devices with root (superuser) permissions.

**対象:** Magisk, KernelSU, APatch, SuSFS, Shamiko.

**動作:** Searches for su, , magisk. Detects mounts, , s. Kills the app if root.

### 5) VM完全性

**保護するもの:** Protects the virtual machine (VM) that interprets your protected code.

**対象:** Code modification, VM modification, hooks that redirect VM functions.

**動作:** Converts code to VM bytecode. Verifies with checksums. Kills the app if patched.

### 6) 署名チェック

**保護するもの:** Verifies the APK signature against repackaging.

**対象:** Repackaging with a fake key, malware pretending to be your app.

**動作:** Calculates the V1+V2/V3 signature hash and compares it with the expected signature. Stops the app if mismatched.

### 7) DEX注入検出

**保護するもの:** Detects DEX loaded that don't come from the APK.

**対象:** Dex injection at runtime, malicious classes loaded on the fly.

**動作:** Lists ClassLoaders and DexFiles. Compares against legitimate dex. Kills the app if extra DEX.

### 8) ADBガード

**保護するもの:** Blocks ADB shell access on the device.

**対象:** ADB to view logs, extract files, inject commands.

**動作:** Detects if ADB is enabled or USB debugging is connected. Kills the app if active.

### 9) ライブラリ注入検出

**保護するもの:** Detects libraries injected into the process.

**対象:** , ptrace inject, hooking libraries, malware.

**動作:** Scans /self/maps. Verifies all .so come from the app. Kills the app if strange.

### 10) ログ削除

**保護するもの:** Removes all Log.* calls from the DEX files.

**対象:** Hackers reading logs, malware reading logs, easier debugging.

**動作:** Removes Log.v/d/i/w/e calls. Reduces size. Removes attacker info.

## オプション保護

### 11) スクリーン共有ブロック

スクリーン共有ブロック — 画面録画と共有を防止. キャプチャを検出. オプション.

### 12) キーロガーブロック

キーロガーブロック — キーロガーと入力キャプチャをブロック. オーバーレイを検出. オプション.

### 13) 偽GPSブロック

偽GPSブロック — GPSなりすましを防止. モックロケーションを検出. オプション.

### 14) VPN / プロキシブロック

VPN / プロキシブロック — VPN と MITM プロキシを検出. tun0/wg0 を検出. オプション.

### 15) SSLピンニング

SSLピンニング — MITM 防止のため証明書をピン留め. オプション.

## クイックサマリー

VM Integrity, Signature Check, Lib Injection, Remove Logs — always recommended. Anti-Hook, Anti-Debug, Anti-Emulator, Root Detection, DEX Injection, ADB Guard — anti-fraud. Screen Share, Keylogger, Fake GPS, VPN/Proxy, SSL Pinning — optional.

---

© Kov-Sec. All rights reserved. https://kov-sec.com
<!-- Last update: 2026-08-29 23:15 UTC -->
