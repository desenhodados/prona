# Permissões necessárias (módulo de ocorrências)

## Android — android/app/src/main/AndroidManifest.xml
Dentro de `<manifest>`, antes de `<application>`:

```xml
<uses-permission android:name="android.permission.CAMERA" />
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
```

Em `android/app/build.gradle` (ou `build.gradle.kts`), confirmar:
- `minSdk` 21 ou superior (o geolocator exige-o);
- `compileSdk` 34 ou superior.

## iOS — ios/Runner/Info.plist
Dentro de `<dict>`:

```xml
<key>NSCameraUsageDescription</key>
<string>A câmara é usada para fotografar as ocorrências.</string>
<key>NSPhotoLibraryUsageDescription</key>
<string>A galeria é usada para anexar fotografias às ocorrências.</string>
<key>NSLocationWhenInUseUsageDescription</key>
<string>A localização é usada para registar as coordenadas da ocorrência.</string>
```
