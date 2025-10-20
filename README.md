# OzonBarCode
Штрихкод из цифрового кода для получения/возврата товара на [OZON](https://www.ozon.ru/) (Linux/Windows).

**Компиляция:** Lazarus-4.2-x86_64 + пакет [LazBarcodes](https://wiki.lazarus.freepascal.org/LazBarcodes) (из сетевого диспетчера пакетов)

На сайте **OZON** (для настольных компьютеров) отсутствует возможность получения штрихкода заказа, он есть только в мобильной версии. Таким образом, сделать быстрое получение или возврат покупки становится затруднительным.

![](https://github.com/AKotov-dev/OzonBarCode/blob/main/Snapshot2.png)

Программа **OzonBarCode** создаёт штрихкод после ввода/вставки цифрового кода заказа. Теперь можно сфотографировать или сохранить готовый штрихкод вместе с цифровым кодом на телефон и отправляться за товаром в пункт выдачи.

Для запуска программы распакуйте нужный архив и запустите файл **ozon_barcode** (для Linux) или **ozon_barcode.exe** (для Windows).

**Примечание:** На смартфоне должна быть включена [отладка через USB](https://losst.pro/kak-podklyuchitsya-k-telefonu-adb). Подключение смартфона через порт компьютера `USB2`. Для работы смартфона через ADB для Windows могут потребоваться драйверы. Подробнее можно ознакомиться, например [здесь](https://adbappcontrol.com/ru/docs/) в разделе `"Драйвера (программа не видит устройство)"`. Для Linux должны быть установлены правила udev, а пользователь должен быть добавлен в группу `adbusers`:
```
su/password
groupadd adbusers; usermod -aG adbusers $(logname)
wget https://raw.githubusercontent.com/M0Rf30/android-udev-rules/master/51-android.rules -O /etc/udev/rules.d/51-android.rules
reboot
```
### Использованы материалы и ПО
+ Статья с сайта Losst (см. выше)
+ Руководство `ADB AppControl` (см. выше)
+ These archives include `adb` and `adb.exe`, as well as libraries from the `Android SDK` licensed under the `Apache License 2.0`
