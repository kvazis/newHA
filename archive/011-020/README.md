### Архив, итерации - 11-20    
:leftwards_arrow_with_hook: [Вернуться в основной список](https://github.com/kvazis/newHA/blob/master/README.md)    
____
### 2022 04 13 Итерация 20    

Много косметических изменений, переносил кейсы управления освещением в гостиной.    

#### Конфигурация    
:arrow_right: [configuration.yaml](https://github.com/kvazis/newHA/blob/master/configuration.yaml) - добавлен раздел input_button: для виртуальных кнопок подробнее в [блоге про input button](https://youtu.be/b4VB-Sm9rvs)    

#### Пакаджи    
:arrow_right: [lr_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_light.yaml) - перенес несколько автоматизаций по управлению светом, контроль и перезагрузка зависших люстр    
:arrow_right: [lr_light_cinema.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_light_cinema.yaml) - отдельный пакадж для цветной подсветки для просмотра ТВ, показано в [блоге про input button](https://youtu.be/b4VB-Sm9rvs)    
Остальные изменения - касаются добавления описаний объектов в раздел customize    

#### Интерфейс, в режиме yaml    

Изменены `multiple-entity-row` карты для розеток с `utility meter` - подсчет электроэнергии за месяц, подробнее в [блоге](https://youtu.be/rUFduUE0ZMc)    
:arrow_right: [05_lr_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/05_lr_control.yaml) - добавлены оставшиеся светильники, карты розеток, тут пример карты entity button из [блога про input button](https://youtu.be/b4VB-Sm9rvs)    
:arrow_right: [07_dd_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/07_dd_control.yaml) - карты розеток с энергомониторингом    
:arrow_right: [08_da_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/08_da_control.yaml) - карты розеток с энергомониторингом    

____
### 2022 04 05 Итерация 19    

#### Пакаджи    
:arrow_right: [dd_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_sensors.yaml) - добавлен темплейт перевода давления ГПа в мм рт. ст, с проверкой на корректность данных    
:arrow_right: [lr_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_light.yaml) - добавлены описания светильников    
:arrow_right: [lr_switch_power.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_switch_power.yaml) - новый пакадж для реле и розеток, добавлены описания, запись показаний энергомониторинга    

#### Интерфейс, в режиме yaml    
:arrow_right: [07_dd_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/07_dd_control.yaml) - добавлены графики с датчика климата - температура, влажность, давление    
:arrow_right: [02_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml) - добавлены динамические карты, отображающие switch с потреблением более 10 Ватт, включенные светильники, таймеры    

Страница `02_control.yaml`    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0013.png)

____
### 22022 03 29 Итерация 18    

#### Пакаджи    
:arrow_right: [dd_heat.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_heat.yaml) - добавлена автоматизация которая при отключении режима отопления устанавливает на термоголовке t 15    
:arrow_right: [da_heat.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_heat.yaml) - аналогично    
:arrow_right: [lr_heat_1.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_heat_1.yaml) - аналогично    
:arrow_right: [lr_heat_2.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_heat_2.yaml) - аналогично    
:arrow_right: [kn_heat.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_heat.yaml) - по шаблону добавлено управление последней, пятой термоголовкой    
:arrow_right: [kn_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_sensors.yaml) - пакадж для сенсоров в кухне    

#### Интерфейс, в режиме yaml    
:arrow_right: [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлена страница управления для кухни - климат    
:arrow_right: [04_kn_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/04_kn_climate.yaml) - страница климата и управление термостатом для кухни    

Страница `04_kn_climate.yaml`    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0012.png)

____
### 2022 03 28 Итерация 17    

#### Пакаджи    
:arrow_right: [kn_boiler.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_boiler.yaml) - пакадж управления вторым бойлером на кухне, в отличии от первого - он, при активации режима нагрева, работает в течении дня, схема немного проще.    

#### Интерфейс, в режиме yaml    
:arrow_right: [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлена страница управления для кухни - бойлер    
:arrow_right: [04_kn_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/04_kn_control.yaml) - страница управления для кухни - бойлер    

По остальным страницам - косметические изменения.     
____
### 2022 03 26 Итерация 16    

#### Пакаджи    
:arrow_right: [bt_alarm.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/bt_alarm.yaml) - добавлены автоматизации по обнаружению протечки. уведомление в телеграм, голосом через шлюз Xiaomi, световая. после устранения - так же уведомление    

#### Интерфейс, в режиме yaml    
:arrow_right: [06_bt_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/06_bt_control.yaml) - на страницу добавлены датчики протечек, немного изменен формат отображения данных    

____
### 2022 03 25 Итерация 15    

#### Пакаджи    

:arrow_right: [ip_camera.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/ip_camera.yaml) - добавлены камеры, rtsp потоки    
:arrow_right: [da_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_light) - добавлены дополнительные автоматизации и сущности для освещения в детской А    
:arrow_right: [da_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_switch.yaml) - добавлены новые описания switch    
:arrow_right: [lr_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_light.yaml) - пакадж для управления освещением в гостиной (начал перевод с старых серверов)    

#### Интерфейс, в режиме yaml    
:arrow_right: [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлена страница управления для гостиной    
:arrow_right: [05_lr_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/05_lr_control.yaml) - добавлены потолочные светильники для гостиной    
:arrow_right: [08_da_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/08_da_control.yaml) - добавление новых сущностей на страницу управление, изменение шаблона (информация по zigbee датчикам)    

Страница `08_da_control.yaml`    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0011.png)
____
### 2022 03 23 Итерация 14    

#### Пакаджи    
:arrow_right: [bt_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/bt_sensors.yaml) - добавление описаний новых сенсоров    
:arrow_right: [bt_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/bt_light.yaml) - управление освещением, яркость в зависимости от времени суток, длительность работы таймера автоотключение в зависимости от времени и состояния двери    
:arrow_right: [bt_vent.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/bt_vent.yaml) - управление вентиляцией, включение по превышению порога влажности, таймер автоотключения, условие на время работы    

#### Интерфейс, в режиме yaml    
:arrow_right: [06_bt_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/06_bt_control.yaml) - страница для ванной комнаты, освещение, вентиляция, добавлен данные с сенсора климата    

Страница `06_bt_control.yaml`    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0010.png)

____
### 2022 03 21 Итерация 13    

Не совсем корректно стал работать мой старый пакадж по управлению бойлером. Пришлось переписать, сразу на новом сервере.    
#### Пакаджи    
:arrow_right: [boiler.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/boiler.yaml)    
Бойлер можно включить только когда активирован режим нагрева бойлера - связка шаблонного выключателя и бинарного сенсора на платформе mqtt. Есть проверка на его состояние, если он отключен, то питание будет выключаться. В автоматическом режиме работает по часу утром и вечером - интервалы установлены в бинарных сенсорах платформы tod (time of day). Так же возможно ручное включение, для этого сделан еще один шаблонный switch - связанный с часовым таймером. После ручного включения бойлер также будет работать 1 час - по таймеру.    

#### Интерфейс, в режиме yaml    
:arrow_right: [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлена страница ванной комнаты    
:arrow_right: [06_bt_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/06_bt_control.yaml) - страница для ванной комнаты, управление бойлером. Для таймера применена карта flipdown-timer-card    

#### Конфигурация    
:arrow_right: [configuration.yaml](https://github.com/kvazis/newHA/blob/master/configuration.yaml) - добавлена карта flipdown-timer-card    

Страница `06_bt_control.yaml`   
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0009.png)

____
###  2022 02 24 Итерация 12    

#### Обновление которое планировалось на 24 февраля после выхода урока по голосовым уведомлениям. Война, развязанная россией против народа Украины - поменяла все планы. Фактическая дата публикации - 18 марта, на сегодняшний день я в порядке, как будет дальше - неизвестно, обстрелы ежедневно.    

#### Пакаджи     
:arrow_right: [dd_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_light.yaml) - добавление автоматизаций по управлению освещением    
:arrow_right: [dd_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_switch.yaml) - добавлены новые сущности в customize, управление принтером     
:arrow_right: [dd_hum.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_hum.yaml) - управление увлажнителем воздуха через реле выключателя с энергомониториноом     
:arrow_right: [da_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_light) - управление освещением    
:arrow_right: [da_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_switch.yaml) - добавлены описания switch     
:arrow_right: [dd_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_sensors.yaml) - добавление описаний новых сенсоров    
:arrow_right: [da_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_sensors.yaml) - добавление описаний новых сенсоров    
:arrow_right: [lr_air_quality.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_air_quality.yaml) - контроль и уведомления о качестве воздуха - CO2, [урок по голосовым уведомлениям](https://youtu.be/xKbEj7pE9iU)    
:arrow_right: [lr_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_sensors.yaml) - добавление описаний новых сенсоров    

#### Интерфейс, в режиме yaml    
:arrow_right: [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлены новые страницы    
:arrow_right: [07_dd_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/07_dd_control.yaml) - страница управления, добавлены новые сущности    
:arrow_right: [08_da_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/08_da_control.yaml) - новая страница управления по шаблону    
:arrow_right: [05_lr_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/05_lr_climate.yaml) - добавление данных по CO2, изменени формат вывода    

____
###  2022 02 21 Итерация 11    

Перенес управление отоплением еще в одной комнате, суть таже, кроме того, что используются 2 одинаковые  термоголовки. За счет использования шаблонных пакаджей - перенос занимает до 5 минут.    
#### Пакаджи     
:arrow_right: [lr_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_sensors.yaml) - сенсоры для климат контроля в гостиной    
:arrow_right: [lr_heat_1.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_heat_1.yaml) - управление термоголовкой TV01    
:arrow_right: [lr_heat_2.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_heat_2.yaml) - управление термоголовкой TV01    
:arrow_right: [dd_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_sensors.yaml) - добавлен сенсор освещенности, перенос switch в новый пакадж    
:arrow_right: [da_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_sensors.yaml) - перенос switch в новый пакадж    
:arrow_right: [dd_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_light.yaml) - добавлены иконки для светильников в секции customize    
:arrow_right: [dd_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_switch.yaml) - пакадж для switch - подбор шаблона для отображения сущностей розеток и реле    
:arrow_right: [da_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_switch.yaml) - пакадж для switch    

#### Интерфейс, в режиме yaml    
:arrow_right: [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлены новые страницы    
:arrow_right: [05_lr_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/05_lr_climate.yaml) - страница управления термоголовками и мониторинг датчика климата    
:arrow_right: [07_dd_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/07_dd_climate.yaml) - добавлен график по освещенности    
:arrow_right: [07_dd_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/07_dd_control.yaml) - страница управления, добавлены светильники, розетка, несколько сенсоров (пока в поиске универсального шаблона)    
:arrow_right: [08_da_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/08_da_climate.yaml) - косметические изменения    

Страница `07_dd_control.yaml` Вариант оформления страницы управления    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0008.png)

____
### Как поддержать развитие проекта?
* [Стать спонсором моего Youtube](http://kvazis.link/sponsorship)
* [Подписаться на Patreon](http://kvazis.link/patreon)
* [Перевод через Paypal](http://kvazis.link/paypal)
* Webmoney - Z243592584952
* BTC - 1Gzr7WQugfnPuWVawu47EiCMTDUBqCAshj
* ETH - 0xa0ce3E29Cf537013649Ae9cdbc08C4853fF91FAc
* LTC - ltc1qs493yk2wk9ywx5h6aruk4p9zm75hx42ekv4ym2
* TRX - TFTCLqvS1tMBwokRHBwz1TCDJ4oD1Z5zPk