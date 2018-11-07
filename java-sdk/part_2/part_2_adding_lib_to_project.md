---
title: Добавление библиотеки к проекту
sidebar: javasdk_sidebar
permalink: part_2_adding_lib_to_project.html
---

# Добавление библиотеки к проекту

В ```build.gradle``` проекта необходимо добавить ссылку на репозиторий jitpack:

```
allprojects {
    repositories {
        maven { url "https://jitpack.io" }
    }
}
```

в модуле ```build.gradle``` необходимо прописать зависимость и указать точную версию:

    implementation 'com.github.kassatka-online:android-api:' + apiLatestVersion
	
где, ```apiLatestVersion``` определена в секции ```ext``` того же ```build.gradle``` файла.

Также необходимо указать ```minSdkVersion``` проекта:

```
defaultConfig {
	minSdkVersion 22
	...
}
```

Для корректной сборки проекта должны быть добавлены следующие строки в ```build.gradle``` файл модуля:

```
android {
  compileOptions {
    sourceCompatibility JavaVersion.VERSION_1_8
    targetCompatibility JavaVersion.VERSION_1_8
  }}
```
