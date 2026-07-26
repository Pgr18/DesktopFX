[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=ak-git_DesktopFX&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=ak-git_DesktopFX)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=ak-git_DesktopFX&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=ak-git_DesktopFX)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=ak-git_DesktopFX&metric=security_rating)](https://sonarcloud.io/dashboard?id=ak-git_DesktopFX)

[![Bugs](https://sonarcloud.io/api/project_badges/measure?project=ak-git_DesktopFX&metric=bugs)](https://sonarcloud.io/dashboard?id=ak-git_DesktopFX)
[![Code Smells](https://sonarcloud.io/api/project_badges/measure?project=ak-git_DesktopFX&metric=code_smells)](https://sonarcloud.io/dashboard?id=ak-git_DesktopFX)
[![Duplicated Lines (%)](https://sonarcloud.io/api/project_badges/measure?project=ak-git_DesktopFX&metric=duplicated_lines_density)](https://sonarcloud.io/dashboard?id=ak-git_DesktopFX)
[![Vulnerabilities](https://sonarcloud.io/api/project_badges/measure?project=ak-git_DesktopFX&metric=vulnerabilities)](https://sonarcloud.io/dashboard?id=ak-git_DesktopFX)

## Run (IntelliJ / VS Code / Cursor)

Requires **JDK 21** (toolchain) and JavaFX **21.0.6**, plus Gradle Wrapper.

### CLI

```bash
./gradlew :Desktop:run -Pprofile=rcms
./gradlew :Desktop:run -Pprofile=rcm
./gradlew :Desktop:run -Pprofile=loopback
```

### VS Code / Cursor

1. Install recommended extensions (prompt on open): **Extension Pack for Java**, **Gradle for Java**.
2. **Reload Window**, wait for Gradle import (daemon must be JDK 21 — pinned in `gradle.properties`).
3. **Run and Debug** → `Rcms` / `Rcm` (Gradle `--debug-jvm` + attach; same as CLI).
4. Or **Terminal → Run Task…** → `run: rcms`.

If IDE shows `Unsupported class file major version 69`, system `java` is JDK 25 — restart Cursor after reload; Gradle is forced to JDK 21 via `org.gradle.java.home`.
