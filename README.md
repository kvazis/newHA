<a href="https://www.youtube.com/channel/UCcq9onYHbs6go3kDpfBoqhg?sub_confirmation=1" target="_blank"><img src="https://raw.githubusercontent.com/kvazis/training/master/lessons/img/subscribe.png" alt="Subscribe" style="height: 71px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>

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
#### Много косметмических изменений, есть интересная карта истории, планирую снять урок    

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