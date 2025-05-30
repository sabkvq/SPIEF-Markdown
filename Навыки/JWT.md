---
tags:
  - security
---
---

# JWT (JSON Web Tokens)

## Описание

JSON Web Token (JWT) - это открытый стандарт (RFC 7519) для безопасной передачи информации между сторонами в виде JSON-объекта. Токен содержит цифровую подпись, обеспечивающую аутентичность и целостность передаваемых данных

## Инструменты

* **Библиотеки**
  * jsonwebtoken (Node.js)
  * PyJWT (Python)
  * jjwt (Java)
  * System.IdentityModel.Tokens.Jwt (.NET)
* **Инструменты разработки**
  * jwt.io Debugger
  * Postman JWT Plugin
  * JWT Inspector (Chrome)

## Связь с другими навыками

| Технология     | Взаимодействие                                             |
| -------------- | ---------------------------------------------------------- |
| OAuth 2.0      | Используется как формат токенов доступа                    |
| OpenID Connect | Основной механизм передачи информации                      |
| [[HTTPS]]      | Требуется для безопасной передачи токенов                  |
| [[SSL]]        | Используется для шифрования при передаче                   |
| Base64         | Используется для кодирования заголовка и полезной нагрузки |

## Практика

### Оценка уровня навыка

| Уровень | Описание                     | Ключевые навыки                                                        | Критерии оценки                         |
| ------- | ---------------------------- | ---------------------------------------------------------------------- | --------------------------------------- |
| Junior  | Базовое понимание JWT        | Генерация и валидация токенов                                          | Успешная аутентификация пользователей   |
| Middle  | Продвинутая настройка        | Настройка собственных claims, реализация refresh tokens                | Безопасная работа с токенами            |
| Senior  | Оптимизация и безопасность   | Разработка собственных схем подписи, оптимизация производительности    | Высокая производительность системы      |
| Expert  | Архитектурное проектирование | Создание кастомных библиотек JWT, проектирование систем аутентификации | Масштабируемость и безопасность системы |

### Бизнес-ценность и использование в работе

| Применение      | Описание                               | Преимущества                   | Рекомендации по использованию     |
| --------------- | -------------------------------------- | ------------------------------ | --------------------------------- |
| Аутентификация  | Безопасная идентификация пользователей | Безопасность, масштабируемость | Использовать с HTTPS              |
| Авторизация API | Контроль доступа к API                 | Простота интеграции, гибкость  | Реализовать валидацию claims      |
| Микросервисы    | Обмен данными между сервисами          | Прозрачность, надежность       | Настроить механизм отзыва токенов |

### Pet-project

| Уровень    | Название проекта | Описание | Технологии | Критерий успеха | Вспомагательные ссылки |
|------------|------------------|----------|------------|----------------|----------------------|
| Junior     | Авторизация API  | Реализация базовой аутентификации с JWT | Node.js, Express, jsonwebtoken | Успешная аутентификация пользователей | 


## Траблшутинг

| Проблема | Причина | Решение | Предотвращение |
|----------|---------|---------|----------------|
| Проблемы безопасности | Неправильное хранение ключей | Использовать переменные окружения | Регулярный аудит безопасности |
| Проблемы производительности | Большой размер токенов | Оптимизация claims | Мониторинг размера токенов |
| Проблемы интеграции | Несовместимость версий | Использовать LTS-версии библиотек | Тестирование совместимости |

## Ресурсы, форумы

- [jwt.io](https://jwt.io) - официальная документация и дебаггер
- [StackOverflow](https://stackoverflow.com/questions/tagged/jwt) - тег JWT
- [GitHub](https://github.com/auth0/node-jsonwebtoken) - библиотеки и примеры
- [Auth0 Blog](https://auth0.com/blog/tag/jwt/) - статьи и туториалы