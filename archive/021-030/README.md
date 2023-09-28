### Архив, итерации - 21-30    
:leftwards_arrow_with_hook: [Вернуться в основной список](https://github.com/kvazis/newHA/blob/master/README.md)    

____
### 2022 07 02 Итерация 30    

:point_up: Много изменений, постарался максимально все охватить уроками на Youtube, поэтому долго не было обновлений.    
:point_up: По возможности добавляю комментарии ко всем измененным файлам, но много вызывано просто дообавлением описания в раздел кастомизации.    

#### Конфигурация    
:arrow_right: [configuration.yaml](https://github.com/kvazis/newHA/blob/master/configuration.yaml) - добавлены дополнительные ID чат телеграмм, мелкие несущественные изменения    

#### Пакаджи    

:arrow_right: [system_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/system_sensors.yaml) - сюда перенесены базовые настройки recorder, добавлен кастомный сенсор времени, обновляется раз в 30 сек, обновлен формат вывода сенсоров времени с последне загрузка НА и сервера. [Подробнее](https://youtu.be/O13Rbm_sdLE)    
:arrow_right: [telemetry.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/telemetry.yaml) - не влияющие на логику изменения в ходе тестирования.    
:arrow_right: [test.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/test.yaml) - небольшой испытательный полигон    
:arrow_right: [telegram_alarm.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Telegram/telegram_alarm.yaml) - пакадж аварийных уведомлений - [Телеметрия, часть 2. Аварийные уведомления](https://youtu.be/IKxOpfoptzg)    
:arrow_right: [telegram_telemetry.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Telegram/telegram_telemetry.yaml) - пакадж для мониторинга - [Телеметрия, часть 3. Мониторинг состояния системы в Telegram](https://youtu.be/EGxy2jm5Sb8)    
:arrow_right: [telegram_dialog.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Telegram/telegram_dialog.yaml) - стартовый диалог для меню управления - [Управление через Telegram, текстовые диалоги](https://youtu.be/gksZK58ZLDQ)    
:arrow_right: [telegram_control.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Telegram/telegram_control.yaml) - меню управления через телеграмм, изменения связанные с добавлением телеметри. [Управление умным домом через Telegram](https://youtu.be/tPYXpQwDLYc)    
:arrow_right: [boiler.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/boiler.yaml) - полностью переписан пакадж для бойлера, урока еще не не делал    
:arrow_right: [bt_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/bt_light.yaml) - не влияющие на логику изменения в ходе тестирования.    
:arrow_right: [bt_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/bt_switch.yaml) - замена розетки, в кастомизации прописана новая.    
:arrow_right: [bt_vent.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/bt_vent.yaml) - не влияющие на логику изменения в ходе тестирования.  
:arrow_right: [da_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_sensors.yaml) - добавлены описания сущностей    
:arrow_right: [da_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_switch.yaml) - добавлены описания сущностей    
:arrow_right: [dd_hum.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_hum.yaml) - оптимизация логики работы увлажнения воздуха    
:arrow_right: [en_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_EN/en_light.yaml) - добавлены описания сущностей    
:arrow_right: [en_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_EN/en_switch.yaml) - добавлены описания сущностей    
:arrow_right: [kn_alarm.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_alarm.yaml) - закомментировано, в виду внедрения общей автоматизации аварийных уведомлений    
:arrow_right: [kn_boiler.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_boiler.yaml) - новый пакадж для бойлера, урока еще не не делал    
:arrow_right: [kn_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_light.yaml) - добавлены описания сущностей    
:arrow_right: [kn_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_sensors.yaml) - добавлены описания сущностей    
:arrow_right: [kn_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_switch.yaml) - добавлены описания сущностей    
:arrow_right: [kn_tv_control.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_tv_control.yaml) - добавлена специфическая контрольная автоматизация    
:arrow_right: [ln_washmashine.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LN/ln_washmashine.yaml) - уведомление о завершении стирки    
:arrow_right: [lr_air_quality.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_air_quality.yaml) - небольшие изменения в логике (общее время для уведомлений)    
:arrow_right: [lr_balcony_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_balcony_light.yaml) - забыл при переносе про управлением светом на балконе, добавил    
:arrow_right: [lr_conditioner.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_conditioner.yaml) - Сделал "Ленивый кондиционер", чтобы не искать пульт     
:arrow_right: [lr_hum.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_hum.yaml) - пакадж управление увлажнителем Smartmi (мойка воздуха)    
:arrow_right: [lr_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_light.yaml) - добавлены описания сущностей    
:arrow_right: [lr_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_sensors.yaml) - добавлены описания сущностей    
:arrow_right: [lr_tv_control.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_tv_control.yaml) - добавлены описания сущностей  
:arrow_right: [tt_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_TT/tt_light.yaml) - создан [виртуальный светильник](https://youtu.be/hmimb2mvMMc) с логикой перехода на запасной в случае сбоя и параметрами включения от времени суток    

#### Интерфейс, в режиме yaml    
#### Много косметмических изменений    

____
### 2022 06 12 Итерация 29    

:point_up: Перед запуском зеркала - экспериментирую и оптимизирую пакаджи. 

#### Пакаджи    
:arrow_right: [ip_camera.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/ip_camera.yaml) - вывел еще одну камеру reolink в rtsp (параллельно с интеграцией Reolink) для отображение в интерфейсе [Home Habit](https://youtu.be/pQM16hcdcJs)    
:arrow_right: [cr_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_CR/cr_light.yaml) - добавлены описания сущностей    
:arrow_right: [da_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_sensors.yaml) - добавлены описания сущностей    
:arrow_right: [dd_light](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_light.yaml) - создан [виртуальный светильник](https://youtu.be/hmimb2mvMMc), для управления настольной лампой     
:arrow_right: [en_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_EN/en_light.yaml) - добавлена проверка доступности лампочкой    
:arrow_right: [kn_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_light.yaml) - для вывода в интерфейс, создан [виртуальный светильник](https://youtu.be/hmimb2mvMMc)    
:arrow_right: [lr_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_light.yaml) - для вывода в интерфейс, созданы [виртуальные светильники](https://youtu.be/hmimb2mvMMc)    
:arrow_right: [lr_light_cinema](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_light_cinema.yaml) - подсветка для кино, переписана через [виртуальный светильник](https://youtu.be/hmimb2mvMMc)    
:arrow_right: [tt_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_TT/tt_light.yaml) - добавлены условия для параметров автовыключения в зависимости от времени суток....
:arrow_right: [dd_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_sensors.yaml) - добавлены описания сущностей    
:arrow_right: [dd_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_switch.yaml) - добавлены описания сущностей    

#### Интерфейс, в режиме yaml    
:arrow_right: [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлена тестовая страница     
:arrow_right: [test.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/test.yaml) - страница для экспериментов    

Интерфейс Home Habit на планшете    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0017.png)
____
### 2022 06 05 Итерация 28

:point_up: Большое обновление, наконец перенесены все устройства и все автоматизации, старые сервера отключены.

#### Конфигурация    
:arrow_right: [configuration.yaml](https://github.com/kvazis/newHA/blob/master/configuration.yaml) - добавлен дополнительные адресат в Телеграмм

#### Пакаджи    
:arrow_right: [alarm.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/alarm.yaml) - добавлен еще один светильник к индикации    
:arrow_right: [entity_reboot.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/entity_reboot.yaml) - добавлена тестовая автоматизация для перезагрузки шлюза Mi    
:arrow_right: [dd_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_sensors.yaml) - добавлены описания сущностей    
:arrow_right: [dd_telegram_control.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_telegram_control.yaml) - отдельное меню управления комнатой в телеграмм, подробнее в уроке [Управление через Telegram, текстовые диалоги, права пользователей](https://youtu.be/gksZK58ZLDQ)    
:arrow_right: [dd_telegram_wled.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_telegram_wled.yaml) - управление адресной лентой через телеграмм подробнее в уроке [Управляем адресным светильником WLED через меню в Telegram](https://youtu.be/KqjjBY3QaCg)    
:arrow_right: [en_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_EN/en_light.yaml) - управление лампочкой в прихожей    
:arrow_right: [kn_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_light.yaml) - незначительные изменения, добавлен еще один триггер    
:arrow_right: [kn_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_sensors.yaml) - добавлены описания сущностей    
:arrow_right: [kn_tv_control.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_sensors.yaml) - добавлена контрольная автоматизация следящая за включением ТВ     
:arrow_right: [ln_alarm.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LN/ln_alarm.yaml) - тревога по срабатыванию датчика протечки в прачечной    
:arrow_right: [ln_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LN/ln_light.yaml) - управление светом в прачечной    
:arrow_right: [ln_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LN/ln_sensors.yaml) - добавлены описания сущностей    
:arrow_right: [ln_washmashine.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LN/ln_washmashine.yaml) - Напоминание в телеграмм о завершении стирки    
:arrow_right: [lr_fan_router.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_fan_router.yaml) - управление охлаждающей подставкой для роутера    
:arrow_right: [lr_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_sensors.yaml) - добавлены описания сущностей    
:arrow_right: [lr_telegram_wled.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_telegram_wled.yaml) - управление адресным светильником через телеграмм подробнее в уроке [Управляем адресным светильником WLED через меню в Telegram](https://youtu.be/KqjjBY3QaCg)    
:arrow_right: [tt_alarm.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_TT/tt_alarm.yaml) - тревога по срабатыванию датчика протечки в туалете    
:arrow_right: [tt_sensor.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_TT/tt_sensor.yaml) - добавлены описания сущностей    
:arrow_right: [tt_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_TT/tt_light.yaml) - управление светом в туалете    

#### Интерфейс, в режиме yaml    
:arrow_right: [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлена объединенная страницы для туалета и прачечной     
#### Много изменений связанный с приведением страниц в единый формат тображения данных     
____
### 2022 05 25 Итерация 27

#### Пакаджи    
:arrow_right: [telegram_control.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Telegram/telegram_control.yaml) - интерфейс управления через телеграм, подробнее в  [Уроке Home Assistant - Управление умным домом через Telegram из любой точки мира](https://youtu.be/tPYXpQwDLYc)    
:arrow_right: [kn_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_light.yaml) - добавлена автоматизация, которая включает основное освещение, если в кухне кто-то есть более 15 минут    

```yaml

    template:

      - binary_sensor:

    # Сенсор определяющий длительную работу дежурного освещения
          - name: kn_ceiling_auto_long
            state: >
              {{ is_state('binary_sensor.kn_occupancy', 'on')  
                 and is_state('input_boolean.kn_ceiling_light', 'off')
                 and is_state('light.kn_ceiling_light', 'on')
              }}
            delay_on: 
                minutes: 15
            device_class: light
            icon: >
              {% if is_state("binary_sensor.kn_ceiling_auto_long", "on") %}
              mdi:lightbulb-on
              {% else %}
              mdi:dome-light
              {% endif %}
              
    automation:

      - id: Кухня, переключение на основное освещение
        alias: kn_ceiling_auto_long
        description: Если дежурный свет включен более 15 минут, переход на основное освещение
        initial_state: true
        trigger:
    # Кто-то есть в кухнее более 15 минут
        - platform: state
          entity_id: binary_sensor.kn_ceiling_auto_long
          to: 'on'
        condition:
    # Переключатель режима работы сервера
        - condition: state
          entity_id: switch.control_mode
          state: 'on'
        action:
    # Включение переключателя ручного управления
        - service: input_boolean.turn_on
          target:
            entity_id: input_boolean.kn_ceiling_light 
```

Ряд несущественных изменений, связанных с добавлением в триггеры автоматизаций input_button - для возможности их запуска из интерфейса телеграм
____
### 2022 05 19 Итерация 26

#### Конфигурация    
:arrow_right: [configuration.yaml](https://github.com/kvazis/newHA/blob/master/configuration.yaml) - добавлен ИК контроллер Xiaomi (через UI пока добавить нельзя)    

#### Пакаджи    
:arrow_right: [alarm.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/alarm.yaml) - световая индикация при возникновении тревоги на основе [Ukraine Alarm](https://github.com/home-assistant/core/tree/dev/homeassistant/components/ukraine_alarm), подробнее в [Блоге](https://youtu.be/c1qgFBEk4xs)    
:arrow_right: [ip_camera.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/ip_camera.yaml) - незначительные изменения    
:arrow_right: [cr_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_CR/cr_light.yaml) - добавлена еще одна точка управления светом    
:arrow_right: [kn_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_light.yaml) - управление светом в кухне, подробнее в [Блоге](https://youtu.be/Jog7RV3Wqfk)    
:arrow_right: [kn_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_sensors.yaml) - незначительные добавления описаний сенсоров    
:arrow_right: [kn_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_switch.yaml) - описание розеток на кухне    
:arrow_right: [kn_tv_control.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_tv_control.yaml) - пакадж управления телевизором на кухне, логика аналогична как в [Блоге](https://youtu.be/R2jMUh-5PCE) только используется ИК контроллер Xiaomi    

### 2022 05 15 Итерация 25

Изменен формат файлов описаний `README.md` - на мой взгляд так более удобочитабельнее    

#### Интеграции
:arrow_right: Установлена [Reverso TTS / tts](https://github.com/rt400/ReversoTTS-HA)    
:arrow_right: Установлена [Ukraine Alarm](https://github.com/home-assistant/core/tree/dev/homeassistant/components/ukraine_alarm)    

#### Конфигурация    
:arrow_right: [configuration.yaml](https://github.com/kvazis/newHA/blob/master/configuration.yaml) - добавлен reversotts подробнее в [Блог. Home Assistant - Text to speech, озвучка уведомлений, Reverso TTS](https://youtu.be/bDdn7lRqAko)    

#### Пакаджи    
:arrow_right: [entity_reboot.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/entity_reboot.yaml) - продолжаются тесты, поэтому файл меняется    
:arrow_right: [da_hum.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_hum.yaml) - доработка автоматизации увлажнения, чтобы не было лишних срабатываний    
:arrow_right: [dd_hum.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_hum.yaml) - доработка автоматизации увлажнения, чтобы не было лишних срабатываний    
:arrow_right: [telemetry.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/telemetry.yaml) - проверял некоторые идеи, но в результате они не прижились, файл менялся, но по сути изменений нет    
  
#### Интерфейс, в режиме yaml    
Много косметических, незначительных изменений    
:arrow_right: [02_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml) - страница телеметрии, добавлен раздел для медиа плееров, что сейчас играет    
:arrow_right: [05_lr_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/05_lr_control.yaml) - тут также выведены карточки медиа плееров, см. скриншот    

Страница `05_lr_control.yaml`    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0016.png)

____
### 2022 05 08 Итерация 24

#### Конфигурация    
:arrow_right: [configuration.yaml](https://github.com/kvazis/newHA/blob/master/configuration.yaml) - закомментирован раздел updater - интеграция выпадала в ошибку    

#### Пакаджи    
:arrow_right: [entity_reboot.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/entity_reboot.yaml) - здесь будут собираться автоматизации по перезагрузке отдельных устройств, склонных к произвольному отключению    
:arrow_right: [telemetry.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/telemetry.yaml) - добавлены сенсоры для обновлений, подробнее в [Уроки Home Assistant - Телеметрия, часть 1. Отслеживание состояний в режиме онлайн](https://youtu.be/VuRrD-YYV70)    
:arrow_right: [bt_alarm.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/bt_alarm.yaml) - добавлены описания сенсоров    
:arrow_right: [dd_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_sensors.yaml) - добавлены описания сенсоров    
:arrow_right: [kn_alarm.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_alarm.yaml) - пакадж уведомлений при срабатывания датчика дыма и протечки в кухне    
:arrow_right: [kn_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_light.yaml) - пакадж, заготовка под управление освещением в кухне    
:arrow_right: [kn_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_sensors.yaml) - добавлены описания сенсоров    

###### Интерфейс, в режиме yaml        
Много косметических, незначительных изменений    
:arrow_right: [02_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml) - страница телеметрии, добавлен раздел для обновлений    

Страница `02_control.yaml`    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0015.png)

____
### 2022 05 05 Итерация 23

#### Интеграции
:arrow_right: Установлена [Reolink IP camera](https://github.com/fwestenberg/reolink_dev)    

#### Пакаджи    
:arrow_right: [ip_camera.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/ip_camera.yaml) - перенос камер на платформе generic в UI    
:arrow_right: [cr_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_CR/cr_light.yaml) - ручное управление освещением в коридоре    
:arrow_right: [cr_sensor.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_CR/cr_sensor.yaml) - описание сенсоров в коридоре    
:arrow_right: [en_camera.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_EN/en_camera.yaml) - несущественные изменения    
:arrow_right: [en_sensor.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_EN/en_sensor.yaml) - описание сенсоров в прихожей    
:arrow_right: [en_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_EN/en_switch.yaml) - описание свичей в прихожей    
:arrow_right: [system_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/system_sensors.yaml) - перенос сенсора filesize для home-assistant_v2.db в UI    
:arrow_right: [telemetry.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/telemetry.yaml) - добaвлен подсчет общего числа и недоступных камер    

#### Интерфейс, в режиме yaml    
* [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлена страница для коридора    
* [02_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml) - страница телеметрии, добавлен раздел для камер - всего и недоступно    
* [03_cr_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/03_cr_control.yaml) - страница управления сущностями в коридоре    

Страница `03_cr_control.yaml`    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0014a.png)

____
### 2022 04 26 Итерация 22

#### Пакаджи    
:arrow_right: [ip_camera.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/ip_camera.yaml) - добавлены IP камеры    
:arrow_right: [en_camera.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_EN/en_camera.yaml) - пакадж отправки уведомлений и фото при открытии входной двери в [блоге](https://youtu.be/YxzUqcTerSE)    

#### Интерфейс, в режиме yaml    
:arrow_right: [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлена страница для прихожей    
:arrow_right: [04_kn_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/01_en_control.yaml) - страница для прихожей и камеры на этаже, карточки для камер показаны в [блоге](https://youtu.be/YxzUqcTerSE)    

Страница `01_en_control.yaml`    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0014.png)

____
### 2022 04 14 Итерация 21

#### Пакаджи    
:arrow_right: [lr_tv_control.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_tv_control.yaml) - управление телевизором через ИК базу Broadlink кнопок подробнее в [блоге](https://youtu.be/R2jMUh-5PCE)    

#### Интерфейс, в режиме yaml    
Добавление новых элементов на страницы комнат, ключевых изменений нет    

____
#### Поддержать развитие проекта *Умный дом с Alex Kvazis*    
<a href="https://www.youtube.com/channel/UCcq9onYHbs6go3kDpfBoqhg/join" target="_blank"><img src="https://raw.githubusercontent.com/kvazis/training/master/lessons/img/youtube.png" alt="Youtube Sponsorship" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>
<a href="https://www.patreon.com/alex_kvazis" target="_blank"><img src="https://raw.githubusercontent.com/kvazis/training/master/lessons/img/patreon-button.png" alt="Patreon Support" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>
<a href="https://www.buymeacoffee.com/greatkvazis" target="_blank"><img src="https://raw.githubusercontent.com/kvazis/training/master/lessons/img/buymeacoffee.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>
<a href="https://www.paypal.com/paypalme/greatkvazis" target="_blank"><img src="https://raw.githubusercontent.com/kvazis/training/master/lessons/img/paypal.png" alt="PayPal Me" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>

#### Или перевод любой суммы на -     
* Webmoney - Z243592584952
* BTC - 1Gzr7WQugfnPuWVawu47EiCMTDUBqCAshj
* ETH - 0xa0ce3E29Cf537013649Ae9cdbc08C4853fF91FAc
* LTC - ltc1qs493yk2wk9ywx5h6aruk4p9zm75hx42ekv4ym2
* TRX - TFTCLqvS1tMBwokRHBwz1TCDJ4oD1Z5zPk

