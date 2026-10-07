<div align="center">

<a href="https://vazovsky.pro"><img src="assets/header.svg" alt="Vazovsky — Android developer and product builder." width="100%"></a>

<br>

<a href="https://vazovsky.pro"><img src="https://img.shields.io/badge/vazovsky.pro-website-4CB0FF?style=for-the-badge&labelColor=04070F&logo=safari&logoColor=4CB0FF" alt="Website vazovsky.pro"></a>
<a href="https://t.me/vazovsky17"><img src="https://img.shields.io/badge/Telegram-@vazovsky17-04070F?style=for-the-badge&logo=telegram&logoColor=4CB0FF" alt="Telegram @vazovsky17"></a>
<a href="mailto:vazovsky.hub@gmail.com"><img src="https://img.shields.io/badge/Email-04070F?style=for-the-badge&logo=gmail&logoColor=8B66FF" alt="Email vazovsky.hub@gmail.com"></a>
<a href="https://www.behance.net/vazovsky17"><img src="https://img.shields.io/badge/Behance-04070F?style=for-the-badge&logo=behance&logoColor=4477FF" alt="Behance vazovsky17"></a>

<br><br>

**I write Kotlin, Jetpack Compose and Android SDK.**<br>
Not just the app interface, but also the backend, infrastructure, release and publishing.<br>
I build my own products.

<br>

**[More about my projects at vazovsky.pro →](https://vazovsky.pro)**

</div>

<br>

`MAIN PROJECT · OWN PRODUCT`

## [Vazie](https://vazie.app) — a local-first app ecosystem

Vazie is my own product: a small ecosystem of apps where data stays on the device and an account is optional. The first released product is **[Vazie VPN](https://github.com/vazovsky17/VazieVPN)**, a native Android client for VLESS.

<p>
  <a href="https://vazie.app"><img src="https://img.shields.io/badge/Open-vazie.app-4CB0FF?style=for-the-badge&labelColor=04070F&logo=android&logoColor=4CB0FF" alt="Open vazie.app"></a>
  <a href="https://vazie.app/vpn"><img src="https://img.shields.io/badge/Vazie_VPN-APK-04070F?style=for-the-badge&logo=android&logoColor=4477FF" alt="Download Vazie VPN"></a>
  <a href="https://github.com/vazovsky17/VazieVPN"><img src="https://img.shields.io/badge/Source-GitHub-04070F?style=for-the-badge&logo=github&logoColor=8B66FF" alt="Vazie VPN repository"></a>
  <a href="https://t.me/vazieapp"><img src="https://img.shields.io/badge/Log-@vazieapp-04070F?style=for-the-badge&logo=telegram&logoColor=4CB0FF" alt="Vazie project log on Telegram"></a>
</p>

| Product | What it is | Status |
| :-- | :-- | :-- |
| **[Vazie VPN](https://github.com/vazovsky17/VazieVPN)** | VPN client for your own VLESS configuration | **Released · v1.0.0** |
| **[Vazie Keep](https://github.com/vazovsky17/VazieKeep)** | Password manager for `.kdbx` files | Coming soon |
| **[Vazie Relay](https://github.com/vazovsky17/VazieRelay)** | Files between your own devices over the local network | Early stage |
| **[Vazie Rhythm](https://github.com/vazovsky17/VazieRhythm)** | Habits and routines, stored locally | Concept |
| **[Vazie Letter](https://github.com/vazovsky17/VazieLetter)** | A calm email client | Concept |

The rule across the ecosystem is simple: the free version works without an account, data stays with the user, and only capabilities that need a running service are paid.

<br>

`CASES`

## What I actually did in these products

Own projects you can open and check: code on GitHub, design cases on Behance. No client logos and no numbers that cannot be verified.

### 01 · Vazie VPN — a native Android VPN client

`Released · v1.0.0` · `APK on vazie.app`

> **Problem.** Someone already has a `vless://` link from their own or a rented server. They need a client that brings up a tunnel through it with no account and no ads — and says honestly when the connection does not work.

**What I did:** the whole product — the Android app, the Kotlin backend, the website and the servers for the paid VPN Plus plan.

- 23 Gradle modules; a convention plugin checks the boundaries between them on every build
- After connecting, the app separately checks packets, DNS and TLS and shows exactly what is failing
- Configurations are encrypted with a key from Android Keystore; system backup is disabled
- CI unpacks the release APK and fails the build if it finds a secret or a debug tool inside

`Kotlin` `Compose · Material 3` `Glance` `Hilt` `Ktor` `libXray` `Robolectric` `GitHub Actions`

[Product page ↗](https://vazie.app/vpn) &nbsp;·&nbsp; [Code on GitHub ↗](https://github.com/vazovsky17/VazieVPN) &nbsp;·&nbsp; [Case on Behance ↗](https://www.behance.net/gallery/256711563/Vazie-VPN-Native-Android-VPN-Client)

<br>

### 02 · PermAware — an Android privacy utility

`Published on RuStore · v1.0.0`

<img src="assets/permaware-flow.svg" alt="How PermAware turns Android permissions into a private, readable history: packages, interpretation, snapshot comparison, local Room database" width="100%">

> **Problem.** It is hard to tell which data and device features installed apps can access. Sending that list to someone else's server just to get an answer is a bad idea.

**What I did:** the whole app — from parsing permissions to publishing and passing review on RuStore.

- Analysis runs only on the device; results are never sent anywhere
- Permissions are read through standard Android APIs; other apps' settings are not changed
- Reports export to text or JSON through the system share sheet

`Kotlin` `Jetpack Compose` `Android API`

[RuStore ↗](https://www.rustore.ru/catalog/app/app.vazovsky.permaware) &nbsp;·&nbsp; [Code on GitHub ↗](https://github.com/vazovsky17/PermAware) &nbsp;·&nbsp; [Case on Behance ↗](https://www.behance.net/gallery/256712279/PermAware-Android-Privacy-Audit)

<br>

### 03 · The Vazie ecosystem — a shared foundation for several apps

`One of five products released`

> **Problem.** Several apps should look and behave alike but work independently: each is useful on its own and requires nothing from the others.

**What I did:** the product model, the [vazie.app](https://vazie.app) website, the shared account and the monetization rules. VPN is the first app where all of this comes together. Vazie Relay is built on Kotlin Multiplatform with a native UI on Android and iOS.

`Kotlin` `Kotlin Multiplatform` `Jetpack Compose` `SwiftUI`

<br>

`STACK`

## What I work with

| Android | Architecture · data and network | Testing and release | Backend and iOS |
| :-- | :-- | :-- | :-- |
| Kotlin | MVVM · Clean Architecture | JUnit · Robolectric | Backend in Kotlin |
| Jetpack Compose · Material 3 | Multi-module projects | Compose UI tests | Spring Boot · PostgreSQL |
| Coroutines / Flow | Hilt · Gradle convention plugins | GitHub Actions · R8 | Docker |
| Navigation · Glance · VpnService | Room · DataStore · Ktor | Signing and release builds | Swift / SwiftUI |
| Android SDK | Firebase · Android Keystore | Google Play · RuStore | Kotlin Multiplatform |

Backend and iOS so far only in my own projects, and I say so plainly.

<br>

`COMMERCIAL EXPERIENCE`

## In Android development since 2022

| Period | Company | What I did |
| :-- | :-- | :-- |
| Jan 2024 — Aug 2026 | **Zhili Byli** | Independently led the Android side of several commercial projects: architecture, task estimation, building from scratch, maintenance, code review and releases |
| Sep 2023 — Feb 2024 | **Sandbox Development** | Alongside my main job, built a commercial Android app from scratch: from architecture to backend integration |
| Apr 2023 — Aug 2023 | **Smartway** | Migrated a commercial app from React Native to native Android |
| Feb 2022 — Mar 2023 | **Heads and Hands** | Feature team of the Sportmaster app: physical activity tracker, Google Fit, unit tests |

<br>

---

<div align="center">

### Get in touch

The website, projects and contacts are at [vazovsky.pro](https://vazovsky.pro). Telegram is the fastest way to reach me.

**[Message on Telegram →](https://t.me/vazovsky17)**

<br><br>

[vazovsky.pro](https://vazovsky.pro) &nbsp;·&nbsp; [@vazovsky17](https://t.me/vazovsky17) &nbsp;·&nbsp; [vazovsky.hub@gmail.com](mailto:vazovsky.hub@gmail.com) &nbsp;·&nbsp; [Behance](https://www.behance.net/vazovsky17) &nbsp;·&nbsp; [vazie.app](https://vazie.app)

</div>
