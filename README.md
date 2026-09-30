<div align="center">

<img src="assets/header.svg" alt="Vazovsky — mobile systems, native interfaces, privacy by architecture" width="100%">

<br>

<a href="https://github.com/vazovsky17/VazieVPN"><img src="https://img.shields.io/badge/featured-Vazie_VPN-55E6C1?style=flat-square&labelColor=101525" alt="Featured project: Vazie VPN"></a>
<img src="https://img.shields.io/badge/focus-mobile_systems-9B8CFF?style=flat-square&labelColor=101525" alt="Focus: mobile systems">
<img src="https://img.shields.io/badge/based_in-Saratov-6A78A8?style=flat-square&labelColor=101525" alt="Based in Saratov">

<br><br>

**I build mobile products where platform constraints become part of the design.**<br>
Android is home ground. iOS is the next native surface. Shared logic belongs in KMP; private data belongs on the device.

<br>

<a href="https://t.me/vazovsky17"><img src="https://img.shields.io/badge/Telegram-101525?style=for-the-badge&logo=telegram&logoColor=55E6C1" alt="Telegram @vazovsky17"></a>
<a href="mailto:vazovsky.app@gmail.com"><img src="https://img.shields.io/badge/Email-101525?style=for-the-badge&logo=gmail&logoColor=9B8CFF" alt="Email vazovsky.app@gmail.com"></a>
<a href="https://www.linkedin.com/in/vazovsky17"><img src="https://img.shields.io/badge/LinkedIn-101525?style=for-the-badge&logo=linkedin&logoColor=7FA7FF" alt="LinkedIn vazovsky17"></a>

</div>

<br>

## `01 // current signal` — [Vazie VPN](https://github.com/vazovsky17/VazieVPN)

`Android 9+` · `v1.0.0` · `released` · `VLESS` · `bring your own configuration or use VPN Plus`

Vazie VPN is a native Android client for VLESS. Your own configuration works free and without an account; **VPN Plus** adds Vazie-managed servers with one-off monthly or yearly payments and no auto-renewal.

The first stable release includes split tunneling, packet/DNS/TLS health checks, encrypted local configuration storage, a Quick Settings tile, Glance widgets, launcher shortcuts, built-in guides, two themes and English/Russian localization. The app is built as 23 Gradle modules and backed by 950+ tests.

<p>
  <a href="https://vazie.app/vpn"><img src="https://img.shields.io/badge/Download-APK-55E6C1?style=for-the-badge&labelColor=101525&logo=android&logoColor=55E6C1" alt="Download Vazie VPN APK"></a>
  <a href="https://github.com/vazovsky17/VazieVPN"><img src="https://img.shields.io/badge/Open-repository-9B8CFF?style=for-the-badge&labelColor=101525&logo=github&logoColor=9B8CFF" alt="Open the Vazie VPN repository"></a>
  <a href="https://github.com/vazovsky17/VazieVPN/releases/tag/v1.0.0"><img src="https://img.shields.io/badge/Release-v1.0.0-7FA7FF?style=for-the-badge&labelColor=101525&logo=githubactions&logoColor=7FA7FF" alt="Vazie VPN v1.0.0 release"></a>
  <a href="https://t.me/vazieapp"><img src="https://img.shields.io/badge/Project-log-263252?style=for-the-badge&labelColor=101525&logo=telegram&logoColor=55E6C1" alt="Vazie project log on Telegram"></a>
</p>

<br>

## `02 // product lab` — Vazie

**Vazie** is my local-first product lab: focused apps, native interfaces and no pressure to turn every useful tool into a social platform. One product is shipping today; the rest are shown at their actual stage rather than presented as finished apps.

| Build | Signal | Engineering focus |
| :-- | :-- | :-- |
| **[VPN](https://github.com/vazovsky17/VazieVPN)** · *v1.0.0 released* | Your own VLESS configuration for free, or managed servers with VPN Plus | Android `VpnService`, Xray, encrypted storage, tunnel health probes |
| **[Relay](https://github.com/vazovsky17/VazieRelay)** · *bootstrap* | Android ↔ iOS device link; user-facing transfer is not implemented yet | Kotlin Multiplatform core, Compose on Android, SwiftUI on iOS, early LAN discovery |
| **[Keep](https://github.com/vazovsky17/VazieKeep)** · *concept* | Your `.kdbx` vault, without surrendering it to a service | User-owned files, native Android UI, optional services |
| **[Rhythm](https://github.com/vazovsky17/VazieRhythm)** · *concept* | Local-first medication schedules and habits | Offline state, reliable reminders, optional sync |
| **[Letter](https://github.com/vazovsky17/VazieLetter)** · *concept* | Calm, local-first email | Single-account core, optional multi-account access |

The rule across the lab is simple: the local core stays useful on its own, while paid features cover capabilities that require an operated service. VPN is the first complete expression of that model. Its Android client is source-available, while the Kotlin control plane, website and infrastructure operate VPN Plus. Relay is an early cross-platform foundation; Keep, Rhythm and Letter remain product directions, not downloadable releases.

<p>
  <a href="https://github.com/vazovsky17/VazieVPN"><img src="https://img.shields.io/badge/Vazie_VPN-public_repo-55E6C1?style=flat-square&labelColor=101525&logo=github&logoColor=55E6C1" alt="Open the public Vazie VPN repository"></a>
  <a href="https://vazie.app/vpn"><img src="https://img.shields.io/badge/Vazie_VPN-download_APK-7FA7FF?style=flat-square&labelColor=101525&logo=android&logoColor=7FA7FF" alt="Download Vazie VPN APK"></a>
  <a href="https://github.com/vazovsky17/VazieRelay"><img src="https://img.shields.io/badge/Vazie_Relay-follow_the_build-55E6C1?style=flat-square&labelColor=101525&logo=github&logoColor=55E6C1" alt="Follow the Vazie Relay build"></a>
  <a href="https://t.me/vazieapp"><img src="https://img.shields.io/badge/project_log-@vazieapp-7FA7FF?style=flat-square&labelColor=101525&logo=telegram&logoColor=7FA7FF" alt="Vazie project log on Telegram"></a>
</p>

<br>

## `03 // engineering profile`

| Native mobile | Shared systems | Delivery |
| :-- | :-- | :-- |
| Kotlin · Jetpack Compose · Android SDK | Kotlin Multiplatform · Coroutines · Flow | Gradle · GitHub Actions · signed releases |
| Swift · SwiftUI · Apple SDKs | Room · Ktor · offline-first data | Docker · Linux · VPS infrastructure |
| Material 3 · adaptive UI | MVVM · clean boundaries · DI with Hilt | JVM · instrumentation · UI testing |

```kotlin
val approach = MobileEngineering(
    ui = Native(platform = currentPlatform),
    core = Shared(onlyWhenItActuallyHelps),
    data = LocalFirst,
    quality = Tests + MeasuredPlatformBehavior
)
```

I care about the parts that survive the demo: state ownership, failure modes, background limits, migrations, signing, release automation and interfaces that still make sense six months later.

<br>

## `04 // telemetry`

### The counters move. The standard for publishing does not.

<p>
  <img src="https://img.shields.io/github/followers/vazovsky17?style=flat-square&logo=github&logoColor=55E6C1&label=followers&labelColor=101525&color=263252" alt="GitHub followers">
  <img src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.github.com%2Fusers%2Fvazovsky17&query=%24.public_repos&style=flat-square&label=public%20repos&labelColor=101525&color=263252&logo=github&logoColor=9B8CFF" alt="Public repositories">
  <img src="https://komarev.com/ghpvc/?username=vazovsky17&style=flat-square&label=profile+views&labelColor=101525&color=263252" alt="Profile views">
</p>

These numbers are live, but they are not the metric I build for. Most work begins in a private monorepo, where ideas are allowed to be incomplete, renamed or discarded without ceremony.

A project crosses into public view only when someone else can **understand the architecture, reproduce the build and learn from the decisions** — not merely scroll through a commit history. What appears here is the released edge of a much larger workshop.

`prototype in private` → `measure real behavior` → `stabilize the boundaries` → `document the why` → **`publish`**

<br>

---

<div align="center">

### Building something that needs to feel native on both sides?

Android, iOS, local-first architecture or a product that should expose less data — tell me what you are working on.

<a href="https://t.me/vazovsky17"><img src="https://img.shields.io/badge/OPEN_A_CHANNEL-55E6C1?style=for-the-badge&labelColor=101525&logo=telegram&logoColor=55E6C1" alt="Start a conversation on Telegram"></a>

<br><br>

`Saratov · UTC+4` &nbsp; `available via Telegram or email`

</div>
