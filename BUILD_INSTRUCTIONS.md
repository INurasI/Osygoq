# Urban Reign Android — FIXED-v7

## Өзгерістер (v6 → v7)

- Manifest: `isGame=true`, толық `configChanges` (PS2Recomp стилі), GLES2 feature
- Native: `log` + `android` + `EGL` + `GLESv2` + `OpenSLES` link
- Logcat: `UrbanReignDiag` **және** `raylib` тегі (PS2Recomp README бойынша)
- Бір ғана workflow: `urban-reign-android-apk.yml`
- CMake: PLATFORM=Android, GLES2 flags, build error dump
- ISO FD: `#include <limits>`
- Runtime env: MCSERV=0, SIO2, hang dump
- Glue timed-wait + 16 MiB stack

## GitHub

1. Репо **private**
2. Zip-ті root-қа шығарыңыз
3. `.github/workflows/` ішінде **тек** `urban-reign-android-apk.yml` қалсын (басқа yml өшіріңіз)
4. Actions → **Urban Reign Android APK** → Run workflow
5. APK artifact

## Телефон

```
adb logcat -s UrbanReignDiag raylib *:E
```

Лог файл: `Android/data/kz.nurasql77.urbanreign/files/urban_native.log`

## Шектеу

CPU GS; cutscene off; playability APK+logcat-тан кейін.
