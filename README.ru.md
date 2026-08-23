<div align="center">

# 🛡️ Kov-Sec — Защита Android APK от реверс-инжиниринга

### 🇷🇺 Русский

---

| 🏠 [Main / Principal](README.md) |

---

## 🌐 Website / Sitio web

### [👉 https://kov-sec.com](https://kov-sec.com)

---

## ✨ Introduction

**Kov-Sec** — профессиональная платформа защиты Android-приложений. Она преобразует байт-код вашего приложения во **внутреннюю виртуальную машину (VM)** и применяет несколько уровней защиты, делающих реверс-инжиниринг, взлом и модификацию чрезвычайно сложными.

---

## ✅ Google Play Store Compatibility

Ваше приложение остаётся **на 100% функциональным в Google Play Store** — полностью совместимо с требованиями Play Store, App Bundles (AAB) и распространением APK. Поддерживает APK и AAB, все схемы подписи (V1/V2/V3), Android 7.0+ (API 21+) и все архитектуры (arm64-v8a, armeabi-v7a, x86, x86_64).

---

## 🛡️ Core Features

### 🔐 Целостность VM
Критический код преобразуется во **внутренний байт-код VM** — злоумышленники не могут прочитать исходную логику.

### 🪝 Анти-хук
Блокирует FRIDA, Xposed, LSPosed, EdXposed, Zygisk, Substrate.

### 🐛 Анти-отладка
Обнаруживает gdb, lldb, отладчики Android Studio и ptrace.

### 📱 Анти-эмулятор
Обнаруживает BlueStacks, Nox, LDPlayer, MEmu, Genymotion.

### 👑 Обнаружение Root
Обнаруживает Magisk, KernelSU, APatch, SuSFS, Shamiko + продвинутое сканирование ядра.

### 🔑 Проверка подписи
Предотвращает перепаковку и атаки с поддельными подписями (V1+V2/V3).

### 🧪 Обнаружение DEX-инъекций
Обнаруживает DEX, загруженные извне APK во время выполнения.

### 🛡️ Защита ADB
Блокирует доступ через ADB.

### 📚 Обнаружение инъекций библиотек
Сканирует /proc/self/maps на предмет внедрённых библиотек.

### 🗑️ Удаление логов
Удаляет все вызовы Log.* из файлов DEX.

---

## ➕ Optional Protections

Блокировка экрана | Блокировка кейлоггера | Блокировка фейк-GPS | Блокировка VPN/прокси | SSL Pinning

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
