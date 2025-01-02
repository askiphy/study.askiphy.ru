---
title: '☁️ Вступление'
description: 'Информация, о подключении мода к проекту'
pubDate: 'January 02 2025'
course: 'MundoMagis: Arcane'
---

# Начало

Внимание!
Документация описывает работу с MundoMagis: Arcane под Minecraft Forge 1.20.1

## Добавление в проект
Для начала Вам необходимо подключить репозиторий CurseMaven и GeckoLib в файле ```build.gradle```.
Блок ```repositories``` по умолчанию есть в файле ```build.gradle```.
##### Вставьте туда следующий код:

```
maven {
    name = 'Gecko Lib'
    url = 'https://dl.cloudsmith.io/public/geckolib3/geckolib/maven/'
}
maven {
    url "https://cursemaven.com"
    content {
        includeGroup "curse.maven"
    }
}
```
После добавления, ниже Вы найдете ```dependencies```. В этом блоке происходит подключение необходимых модов.
##### Вставьте туда следующий код:
```
implementation fg.deobf("curse.maven:mundomagis-arcane-1116432:5791963")
implementation fg.deobf("curse.maven:architectury-api-419699:5137938")
implementation fg.deobf("software.bernie.geckolib:geckolib-forge-1.20.1:4.4.6")
implementation fg.deobf("com.eliotlash.mclib:mclib:20")
```

После этого перезагрузите проект в IDE и Вы увидите классы мода.