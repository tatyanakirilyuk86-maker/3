Vision Tracker — Android project

Це вихідний Android-проєкт, а не APK. APK можна зібрати онлайн без встановлення Android Studio через GitHub Actions.

Підготовка репозиторію:
1. Створіть на GitHub новий репозиторій (для простішого безкоштовного запуску workflow — Public).
2. Завантажте в корінь репозиторію ВМІСТ цієї папки: app/, build.gradle, settings.gradle, gradle.properties, .github/.
   Не завантажуйте ZIP-архів як є та не додавайте зовнішню папку VisionTrackerAndroidProject як ще один рівень.
3. Перейдіть у вкладку Actions. Оберіть "Build Vision Tracker APK" і натисніть Run workflow.
4. Дочекайтеся завершення із зеленою галочкою.
5. У сторінці запуску (workflow run) унизу в секції Artifacts скачайте VisionTracker-APK.zip.
6. Розпакуйте ZIP: всередині буде app-debug.apk. Перенесіть APK на Android і встановіть.

Workflow вже включений у .github/workflows/build-apk.yml.

Технічні параметри:
- Android Gradle Plugin 8.7.3
- Gradle 8.9
- Java 17
- compile/target SDK 35, min SDK 23
- WebView завантажує app/src/main/assets/index.html; робота офлайн.
- Прогрес зберігається локально через WebView localStorage.

Якщо збірка не проходить, відкрийте логи конкретного workflow run та скопіюйте повідомлення помилки.
