<!-- Global site tag (gtag.js) - Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=UA-142612198-1"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'UA-142612198-1');
</script>

  

# All IPTV
<img src="./logo.png" width="256" height="256">

# [EN]

[Download latest version](https://github.com/Slev7nm/all-iptv-dune-plugin/releases/latest)

All IPTV is a program for converting m3u / m3u8 playlists of any iptv provider into a plugin for viewing iptv on Dune HD Players.
We do not provide a plugin for a particular provider - you build it yourself!

## Main features

- Categories with icons
- Selection of channel icons
- Selection of channel schedules from http://www.vsetv.com/ and https://teleguide.info/
- Archives for verified providers
- MultiPlaylist
- Update Plugin Platlists Via PC On Local Network

## How to use

Just drag the m3u / m3u8 playlist from any folder onto the application icon.

Also The Software supports the conversion of multiple playlists in one plugin.

Demo Video

[![DEMO](http://img.youtube.com/vi/bny51TSvB7s/0.jpg)](https://www.youtube.com/watch?v=bny51TSvB7s)


Option to switch playlists in the generated plugin on the settings page

## Working With The Software

If your provider provides the ability to download playlist channels in the formats m3u/m3u8, then with the help of this converter you can turn it into a plugin for Dune HD with your own hands. We tried to reduce the number of settings to a minimum and reduce the conversion process to a few clicks and the plugin is ready to installation.

No services! No paid subscriptions! No restrictions - download the program only once and Convert as much as you want.
During processing, the program will intellectually try to find icons, a schedule, and archives to the list of channels from m3u playlist that you choose to convert.

Unfortunately, the m3u contains only information about groups and channel names, and the channel names themselves are named in any form (often also with typos), that is why a small part of the channels may not be converted in the generated plug-in. In this case, you can watch them, but without additional features. If you have a lot of patience, then you can correct this moment by manually writing configs for them.

## List of verified providers

- [itv.live](https://itv.live/) (supported playlists halvatv.m3u8, logom3u.m3u8, progdvb.m3u, ssiptv.m3u8, hls.m3u8, mpegs.m3u, perfectpl.m3u8, siptv.m3u; partial supported playlist ottplayeres.m3u8)
- [greatiptv.cc](https://bill.greatiptv.cc/) (you can get a working playlist at t.greatiptv.cc/pl/{your token}/playlist.m3u; playlists from account will not work)  
- [shura.tv](https://shura.tv/)
- [ottclub.cc](https://www.ottclub.cc/go/id/6698/)
- [cbilling.tv](https://cbilling.tv/?mode=signup&referral_id=564979/)
- [edem.tv](https://edem.tv/welcome/register/2e46753ef3a66656/)
- [tvclub.cc](https://tvclub.cc/)
- [shara-tv.org](https://shara-tv.org/)
- [schuriktv.nethouse.ru](https://schuriktv.nethouse.ru/) (supported playlists "Playlist M3U", "SIP Player M3U", "SIP Player M3U8")
- [tv.team](http://tv.team/) (supported playlists "HLS", "HLS + archives", "Halva TV", "MPEG-TS")
- [sharavoz.tv](https://www.sharavoz.tv/Account/Register?hash=_u5B0EY6S7sioGIS9XzyGaskFDu4NP48n9jhZlRBXDw=/) (channel list with archives support see in your account)
- [kingmodiptv.top](http://kingmodiptv.top/) (supported playlists tv.m3u) 
- [global-iptv.net](http://global-iptv.net/) (supported playlists tv.m3u)
- [ontv.pro](https://bill.ontv.pro/account/register?ref=1627&c=1667)


## List of verified providers (without archives)

- [ip-tv.club](https://ip-tv.club/partner/10437/) 
- [fox-tv.fun](http://shop.fox-tv.fun/) ("M3U Plus" playlist recommended)
- [tvoetv.in.ua](https://tvoetv.in.ua/)
- [strah.tv](http://strah.tv/7004534/) (it is recommended to enable the option "MPEG-2 TS" before downloading a playlist)
- [my.1ott.net](http://my.1ott.net/) ("ottnavm3u8.m3u8" playlist recommended)
- [shara.club](https://www.shara.club/reg-205521.html/)
- [voron.info](http://voron.info/)
- [sovok.tv](http://sovok.tv/register/?ruser=26692/) (required to enable "Группировать по категориям" -> "Спец полями" before downloading a playlist)
- [ottglanz.tv](http://ottglanz.tv/partner/slev7n/) recommended HLS playlist 220+ channels.the HLS playlist 450+ is currently in the work on the server side

## Adding custom icons, groups, and more

You can change the parameters of channels and icons of standard groups.

When converting, the exclusions.xml and conf.yaml files in the program root are taken into program priority, as well as the files <m3u name>.conf.yaml and <m3u name>.exclusions.yaml, which are located next to the m3u playlist. Configs next to m3u have higher priority. Thus, you have the ability to configure part of the parameters equally for all m3u, and some providers of m3u individually.

Examples of settings are in the examples folder.

### Setting Up Groups

The conf.yaml file contains a list of channel groups and icons for them in yaml format.
```yaml
'name of the group from m3u':'icon'
```
The icon can be a local or relative path or http(s) address (during the conversion, such images will be downloaded).

For convenience, you can use the online editor with checking yaml syntax https://onlineyamltools.com/edit-yaml

It is not recommended to change the standard icons in the icons directory, as they will be reset when the program is updated.

### Customize Channels 

The exclusions.xml file allows you to customize icons and channel schedules.
```xml
<?xml version="1.0" encoding="utf-8" ?>
<tv_info>
  <tv_channels>
    <tv_channel>
      <caption>name of the channel from m3u m3u</caption>
      <epg_id>id from vsetv.com</epg_id>
      <tvg_id>id from teleguide.info</tvg_id>
      <icon_url>icon</icon_url>
    </tv_channel>
    <tv_channel>
      <caption>name of the channel from m3u m3u</caption>
      <epg_id>id from vsetv.com</epg_id>
      <tvg_id>id from teleguide.info</tvg_id>
      <icon_url>icon</icon_url>
    </tv_channel>
    <!-- и т.д ... -->
  </tv_channels>
</tv_info>
```
Id from vsetv.com can be found from the channel url type http://www.vsetv.com/schedule_channel_1071_day_2019-04-04.html The number between channel_ and _day is id (1071).

Id from teleguide.info find out from the url of the channel like https://www.teleguide.info/kanal1006_20190326.html The number between kanal and _ is id (1006).

The icon can be a local absolute or relative path or http(s) address (during the conversion, such images will be downloaded).

### Main application icon

Like setting up group icons in conf.yaml, add a line or change an existing one.
```yaml
_:'icon'
```

## Questions and answers

> Archives do not work.

There are a lot of providers, they appear and disappear. At the same time, there is no single standard for specifying the syntax of archives via the m3u playlist. Each provider provides them as they feel needed to. We have added and tested the most popular providers in our opinion.

If your provider is not in the list of supported, then write to us in the telegram group [@all_iptv_dune_plugin](https://taraflex.github.io/tg/#https://t.me/all_iptv_dune_plugin) or in [issues](https://github.com/Slev7nm/all-iptv-dune-plugin/issues) - we will add it.

> Configs inconvenient to edit. Can you do something about it?

Maybe someday we will add a constructor instead of config files to the gui application, but probably not very soon.

> Do you plan to open the source of the application?

Not yet. They are fast coded and not commented , We are ashamed of the source code. the source of php plugin can be viewed by unpacking the generated zip archive.

> Your standard pictures for channel groups are terrible.

We do not mind if someone draws them more decently or offers alternative options with a free license.

> My iptv provider does not provide m3u. Can I still use your program somehow?

Write us in the telegram group [@all_iptv_dune_plugin](https://taraflex.github.io/tg/#https://t.me/all_iptv_dune_plugin) or in [issues](https://github.com/Slev7nm/all-iptv-dune-plugin/issues). We will consider the possibility of adding additional formats to the parser.

> I want to help in the development! How?

We also want to help us! Right now, we need a designer to draw application icons and channel groups. Write to the telegram group [@all_iptv_dune_plugin](https://taraflex.github.io/tg/#https://t.me/all_iptv_dune_plugin) or to [issues](https://github.com/Slev7nm/all-iptv-dune-plugin/issues). 
Well, of course, you can also help with finances.

[<img src="https://az743702.vo.msecnd.net/cdn/kofi5.png?v=2" width="202" alt="https://ko-fi.com/alliptv"/>](https://ko-fi.com/alliptv)

> Why does the program need access to the network?

To download the unrecognizable icons list of channels from vsetv.com and teleguide.info and channel icons, to well as to check for updates and also to send erorrs if there were in proccess of convertion

The program comes with a certain set of icons, but it is not always enough.

You can view with the sniffer that no additional data is transmitted.

> I do not want to send anything anywhere! Can you turn off your godless telemetry?

Yes. Simply create the notelemetry.txt file in the application directory. Remember that the collected error statistics helps to improve the 
algorithms for selecting icons and channel schedules.

> So the access tokens in my playlists are safe?
   
Yes

> Nothing works! You are the hands!

Well... nothing working at all... probably...

The world is ruled by money! So If You Left Handed Hands This can be compensated by the involvement of additional developers, with two normal working hands.

[<img src="https://az743702.vo.msecnd.net/cdn/kofi5.png?v=2" width="202" alt="https://ko-fi.com/alliptv"/>](https://ko-fi.com/alliptv)

> I want more features! Why are you so slow?

¯\\_(ツ)_/¯

# [RU]

[Скачать последнюю версию](https://github.com/Slev7nm/all-iptv-dune-plugin/releases/latest)

All IPTV - программа для конвертации m3u/m3u8 плейлиста любого iptv провайдера в плагин для просмотра iptv на приставках Dune HD.
Мы не предоставляем плагин под какого-то конкретного провайдера - вы собираете его сами!

## Основные возможности

- Категории с иконками
- Подбор иконок каналов
- Подбор расписания каналов с http://www.vsetv.com/ и https://teleguide.info/
- Архивы для [проверенных провайдеров](#cписок-проверенных-провайдеров) 
- Мультиплейлист
- обновление плагина и плейлистов через пк по локалнои сети

## Как использовать

Просто перетащите m3u/m3u8 плейлист из любой папки на иконку приложения.

Также поддерживается конвертация нескольких плейлистов в один плагин.

демо видео

[![DEMO](http://img.youtube.com/vi/bny51TSvB7s/0.jpg)](https://www.youtube.com/watch?v=bny51TSvB7s)

Переключать плейлисты в сгенерированном плагине вы сможете на странице настроек. 

## Принцип работы

Если ваш провайдер предоставляет возможность скачать плейлист каналов в форматах m3u/m3u8, то с помощью данного конвертера можно превратить его в плагин для Dune HD своими руками. Мы постарались свести число настроек к минимуму и свести процесс конвертации к нескольким нажатиям на enter.

Никаких сервисов! Никаких платных подписок! Никаких ограничений - качаем программу лишь раз и обрабатываем хоть тысячу плейлистов. 
В процессе обработки программа будет пытаться интелектуально подобрать иконки, расписание, и архивы к списку каналов из вашего m3u плейлиста.

К сожалению в m3u содержится лишь информация о группах и названиях каналов, а сами названия каналов записано в какой угодно форме (зачастую еще и с опечатками), поэтому в сгенерированном плагине существенная часть каналов может не определится. При этом вы сможете их просматривать, но без дополнительных возможностей. Если у вас много терпения, то вы можете исправить этот момент ручным написанием конфигов под них.

## Список проверенных провайдеров

- [itv.live](https://itv.live/) (поддерживаемые плейлисты halvatv.m3u8, logom3u.m3u8, progdvb.m3u, ssiptv.m3u8, hls.m3u8, mpegs.m3u, perfectpl.m3u8, siptv.m3u; чуть менее подходит ottplayeres.m3u8)
- [greatiptv.cc](https://greatiptv.cc/) (получить рабочий плейлист можно по адресу t.greatiptv.cc/pl/{ваш токен}/playlist.m3u; плейлисты из личного кабинета работать не будут)  
- [shura.tv](https://shura.tv/) 
- [ottclub.cc](https://www.ottclub.cc/go/id/6698/) 
- [cbilling.tv](https://cbilling.tv/?mode=signup&referral_id=564979/) 
- [edem.tv](https://edem.tv/welcome/register/2e46753ef3a66656/) 
- [tvclub.cc](https://tvclub.cc/)
- [shara-tv.org](https://shara-tv.org/)
- [schuriktv.nethouse.ru](https://schuriktv.nethouse.ru/) (поддерживаемые плейлисты "Playlist M3U", "SIP Player M3U", "SIP Player M3U8")
- [tv.team](http://tv.team/) (поддерживаемые плейлисты "HLS", "HLS + архивы", "Halva TV", "MPEG-TS")
- [sharavoz.tv](https://www.sharavoz.tv/Account/Register?hash=_u5B0EY6S7sioGIS9XzyGaskFDu4NP48n9jhZlRBXDw=/) (список каналов с архивами смотреть в личном кабинете)
- [kingmodiptv.top](http://kingmodiptv.top/)  (поддерживаемые плейлисты tv.m3u)
- [global-iptv.net](http://global-iptv.net/) (поддерживаемые плейлисты tv.m3u)
- [ontv.pro](https://bill.ontv.pro/account/register?ref=1627&c=1667)


## Список проверенных провайдеров (без архивов)

- [ip-tv.club](https://ip-tv.club/partner/10437/) 
- [fox-tv.fun](http://shop.fox-tv.fun/) (рекомендуется "M3U Plus" плейлист)
- [tvoetv.in.ua](https://tvoetv.in.ua/)
- [strah.tv](http://strah.tv/7004534/) (рекомендуется включить опцию "MPEG-2 TS" перед скачиванием плейлиста)
- [my.1ott.net](http://my.1ott.net/) (рекомендуется "ottnavm3u8.m3u8" плейлист)
- [shara.club](https://www.shara.club/reg-205521.html/)
- [voron.info](http://voron.info/)
- [sovok.tv](http://sovok.tv/register/?ruser=26692/) (требуется включить "Группировать по категориям" -> "Спец полями" перед скачиванием плейлиста)
- [ottglanz.tv](http://ottglanz.tv/partner/slev7n/) (рекомендуется плейлист "HLS" 220+ каналов. В настоящее время плейлист HLS 450+ каналов ремонтируется на серверной стороне провайдера


## Добавление собственных иконок, групп и прочего

Вы можете изменять параметры каналов и иконки стандартных групп.

При конвертации учитываются файлы exclusions.xml и conf.yaml в корне програмы а также файлы <имя m3u>.conf.yaml и <имя m3u>.exclusions.yaml, лежащие рядом с конвертируемым m3u плейлистом. Конфиги рядом с m3u имеют больший приоритет. Таким образом вы имеет возможность сконфигурировать часть параметров одинаково для всех m3u, а часть индивидуально. 

Примеры настроек смотрите в папке examples.

### Настройка групп

Файл conf.yaml содержит список групп каналов и иконки к ним в yaml формате 
```yaml
'имя группы из m3u':'иконка'
```
Иконка может быть локальным абсолютным или относительным путем либо http(s) адресом (во время конвертации такие изображения будут скачаны).

Для удобства можно воспользоваться онлайн редактором с проверкой yaml синтаксиса https://onlineyamltools.com/edit-yaml

Не рекомендуется изменять стандартные иконки в папке icons, так как они будут перезатерты при обновлении программы.

### Натройка каналов

Файл exclusions.xml позволяет настроить иконки и расписание каналов.
```xml
<?xml version="1.0" encoding="utf-8" ?>
<tv_info>
  <tv_channels>
    <tv_channel>
      <caption>имя канала из m3u</caption>
      <epg_id>id c vsetv.com</epg_id>
      <tvg_id>id c teleguide.info</tvg_id>
      <icon_url>иконка</icon_url>
    </tv_channel>
    <tv_channel>
      <caption>имя канала из m3u</caption>
      <epg_id>id c vsetv.com</epg_id>
      <tvg_id>id c teleguide.info</tvg_id>
      <icon_url>иконка</icon_url>
    </tv_channel>
    <!-- и т.д ... -->
  </tv_channels>
</tv_info>
```
Id c vsetv.com можно узнать из url канала вида http://www.vsetv.com/schedule_channel_1071_day_2019-04-04.html Число между channel_ и _day есть id (1071).

Id c teleguide.info узнать из url канала вида https://www.teleguide.info/kanal1006_20190326.html Число между kanal и _ есть id (1006).

Иконка может быть локальным абсолютным или относительным путем либо http(s) адресом (во время конвертации такие изображения будут скачаны).

### Главная иконка приложения

Подобно настройке иконок групп в conf.yaml добавьте строку или измените существующую
```yaml
_:'иконка'
```

## Вопросы и ответы

> Архивы не работают.

Провайдеров очень много, они появляются и исчезают. Одновременно с этим не существует единого стандарта указания расположения архивов через m3u плейлист. Каждый провайдер предоставляет их как захочет. Мы добавили и протестировали наиболее популярных провайдеров на наш взгляд.

Если вашего провайдера нет в списке поддерживаемых, то напишите нам в telegram группу [@all_iptv_dune_plugin](https://taraflex.github.io/tg/#https://t.me/all_iptv_dune_plugin) или в [issues](https://github.com/Slev7nm/all-iptv-dune-plugin/issues) - мы его добавим.

> Конфиги неудобно редактировать. Можете сделать с этим что-нибудь?

Возможно когда-нибудь мы добавим в приложение gui конструктор вместо конфигов, но наверное очень не скоро.

> Планируется открыть исходники приложения?

Пока нет. Они кошмарны. Нам стыдно. Исходники php плагина можно посмотреть, распаковав генерируемый zip архив.

> Ваши стандартные картинки для групп каналов ужасны.

Мы не против, если кто-нибудь нарисует их нам поприличнее или предложит альтернативные варианты со свободной лицензией.

> Мой iptv провайдер не предоставляет m3u. Могу ли я все равно как-нибудь использовать вашу программу?

Напишите нам в telegram группу [@all_iptv_dune_plugin](https://taraflex.github.io/tg/#https://t.me/all_iptv_dune_plugin) или в [issues](https://github.com/Slev7nm/all-iptv-dune-plugin/issues). Мы рассмотрим возможность добавления в парсер дополнительных форматов.

> Хочу помочь в развитии! Как?

Мы тоже хотим, чтобы нам помогали! Прямо сейчас нам нужен дизайнер, чтобы отрисовать иконки приложения и групп каналов. Пишите в telegram группу [@all_iptv_dune_plugin](https://taraflex.github.io/tg/#https://t.me/all_iptv_dune_plugin) или в [issues](https://github.com/Slev7nm/all-iptv-dune-plugin/issues).
Ну и финансами естественно тоже можете помогать.

[<img src="https://az743702.vo.msecnd.net/cdn/kofi5.png?v=2" width="202" alt="https://ko-fi.com/alliptv"/>](https://ko-fi.com/alliptv)

> Зачем программе требуется доступ в сеть?

Чтобы скачать неизвестные иконки каналов с vsetv.com и teleguide.info, для проверки обновлений, а также для отправки ошибок о конвертации. 

С программой поставляется определенный набор иконок, но его не всегда достаточно.

Вы можете просмотреть сниффером, что никакие дополнительные данные не передаются. 

> Я не хочу ничего никуда отправлять! Можно отключить вашу богомерзкую телеметрию?

Да. Просто создайте файл notelemetry.txt в директории приложения. Помните, что собираемая статистика ошибок помогает улучшать алгоритмы подбора иконок и расписаний каналов.  

> Значит токены доступа в моих плейлистах в безопасности?

Да. 

> Ничего не работает! Вы рукожопы!

Нуу... совсем ничего не работать не может... наверное...

Миром правят деньги! Часть рукожопости можно компенсировать привлечением дополнительных разработчиков, с более прямыми руками. 

[<img src="https://az743702.vo.msecnd.net/cdn/kofi5.png?v=2" width="202" alt="https://ko-fi.com/alliptv"/>](https://ko-fi.com/alliptv)

> Хочу больше фичь! Почему вы такие медленные? 

¯\\_(ツ)_/¯
