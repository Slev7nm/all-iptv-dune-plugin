# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]
- Автоматическая классификация каналов по группам 

## [1.5.4] - 2019-03-25
### Added
- Синонимы с https://iptvx.one/epg/epg_channels.php
- Автообновления через github
- Более детальный вывод об ошибке в конфиге 
- Новые группы для стандартного конфига

### Changed
- Ключи конфига стали регистронезависимы
- Изменено меню выбора плейлиста в dune плагине
- epg/tvg, которых нет на www.vsetv.com и teleguide.info, не будут добавлены

### Fixed
- Юникод в путях