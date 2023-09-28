<a href="https://www.youtube.com/channel/UCcq9onYHbs6go3kDpfBoqhg?sub_confirmation=1" target="_blank"><img src="https://raw.githubusercontent.com/kvazis/training/master/lessons/img/subscribe.png" alt="Subscribe" style="height: 71px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>


### 2023 06 25 Итерация 36


#### Пакаджи    
:point_up: Давно не обновлялся, изменений за это время было довольно много, постараюсь ничего не упустить, незначительные и несущественные правки упоминать не буду    
:arrow_right: [configuration.yaml](https://github.com/kvazis/newHA/blob/master/configuration.yaml) - добавил несколько новых карт в интерфейс     
:arrow_right: [telemetry.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/telemetry.yaml) - часть сенсоров суммирующих потребление перенес в папки по комнатам    
:arrow_right: [test.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/test.yaml) - возникают вопросы по этому пакаджу - он нужен только для тестов    
:arrow_right: [bluetooth.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Control/bluetooth.yaml) - перезагрузка BT адаптера    
:arrow_right: [electricity.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Control/electricity.yaml) - для повышения надежности сделал второй физический сенсор электрики, логический сработает при включении обоих    
:arrow_right: [event_camera.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Outdoor/event_camera.yaml) - вывод изображения с камеры в коридоре на гугл экран по нажатию кнопки или движению в дневное время    
:arrow_right: [out_camera.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Outdoor/out_camera.yaml) - добавлены триггеры для вывода картинки с уличных камер на экран по кнопкам Aqara Opple    
:arrow_right: [da_wled_control.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_wled_control.yaml) - запуск эффектов на WLED по нажатию на кнопки    
:arrow_right: [da_fan_router.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_fan_router.yaml) - управление охлаждающей подставкой второго роутера    
:arrow_right: [lr_ups_1.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_ups_1.yaml) - логика работы бесперебойника [часть 1](https://youtu.be/SAfi_6aKyfE), [часть 2](https://youtu.be/7ekRAkPX7PQ)    
:arrow_right: [lr_wled_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_wled_light.yaml) - управление и события для [WLED светильника](https://youtu.be/CdS8M7rJumI)    
:arrow_right: [tt_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_TT/tt_light.yaml) - реализация аварийного освещения [видео урок](https://youtu.be/_DwgWu9SBso)    


#### Интерфейс, в режиме yaml    
:point_up: Косметические изменения в интерфейсе    

____

### 2023 03 02 Итерация 35


#### Пакаджи    
:point_up: Большая часть изменений - не влияют на логику работы, например перенос template сенсоров мощности из общего пакаджи - в отдельные пакаджи по комнатам, переименование объектов    
:arrow_right: [blackout.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Control/blackout.yaml) - автоматизация действий при отключении и включении электрики    
:arrow_right: [electricity.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Control/electricity.yaml) - уведомления в телеграмм при отключении и включении электрики    


#### Интерфейс, в режиме yaml    
:point_up: Косметические изменения в интерфейсе    

____

### 2022 12 30 Итерация 34

:point_up: Давно не обновлял, но каких либо существенных изменений не было, в основном мелкие доработки    
:arrow_right: [configuration.yaml](https://github.com/kvazis/newHA/blob/master/configuration.yaml) - добавлена страна, строка 4    

#### Пакаджи    
:point_up: Изменений много, но в основном несущественные правки (кастомизация и иконки) из нового -     
:arrow_right: [reminder.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Calendar/reminder.yaml) - напоминалка по сработке [событий из календаря](https://youtu.be/nLNq187Fcps)    
:arrow_right: [blackout.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Control/blackout.yaml) - мой вариант автоматического отключения сервера при отсутствии электрики    
:arrow_right: [zigbee2mqtt.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Control/zigbee2mqtt.yaml) - автоматизация для включения zigbee2mqtt, который автоматически выключается в случае отключения резервного сервера    


#### Интерфейс, в режиме yaml    
:point_up: Косметические изменения в интерфейсе    
:arrow_right: [ui_graph.yaml](https://github.com/kvazis/newHA/blob/master/ui_graph.yaml) - добавил страницы-графики по мониторингу. 

____


### 2022 09 24 Итерация 33

:point_up: Практически все изменения в пакаджах - конснулись наименований автоматизаций для приведения их к единому шаблону    
:point_up: Существенно переделан интерфейс - добавлено много Mushroom карточек - з [Репозиторий](https://github.com/piitaya/lovelace-mushroom)  - есть в HACS    

:point_up: Увидеть как выглядит измененный интерфейс можно тут - [Блог Home Assistant - демонстрация интерфейса на 23.09.2022](https://youtu.be/isd66esUA5Y)    

____
### 2022 09 04 Итерация 32   

:point_up: Основной сервер перехал с Raspberry 4B 8GB на Beelink GK mini, на Debian 11 [Beelink GK Mini часть 2 - Autoboot, Debian 11, Supervised Home Assistant](https://youtu.be/RqW5q-0RYio)    
:point_up: Большая часть изменений касается интерфейса - переделал нумерацию файлов страниц, затем вынес все графики на отдельный дашборд, после чего занялся оптимизацией - в основном за счет использования карт mushroom     

#### Home Assistant:    
:arrow_right: Интеграции - Убрана -  `Raspberry Pi Power Supply Checker`, Добавлена `ASUS Router`    
:arrow_right: Добавлен аккаунт Nabu Casa, синхронизировано с Google Home    

#### Конфигурация    
:arrow_right: [configuration.yaml](https://github.com/kvazis/newHA/blob/master/configuration.yaml) - добавлен дашбоард `lovelace-graph`, кнопка на панели на `hassio/system`, прописана карта `mushroom.js`    

#### Пакаджи    
:arrow_right: [asus_router.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/asus_router.yaml) - описания сенсоров интеграции Asus Router    
:arrow_right: [telemetry.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/telemetry.yaml) - добавлены сенсоры общего энергопотребления и потребления по комнатам, рассказывал про это тут - [Home Assistant. Урок 12.3 Интерфейс - Lovelace, карта Sankey Chart Card](https://youtu.be/OxJKOp0i3hg)    
:arrow_right: [test.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/test.yaml) - это экспериментальный пакадж для опытов    
:arrow_right: [out_camera.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Outdoor/out_camera.yaml) - пакадж для снятия фото и отправки потока с камер на google nest    
#### Несущественные правки описание устройств и исправление ошибок   

#### Интерфейс, в режиме yaml    
:arrow_right: [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - переделана нумерация страниц, но будет еще одна переделка после оптимизации    
:arrow_right: [ui_graph.yaml](https://github.com/kvazis/newHA/blob/master/ui_graph.yaml) - перечень страниц нового дашборда    
#### Изменения затронули все файлы страниц    
____
### 2022 07 23 Итерация 31    

:point_up: Конфигурация уже полностью рабочая, поэтому основная часть изменений по сути косметических, например прописывание в рекордер, устранение мелких ошибок, поэтому начиная с этой итерации буду описывать только самое основное.    

#### Конфигурация    
:arrow_right: [configuration.yaml](https://github.com/kvazis/newHA/blob/master/configuration.yaml) - добавлен `auth_providers` для работы Restful сенсоров [Rest sensor, взаимодействие основного и резервного серверов автоматизаций.](https://youtu.be/1KTHQkkGJeU)    

#### Пакаджи    
:arrow_right: [control_mode.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/control_mode.yaml) - изменен формат mqtt сенсора на новый (логика осталась)    
:arrow_right: [system_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/system_sensors.yaml) - изменен формат вывода сенсоров времени с последней перезагрузки, он стал компактнее     
:arrow_right: [test.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/test.yaml) - это экспериментальный пакадж для опытов, будет менятся постоянно    
:arrow_right: [rest_control.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Rest/rest_control.yaml) - пакадж автоматизаций передачи управления [Rest sensor, взаимодействие основного и резервного серверов автоматизаций.](https://youtu.be/1KTHQkkGJeU)    
:arrow_right: [boiler.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/boiler.yaml) - бойлер ванная, 2 периода включения, изменен формат mqtt сенсора на новый, добавлена синхронизация [Автоматизация работы бойлера, передача параметров на резервный сервер](https://youtu.be/3yAJ-4mT5vk)    
:arrow_right: [kn_boiler.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_boiler.yaml) - бойлер кухня, 3 периода включения, изменен формат mqtt сенсора на новый, добавлена синхронизация [Автоматизация работы бойлера, передача параметров на резервный сервер](https://youtu.be/3yAJ-4mT5vk)    


#### Интерфейс, в режиме yaml    
#### Много косметических изменений, есть интересная карта истории, планирую снять урок    

____
### Для удобства, чтобы не перегружать файл, старые итерации переносятся в архив    
:arrow_right_hook: [Архив 001-010](https://github.com/kvazis/newHA/blob/master/archive/001-010/README.md)    
:arrow_right_hook: [Архив 011-020](https://github.com/kvazis/newHA/blob/master/archive/011-020/README.md)    
:arrow_right_hook: [Архив 021-030](https://github.com/kvazis/newHA/blob/master/archive/021-030/README.md)    

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