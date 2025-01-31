---
translatedFrom: en
translatedWarning: Если вы хотите отредактировать этот документ, удалите поле «translationFrom», в противном случае этот документ будет снова автоматически переведен
editLink: https://github.com/ioBroker/ioBroker.docs/edit/master/docs/ru/adapterref/iobroker.opendtu/README.md
title: ioBroker.opendtu
hash: 5/aAAEmF79xpuBgt5z18ES7+acrc21rpLE6m5pO7Woc=
---
![Логотип](../../../en/adapterref/iobroker.opendtu/admin/opendtu.png)

![версия NPM](https://img.shields.io/npm/v/iobroker.opendtu.svg)
![Загрузки](https://img.shields.io/npm/dm/iobroker.opendtu.svg)
![Количество установок](https://iobroker.live/badges/opendtu-installed.svg)
![Текущая версия в стабильном репозитории](https://iobroker.live/badges/opendtu-stable.svg)
![НПМ](https://nodei.co/npm/iobroker.opendtu.png?downloads=true)

# IoBroker.opendtu
**Тесты:** ![Тестирование и выпуск](https://github.com/o0shojo0o/ioBroker.opendtu/workflows/Test%20and%20Release/badge.svg) [![CodeQL](https://github.com/o0shojo0o/ioBroker.opendtu /действия/рабочие процессы/codeql.yml/badge.svg)](https://github.com/o0shojo0o/ioBroker.opendtu/actions/workflows/codeql.yml)

## Адаптер opendtu для ioBroker
Этот адаптер получает данные из проекта [OpenDTU](https://github.com/tbnobody/OpenDTU), доступные в режиме реального времени.
Кроме того, через адаптер можно использовать следующие точки данных для ограничения мощности OpenDTU.

```
- opendtu.0.xxxxxx.power_control.limit_nonpersistent_absolute
- opendtu.0.xxxxxx.power_control.limit_nonpersistent_relative
- opendtu.0.xxxxxx.power_control.limit_persistent_absolute
- opendtu.0.xxxxxx.power_control.limit_persistent_relative
```

Для получения дополнительной информации о точках данных см. их описание или нажмите [здесь](https://github.com/tbnobody/OpenDTU/blob/master/docs/MQTT_Topics.md#inverter-limit-specific-topics).

## Конфигурация
1. Создайте новый экземпляр адаптера
2. Заполните схему *(по умолчанию http)*, WebUi-Address и WebUi-port *(по умолчанию 80)* оборудования [OpenDTU](https://github.com/tbnobody/OpenDTU).
3. Установите WebUi-пароль **(это обязательно, если он неверный, ограничение не может быть установлено!)**
4. Сохраните настройки

## Changelog
<!--
 https://github.com/AlCalzone/release-script#usage
    npm run release major -- -p iobroker license --all 0.9.8 -> 1.0.0
    npm run release minor -- -p iobroker license --all 0.9.8 -> 0.10.0
    npm run release patch -- -p iobroker license --all 0.9.8 -> 0.9.9
    npm run release prerelease beta -- -p iobroker license --all v0.2.1 -> v0.2.2-beta.0
	Placeholder for the next version (at the beginning of the line):
	### **WORK IN PROGRESS**
-->
### 0.1.7 (2023-06-30)

- (o0shojo0o) workaround for incorrectly used button data point

### 0.1.6 (2023-06-30)

- (o0shojo0o) fix power control (power_off)

### 0.1.5 (2023-05-15)

- (o0shojo0o) code optimizations

### 0.1.4 (2023-03-23)

- (o0shojo0o) fix power control `on`, `off`, `restart`
- (o0shojo0o) support for password protected liveview
- (o0shojo0o) other small fixes

### 0.1.2 (2023-03-03)

- (o0shojo0o) fix yield* values

### 0.1.1 (2023-02-24)

- (o0shojo0o) state rolls corrected
- (o0shojo0o) add DTU datapoint `rssi` and `ip`
- (o0shojo0o) repeated writing of the yieldtotal set to 00:01:00. (is necessary for e.g. sourceanalytix)

### 0.1.0 (2023-02-17)

- (o0shojo0o) initial release

## License
MIT License

Copyright (c) 2023 Dennis Rathjen <dennis.rathjen@outlook.de>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.