---
title: '📜 Создание MundoAddon'
description: 'Информация, о создании MundoAddon'
pubDate: 'January 02 2025'
course: 'MundoMagis: Arcane'
isHidden: true
---

## Создание аддона

Для создания аддона создайте новый Java класс и унаследуйте его от интерфейса ```IMundoAddon``` из пакета ```ru.bananus.mmarcane.api```.

Унаследуйте из интерфейса функции:
- ```getAddonId()```
- ```getModId()```
- ```getItemRegistry()```
- ```getAddonSpells()```

## Функция ```getAddonId()```
### Возвращаемые значения
Данная функция возвращает ```String``` - уникальный идентификатор аддона.

### Использование
Используется для генерации данных аддона.

## Функция ```getModId()```
### Возвращаемые значения
Данная функция возвращает ```String``` - идентификатор вашего мода.

### Использование
Используется для генерации данных аддона.

## Функция ```getItemRegistry()```
### Возвращаемые значения
Данная функция возвращает ```DeferredRegister<Item>``` - DeferredRegister для предметов из вашего мода.

### Использование
Используется для генерации книг заклинаний аддона.

## Функция ```getAddonSpells()```
### Возвращаемые значения
Данная функция возвращает ```List<ISpell>``` - Содержит List с объектами созданных вами заклинаний.

### Использование
Используется для генерации книг заклинаний и подключения всех заклинаний к моду.

## Подключение аддона к основному моду
Для того, чтобы Ваш аддон заработал и отображался в игре его необходимо подключить к системе аддонов MundoMagis.
#### Для этого:
В конструкторе главного класса вашего мода вызовите функцию ```loadAddon()``` из класса ```AddonRegistry```. Передайте в параметры функции объект класса вашего аддона.

## Локализация названия аддона
В файлы локализации добавьте ключ ```addon.<addonId вашего аддона>``` со значением перевода.

## Проверка
Готово! Ваш аддон готов. Теперь, в творческом режиме, появится вкладка с предметами из аддонов. Там, Вы сможете найти свои книги заклинаний.