### Архив, итерации - 1-10    
:leftwards_arrow_with_hook: [Вернуться в основной список](https://github.com/kvazis/newHA/blob/master/README.md)    
____
### 2022 02 21 Итерация 10    

Добавлен, пока экспериментальный (надо понаблюдать как будет работать) сенсор и карта в lovelace, для отслеживания обновлений аддонов в Supervisor    

#### Пакаджи    
:arrow_right: [system_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/system_sensors.yaml) - добавлен сенсор проверки обновлений Supervisor    

```yaml
- platform: command_line
  name: supervisor_updates
  command: 'curl http://supervisor/supervisor/info -H "Authorization: Bearer $(printenv SUPERVISOR_TOKEN)" | jq ''{"newest_version":.data.version_latest,"current_version":.data.version,"update_available":.data.update_available,"addons":[.data.addons[] | select(.update_available)]}'''
  value_template: "{{ value_json.addons | length }}"
  unit_of_measurement: доступно обновлений
  json_attributes:
  - update_available
  - newest_version
  - current_version
  - addons
```
#### Интерфейс, в режиме yaml    
:arrow_right: [01_system.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/01_system.yaml) - карта markdown для Supervisor, выводящая список и версии репозиториев для обновления    

```yaml
- type: markdown
  content: |
    <ha-icon icon="mdi:home-assistant"></ha-icon>&nbsp;&nbsp;&nbsp;Обновлений для Supervisor - {{ states('sensor.supervisor_updates') | default }}
    > {% for addon in state_attr('sensor.supervisor_updates', 'addons') %}
    > {{ addon.name }} {{ addon.version }} -> {{ addon.version_latest }}
    > {% endfor %}
```
____
### 2022 02 21 Итерация 9

#### Пакаджи     
:arrow_right: [da_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_sensors.yaml) - добавлены в recorder и customize датчик освещенности    

#### Интерфейс, в режиме yaml    
:arrow_right: [08_da_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/08_da_climate.yaml) - добавлен график по освещенности    
:arrow_right: [01_system.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/01_system.yaml) - для HACS сделана отдельная карта markdown, выводящая список и версии репозиториев для обновления    

```yaml
- type: markdown
  content: |
    <ha-icon icon="hacs:hacs"></ha-icon>&nbsp;&nbsp;&nbsp;Обновлений для HACS - {{ states('sensor.hacs') | default }}
    > {% for repo in state_attr('sensor.hacs', 'repositories') %}
    > {{ repo.display_name }} {{ repo["installed_version"] }} -> {{ repo["available_version"] }}
    > {% endfor %}
```
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0007.png)
____
### 2022 02 18 Итерация 8

#### Пакаджи    
:arrow_right: [system_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/system_sensors.yaml) - добавлены сенсоры даты и времени    
:arrow_right: [notification.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/notification.yaml) - тут будут уведомления, добавлено первое - отправляется в телеграмм группу при старте сервера, через минуту отправляет количество недоступных сущностей, по доменам    
:arrow_right: [dd_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_sensors.yaml) - по образу и подобию детской А - общие сущности для кейсов увлажения и отопления в детской Д    
:arrow_right: [dd_heat.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_heat.yaml) - перенесены общие сущности в пакадж сенсоров    

#### Интерфейс, в режиме yaml    
:arrow_right: [07_dd_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/07_dd_climate.yaml) - приведено в один формат с 07_dd_climate    
:arrow_right: [08_da_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/08_da_climate.yaml) - косметические изменения    

Так выглядит уведомление о запуске из пакаджа `notification.yaml`, бота зовут **Луиджи**    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0006.png)

____
### 2022 02 18 Итерация 7

#### Конфигурация    
:arrow_right: [configuration.yaml](https://github.com/kvazis/newHA/blob/master/configuration.yaml) - добавлен телеграмм бот    

#### Пакаджи     
:arrow_right: [control_mode.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/control_mode.yaml) - режим отопления убрал, решил делать отдельный для каждой комнаты    
:arrow_right: [dd_heat.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_heat.yaml) - добавлен MQTT переключатель режима отопления    
:arrow_right: [dd_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_light.yaml) - добавлено отключение всего освещение по нажатию на две клавиши выключателия Aqara    

Немного пересмотрел концепцию организацию сущностей. Так как некоторые датчики используюся в разных кейсах - например отопления, увлажнения, решил создать для них отдельный пакадж, где будут собраны общие объекты. Все что используется только в одном кейсе - собрано в один пакадж.    
:arrow_right: [da_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_sensors.yaml) - общие сущности для кейсов увлажения и отопления    
:arrow_right: [da_hum.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_hum.yaml) - управление увлажнителем воздуха через розетку с энергомониториноом, работает в заданное сенсором tod время, при закрытом окне. Контроль наличия воды по потреблению.    
:arrow_right: [da_heat.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_heat.yaml) - управление термоголовкой TV01    

#### Интерфейс, в режиме yaml    
:arrow_right: [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - корневой файл, в нем содержится общий заголовок и ссылки на файлы, каждый файл - отдельная страница    
:arrow_right: [02_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml) - убрал переключатель режима отопления    
:arrow_right: [07_dd_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/07_dd_climate.yaml) - добавил локальный переключатель режима отопления    
:arrow_right: [08_da_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/08_da_climate.yaml) - управление увлажнением и отоплением в одной из детских комнат    

Страница `08_da_climate.yaml` Вариант оформления страницы управления климатом    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0005.png)

____
### 2022 02 15 Итерация 6

#### Конфигурация    
:arrow_right: [configuration.yaml](https://github.com/kvazis/newHA/blob/master/configuration.yaml) - в white list добавлен доступ к папке config    
:arrow_right: [system_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/system_sensors.yaml) - исправление ошибок в разделе customize    

___
### 2022 02 15 Итерация 5

#### Пакаджи     
:arrow_right: [dd_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_light.yaml) - управление освещением, люстра Philips 620 (mihome) и zigbee лампа Aqara    
:arrow_right: [telemetry.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/telemetry.yaml) - добавлены сенсоры для термоголовок (climate), сенсоров и бинарных сенсоров    

#### Интерфейс, в режиме yaml    
:arrow_right: [02_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml) - аналогично добавление объекты climate, sensor, bimnary sensor + карта вывода батареек с уровнем заряда менее 30% с цветным оформлением карты battery-state-card    

Страница `02_control.yaml` Пример вывода в `auto-entities` c `battery-state-card` данных о разряженных батарейках    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0004.png)

___
### 2022 02 14 Итерация 4

#### Пакаджи     
:arrow_right: [telemetry.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/telemetry.yaml) - сенсоры определяющие общее количество объектов системе, активные, неактивные, недоcтупные, для доменов автоматизаций, скриптов, светильников и свичей    

#### Интерфейс, в режиме yaml    
:arrow_right: [01_system.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/01_system.yaml) - добавлен сенсор количества обновлений для HACS    
:arrow_right: [02_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml) - добавлена карты для пакаджа telemetry - для каждого домена вывод значений в [multiple-entity-row](https://youtu.be/m8WkJv7M9CY) и перечень недоступных объектов в [auto-entities](https://youtu.be/cxDDZkOl-EM)    

Страница `02_control.yaml` Пример вывода в auto-entities недоступного светильника    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0003.png)

___
### 2022 02 13 Итерация 3

#### Пакаджи     
:arrow_right: [control_mode.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/control_mode.yaml) - добавлен еще один шаблонный выключатель с хранением состояния в MQTT, для управлением режимом отопления    
:arrow_right: [dd_heat.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_heat.yaml) - управление термоголовкой TV01, описание в [видеоуроке](https://youtu.be/Y0bkyzhKHh8)    

#### Интерфейс, в режиме yaml    
:arrow_right: [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - корневой файл, в нем содержится общий заголовок и ссылки на файлы, каждый файл - отдельная страница    
:arrow_right: [02_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml) - заготовка под страницу телеметрии системы, добавлен переключатель режима отопления    
:arrow_right: [07_dd_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/07_dd_climate.yaml) - заготовка под страницу климат контроля одной из комнат, выведены параметры термостата из пакаджа dd_heat.yaml    

![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0002.png)

___
### 2022 02 13 Итерация 2

#### Интеграции
:arrow_right: Установлена [Xiaomi MIoT](https://github.com/ha0y/xiaomi_miot_raw)    

#### Пакаджи     
:arrow_right: [google_backup.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/google_backup.yaml) - шаблонные сеноры переписаны в modern style    

___
### 2022 02 13 Итерация 1

#### Платформа    
:ballot_box_with_check: Аппаратная часть - Raspberry Pi 4B 8GB + Argon One M.2 + SSD 128 GB    
:ballot_box_with_check: Операционная система - RaspiOS x64 Lite, Debian 11 Bullseye    
:ballot_box_with_check: Установленные пакеты - `jq` `wget` `curl` `udisks2` `apparmor-utils` `libglib2.0-bin` `network-manager dbus`    
:ballot_box_with_check: Дополнительно - `git` `mc` `argonone-config`    

#### Home Assistant:    
:arrow_right: Адд-оны - `File editor`, `Home Assistant Google Drive Backup`, `MariaDB`, `Mosquitto broker`, `Samba share`, 2 x `Zigbee2mqtt`    
:arrow_right: Интеграции - `HACS`, `MQTT`, `Raspberry Pi Power Supply Checker`, `Tuya`, `Version`, `Xiaomi Gateway 3`, `Xiaomi Miio`, `Yeelight`, `Локальный IP-адрес`    

#### Пакаджи     
:arrow_right: [control_mode.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/control_mode.yaml) - реализован шаблонный выключатель с хранением состояния в MQTT подробнее в статье [MQTT — хранение состояний режимов работы автоматизаций Home Assistant](https://github.com/kvazis/training/tree/master/lessons/articles/mqtt%20state), нужен для условий автоматизаций, используется при переключении управления с одного сервера на другой    
:arrow_right: [google_backup.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/google_backup.yaml) - созданы шаблонные сенсоры на основании значений атрибутов сенсора аддона Home Assistant Google Drive Backup    
:arrow_right: [system_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/system_sensors.yaml) - системные сенсоры для мониторинга системы    

#### Интерфейс, в режиме yaml    
:arrow_right: [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - корневой файл, в нем содержится общий заголовок и ссылки на файлы, каждый файл - отдельная страница    
:arrow_right: [01_system.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/01_system.yaml) - первая страница интерфейса с мониторингом системы и данными о установленных аддонах    

![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0001.png)

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