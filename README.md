<div align="center">

<img src="assets/header.svg" alt="Vazovsky — mobile systems, native interfaces, privacy by architecture" width="100%">

<br>

<a href="https://github.com/vazovsky17/PermAware"><img src="https://img.shields.io/badge/featured-PermAware-55E6C1?style=flat-square&labelColor=101525" alt="Featured project: PermAware"></a>
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

## `01 // current signal` — PermAware

### Your apps have permissions. PermAware makes them visible.

[**PermAware**](https://github.com/vazovsky17/PermAware) is a privacy-focused Android app that audits installed apps, explains access to the camera, microphone, location and contacts, and shows **what changed since the previous scan**.

It is deliberately incapable of uploading that inventory: there is no account, backend, analytics or advertising SDK — and the release manifest contains **no `INTERNET` permission**.

- inspect requested and actually granted permissions;
- detect supported special access and explain unknown states honestly;
- compare snapshots and keep a local change history;
- export a report only through an explicit system share action;
- run entirely on-device, with Room as the private source of truth.

| Network access | Measured scan | Test matrix | Release |
| :-- | :-- | :-- | :-- |
| **No permission** | **473 packages in ~1.5 s** | **81 JVM + 113 device** | **v1.0.0 · 4.2 MB APK** |

`minSdk 28` · `targetSdk 36` · `Kotlin` · `Jetpack Compose` · `Material 3` · `RU / EN`

```mermaid
flowchart LR
    A[PackageManager] --> B[permission parser]
    B --> C[attention engine]
    C --> D[device snapshot]
    D --> E[snapshot differ]
    E --> F[(local Room history)]
    F --> G[Compose UI / report]
```

The domain layer is plain Kotlin; Android framework types stop at `data/platform`. That keeps the attention engine, snapshot diffing and report generation fast to test on the JVM, while device tests validate the platform boundaries. The result is **81 JVM tests + 113 device tests**, clean lint and ktlint, and a reproducible CI build.

<p>
  <a href="https://github.com/vazovsky17/PermAware/releases/latest/download/app-release.apk"><img src="https://img.shields.io/badge/Download-APK-55E6C1?style=for-the-badge&labelColor=101525&logo=android&logoColor=55E6C1" alt="Download PermAware APK"></a>
  <a href="https://github.com/vazovsky17/PermAware"><img src="https://img.shields.io/badge/Explore-source-9B8CFF?style=for-the-badge&labelColor=101525&logo=github&logoColor=9B8CFF" alt="Explore PermAware source"></a>
  <a href="https://github.com/vazovsky17/PermAware/releases/tag/v1.0.0"><img src="https://img.shields.io/badge/Release-v1.0.0-7FA7FF?style=for-the-badge&labelColor=101525&logo=githubactions&logoColor=7FA7FF" alt="PermAware v1.0.0 release"></a>
</p>

> PermAware is an inspector, not an antivirus or a fear score. A permission is context, not a verdict.

<br>

## `02 // product lab` — Vazie

**Vazie** is my local-first product lab: focused apps, native interfaces and no pressure to turn every useful tool into a social platform.

| Build | Signal | Engineering focus |
| :-- | :-- | :-- |
| **VPN** | Bring your own configuration | Android networking, secure local storage |
| **Rhythm** | Medication schedules and habits | Offline state, reliable reminders |
| **Keep** | Password manager for `kdbx` vaults | Files stay where the user puts them |
| **Letter** | Email without a feed | Calm information architecture |
| **[Relay](https://github.com/vazovsky17/VazieRelay)** | Android ↔ iOS device link | Kotlin Multiplatform core, native UI on both sides |

<p>
  <a href="https://github.com/vazovsky17/vazovsky17/releases/latest/download/VazieVPN.apk"><img src="https://img.shields.io/badge/Vazie_VPN-download_APK-55E6C1?style=flat-square&labelColor=101525&logo=android&logoColor=55E6C1" alt="Download Vazie VPN APK"></a>
  <a href="https://github.com/vazovsky17/VazieRelay"><img src="https://img.shields.io/badge/Vazie_Relay-source-9B8CFF?style=flat-square&labelColor=101525&logo=github&logoColor=9B8CFF" alt="Vazie Relay source"></a>
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

<p>
  <img src="https://img.shields.io/github/followers/vazovsky17?style=flat-square&logo=github&logoColor=55E6C1&label=followers&labelColor=101525&color=263252" alt="GitHub followers">
  <img src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.github.com%2Fusers%2Fvazovsky17&query=%24.public_repos&style=flat-square&label=public%20repos&labelColor=101525&color=263252&logo=github&logoColor=9B8CFF" alt="Public repositories">
  <img src="https://komarev.com/ghpvc/?username=vazovsky17&style=flat-square&label=profile+views&labelColor=101525&color=263252" alt="Profile views">
</p>

Public work is the visible edge of a larger private monorepo. Projects move into the open when their architecture, build and documentation are ready to be useful outside my machine.

<br>

---

<div align="center">

### Building something that needs to feel native on both sides?

Android, iOS, local-first architecture or a product that should expose less data — tell me what you are working on.

<a href="https://t.me/vazovsky17"><img src="https://img.shields.io/badge/OPEN_A_CHANNEL-55E6C1?style=for-the-badge&labelColor=101525&logo=telegram&logoColor=55E6C1" alt="Start a conversation on Telegram"></a>

<br><br>

`Saratov · UTC+4` &nbsp; `available via Telegram or email`

</div>
