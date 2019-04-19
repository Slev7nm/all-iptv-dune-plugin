# All IPTV
<img src="./logo.png" width="256" height="256">

# [EN]

All IPTV is a program for converting m3u / m3u8 playlists of any iptv provider into a plugin for viewing iptv on Dune HD Players.
We do not provide a plugin for a particular provider - you build it yourself!

Main features

    Categories with icons
    Selection of channel icons
    Selection of channel schedules from http://www.vsetv.com/ and https://teleguide.info/
    Archives for verified providers
    MultiPlaylist

How to use

Just drag the m3u / m3u8 playlist from any folder onto the application icon. Demo – https://imgur.com/a/tZLKgYJ

Also The Software supports the conversion of multiple playlists in one plugin. Demo - https://imgur.com/a/4sEQxXy

Option to switch playlists in the generated plugin on the settings page ( Button “D” )

Working With The Software

If your provider provides the ability to download playlist channels in the formats m3u / m3u8, then with the help of this converter you can turn it into a plugin for Dune HD with your own hands. We tried to reduce the number of settings to a minimum and reduce the conversion process to a few clicks and the plugin is ready to installation.

No services! No paid subscriptions! No restrictions - download the program only once and Convert as much as you want.
During processing, the program will intellectually try to find icons, a schedule, and archives to the list of channels from m3u playlist that you choose to convert.

Unfortunately, the m3u contains only information about groups and channel names, and the channel names themselves are named in any form (often also with typos), that is why a small part of the channels may not be converted in the generated plug-in. In this case, you can watch them, but without additional features. If you have a lot of patience, then you can correct this moment by manually writing configs for them.

List of verified providers

    [itv.live] https://itv.live/
    [schuriktv.nethouse.ru] https://schuriktv.nethouse.ru/
    [greatiptv.cc] https://bill.greatiptv.cc/
    [shura.tv] https://shura.tv/
    [ottclub.cc] https://ottclub.cc/
    [gomel-sat.bz] https://gomel-sat.bz/
    [edem.tv] https://edem.tv/
    [tvclub.cc] https://tvclub.cc/
    [shara-tv.org] https://shara-tv.org/

Adding custom icons, groups, and more

You can change the parameters of channels and icons of standard groups.

When converting, the exclusions.xml and conf.yaml files in the program root are taken into program priority, as well as the files .conf.yaml and .exclusions.yaml, which are located next to the m3u playlist. Configs next to m3u have higher priority. Thus, you have the ability to configure part of the parameters equally for all m3u, and some providers of m3u individually.

Examples of settings are in the examples folder.

Setting Up Groups

The conf.yaml file contains a list of channel groups and icons for them in yaml format.

‘name of the group from m3u’ : ‘path to icon’

The icon can be a local or relative path or http(s) address (during the conversion, such images will be downloaded).

For convenience, you can use the online editor with checking yaml syntax https://onlineyamltools.com/edit-yaml

It is not recommended to change the standard icons in the default_groups_icons folder, as they will be reset when the program is updated.

Customize Channels

The exclusions.xml file allows you to customize icons and channel schedules.

    <?xml version="1.0" encoding="utf-8" ?>
    <tv_info>
      <tv_channels>
        <tv_channel>
          <caption>name of the channel from m3u</caption>
          <epg_id>id from vsetv.com</epg_id>
          <tvg_id>id from teleguide.info</tvg_id>
          <icon_url>icon</icon_url>
        </tv_channel>
        <tv_channel>
          <caption>name of the channel from m3u</caption>
          <epg_id>id from vsetv.com</epg_id>
          <tvg_id>id from teleguide.info</tvg_id>
          <icon_url>icon</icon_url>
        </tv_channel>
        <!-- и т.д ... -->
      </tv_channels>
    </tv_info>

Id from vsetv.com can be found from the channel url type http://www.vsetv.com/schedule_channel_1071_day_2019-04-04.html The number between channel_ and _day is id (1071).

Id from teleguide.info find out from the url of the channel like https://www.teleguide.info/kanal1006_20190326.html The number between kanal and _ is id (1006).

The icon can be a local absolute or relative path or http (s) address (during the conversion, such images will be downloaded).
Questions and answers

    Archives do not work.

There are a lot of providers, they appear and disappear. At the same time, there is no single standard for specifying the syntax of archives via the m3u playlist. Each provider provides them as they feel needed to. We have added and tested the most popular providers in our opinion.

If your provider is not in the list of supported, then write to us in the telegram group @all_iptv_dune_plugin or in issues - we will add it.

    Configs inconvenient to edit. Can you do something about it?

Maybe someday we will add a constructor instead of config files to the gui application, but probably not very soon.

    Do you plan to open the source of the application?

Not yet. They are fast coded and not commented , We are ashamed of the source code. the source of php plugin can be viewed by unpacking the generated zip archive.

    Your standard pictures for channel groups are terrible.

We do not mind if someone draws them more decently or offers alternative options with a free license.

    My iptv provider does not provide m3u. Can I still use your program somehow?

Write us in the telegram group @all_iptv_dune_plugin or in issues. We will consider the possibility of adding additional formats to the parser.

    Why does the program need access to the network?

To download the current list of channels from vsetv.com and teleguide.info and channel icons, as well as to check for updates.

The program comes with a certain set of icons, but it is not always enough.

You can view with the sniffer that no additional data is transmitted.

    So access tokens from my playlists are safe?

Yes. But remember - on the Internet, no one knows that you are a cat …

    Nothing works! You are the hands!

Well … nothing working at all … probably …

The world is ruled by money! So If You Left Handed Hands This can be compensated by the involvement of additional developers, with two normal working hands.

Link to donate in the application.

    I want to help in the development! How?

We also want to help us! Right now, we need a designer to draw application icons and channel groups. Write to the telegram group @all_iptv_dune_plugin or to issues. Well, of course, you can also help with finances.

    I want more features! Why are you so slow?

The developer of the converter lives in the end of the world. Someday the mail will figure out how to deliver a dune hd player to him. Write software without a device is pain and frustration.

    Where to contact directly with the developer?

Here -> @Taraflex
Support Group Here - https://t.me/all_iptv_dune_plugin



[Download latest version](https://github.com/Slev7nm/all-iptv-dune-plugin/releases/latest)

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

## Как использовать
Просто перетащите m3u/m3u8 плейлист из любой папки на иконку приложения. Демо - https://imgur.com/a/tZLKgYJ

Также поддерживается конвертация нескольких плейлистов в один плагин. Демо - https://imgur.com/a/4sEQxXy

Переключать плейлисты в сгенерированном плагине вы сможете на странице настроек. 

## Принцип работы
Если ваш провайдер предоставляет возможность скачать плейлист каналов в форматах m3u/m3u8, то с помощью данного конвертера можно превратить его в плагин для Dune HD своими руками. Мы постарались свести число настроек к минимуму и свести процесс конвертации к нескольким нажатиям на enter.

Никаких сервисов! Никаких платных подписок! Никаких ограничений - качаем программу лишь раз и обрабатываем хоть тысячу плейлистов. 
В процессе обработки программа будет пытаться интелектуально подобрать иконки, расписание, и архивы к списку каналов из вашего m3u плейлиста.

К сожалению в m3u содержится лишь информация о группах и названиях каналов, а сами названия каналов записано в какой угодно форме (зачастую еще и с опечатками), поэтому в сгенерированном плагине существенная часть каналов может не определится. При этом вы сможете их просматривать, но без дополнительных возможностей. Если у вас много терпения, то вы можете исправить этот момент ручным написанием конфигов под них.

## Список проверенных провайдеров

- [itv.live](https://itv.live/) 
- [schuriktv.nethouse.ru](https://schuriktv.nethouse.ru/) 
- [greatiptv.cc](https://greatiptv.cc/)  
- [shura.tv](https://shura.tv/) 
- [ottclub.cc](https://ottclub.cc/) 
- [gomel-sat.bz](https://gomel-sat.bz/) 
- [edem.tv](https://edem.tv/) 
- [tvclub.cc](https://tvclub.cc/)
- [shara-tv.org](https://shara-tv.org/)

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

Ссылка на донат в приложении.

> Хочу помочь в развитии! Как?

Мы тоже хотим чтобы нам помогали! Прямо сейчас нам нужен дизайнер, чтобы отрисовать иконки приложения и групп каналов. Пишите в telegram группу [@all_iptv_dune_plugin](https://taraflex.github.io/tg/#https://t.me/all_iptv_dune_plugin) или в [issues](https://github.com/Slev7nm/all-iptv-dune-plugin/issues).
Ну и финансами естественно тоже можете помогать.

> Хочу больше фичь! Почему вы такие медленные? 

¯\\_(ツ)_/¯
