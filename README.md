# cake_admin_releases

ریپازیتوری انتشار APK اپ **مدیریت کیک‌آکادمی**.

اپ از [Releases](https://github.com/Pouya-Mohammadi-Parsa/cake_admin_releases/releases) آخرین نسخه را چک می‌کند و در صورت جدید بودن، دانلود را پیشنهاد می‌دهد.

## نحوهٔ انتشار نسخهٔ جدید

1. در پروژهٔ `cake_admin` نسخه را در `pubspec.yaml` بالا ببرید، مثلاً:
   ```yaml
   version: 1.0.1+2
   ```
2. APK بسازید:
   ```bash
   flutter build apk --release
   ```
   فایل خروجی: `build/app/outputs/flutter-apk/app-release.apk`
3. از همین ریپو یک **Release** بسازید:

   ```bash
   gh release create v1.0.1+2 ^
     "D:\project\cake_admin\build\app\outputs\flutter-apk\app-release.apk#cake_admin.apk" ^
     --repo Pouya-Mohammadi-Parsa/cake_admin_releases ^
     --title "1.0.1 (2)" ^
     --notes "توضیح تغییرات این نسخه"
   ```

### قوانین تگ نسخه

- تگ باید با `v` شروع شود و با `version` و `build` در `pubspec.yaml` یکی باشد.
- مثال: `pubspec` → `1.0.1+2` ⇒ تگ → `v1.0.1+2`
- فایل APK را با نامی که به `.apk` ختم شود آپلود کنید (مثلاً `cake_admin.apk`).

## لینک‌ها

| مورد | آدرس |
|------|------|
| سورس اپ | https://github.com/Pouya-Mohammadi-Parsa/cake_admin |
| آخرین ریلیز | https://github.com/Pouya-Mohammadi-Parsa/cake_admin_releases/releases/latest |
