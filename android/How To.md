How To

its easy and simple as 123 

1st download 

2nd 
Point to it in pubspec.yaml

huawei_push:
  path: ../huawei_push  # adjust relative path to where you put it

3rd
Add Huawei repo to settings.gradle.kts

maven { url = uri("https://developer.huawei.com/repo/") }
in both pluginManagement repositories and allprojects repositories

4th
Add AGCP plugin to settings.gradle.kts
id("com.huawei.agconnect") version "1.9.1.301" apply false

5th Apply AGCP in android/app/build.gradle.kts
id("com.huawei.agconnect")

6th
Drop in agconnect-services.json for the new project from AppGallery console.

7th
Copy push_service.dart, hms_service.dart from this project into the new one — they have zero project-specific code, pure reusable logic.


That's the full recipe. The forked plugin folder is the only thing you need to carry forward.

Enjoy


