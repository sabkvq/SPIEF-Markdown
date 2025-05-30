---
tags:
  - security
---
---

# Описание  
SSO (Single Sign-On) — это технология аутентификации, которая позволяет пользователям входить в несколько приложений или систем с использованием одного набора учетных данных . Это решение упрощает процесс входа для пользователей и снижает нагрузку на службы поддержки за счет уменьшения количества запросов на сброс паролей .  

## Инструменты  
- **SAML**: протокол, используемый для реализации SSO через обмен XML-сообщениями между системами .  
- **OAuth 2.0 и OpenID Connect**: современные протоколы для аутентификации и авторизации, часто используемые в SSO .  
- **Провайдеры SSO**: такие как OneLogin, Okta и AWS IAM, предоставляют готовые решения для внедрения SSO .  

## Связь с другими навыками  
| Технология | Взаимодействие |  
| ---------- | -------------- |  
| IAM (Identity and Access Management) | SSO интегрируется с системами управления идентификацией для централизованного контроля доступа . |  
| Многофакторная аутентификация (MFA) | Дополняет SSO для повышения безопасности, особенно для администраторов . |  
| Облачные сервисы | SSO используется для аутентификации пользователей в облачных приложениях, таких как Google Workspace или Microsoft 365 . |  

## Архитектура и основные понятия  
- **SSO-сервер**: центральная система, которая проверяет учетные данные пользователя и предоставляет токены для доступа к приложениям .  
- **Токены аутентификации**: временные ключи, которые передаются между SSO-сервером и приложениями для подтверждения личности пользователя .  
- **Двухэтапная аутентификация (2FA)**: дополнительный уровень безопасности, который часто используется вместе с SSO .  

# Практика  

## Оценка уровня навыка  
| Уровень | Описание | Ключевые навыки | Критерии оценки |  
| ------- | -------- | --------------- | --------------- |  
| Junior  | Базовое понимание принципов работы SSO. | Настройка клиентских приложений для использования SSO. | Может настроить базовый вход с использованием провайдера SSO. |  
| Middle  | Настройка и управление SSO-системой. | Работа с протоколами SAML, OAuth 2.0, OpenID Connect. | Создает конфигурации для интеграции с несколькими приложениями. |  
| Senior  | Проектирование SSO-инфраструктуры. | Интеграция с IAM, настройка MFA, масштабирование системы. | Обеспечивает отказоустойчивость и безопасность. |  
| Expert  | Использование SSO в сложных архитектурах. | Разработка собственных решений для уникальных задач. | Гарантирует высокую производительность и надежность. |  

## Бизнес-ценность и использование в работе  
| Применение      | Описание                               | Преимущества                   | Рекомендации по использованию     |  
| --------------- | -------------------------------------- | ------------------------------ | --------------------------------- |  
| Упрощение входа | Пользователи могут использовать один набор учетных данных для всех приложений. | Удобство для пользователей.    | Использовать SSO для крупных организаций . |  
| Снижение нагрузки | Уменьшение количества запросов на сброс паролей. | Экономия времени и ресурсов.   | Внедрять SSO вместе с MFA для безопасности . |  
| Централизованное управление | Администраторы могут контролировать доступ из единого места. | Легкость администрирования.    | Интегрировать SSO с IAM для лучшего контроля . |  

## Pet-project  

| Уровень    | Название проекта | Описание | Технологии | Критерий успеха | Вспомагательные ссылки |  
| ---------- | ---------------- | -------- | ---------- | --------------- | ---------------------- |  
| **Junior** | Локальная SSO-система | Настройка SSO для двух приложений. | SAML, Apache | Приложения успешно используют единый вход. |  |  
| **Middle** | Интеграция с облачными сервисами | Настройка SSO для Google Workspace и Microsoft 365. | OAuth 2.0, Azure AD | Пользователи могут входить в оба сервиса с одними учетными данными. |  |  
| **Senior** | Высокая доступность | Настройка отказоустойчивого SSO-сервера. | SAML, Keepalived | Сервер продолжает работать при сбое одного узла. |  |  
| **Expert** | Масштабируемая инфраструктура | Создание SSO-инфраструктуры для крупной организации. | SAML, OAuth 2.0, IAM | Система масштабируется без потери производительности. |  |  

## Траблшутинг  
- **Проблемы с аутентификацией**: проверьте корректность настроек SSO-сервера и приложений .  
- **Ошибки при использовании токенов**: убедитесь, что время жизни токенов настроено правильно .  
- **Безопасность**: добавьте MFA для защиты от несанкционированного доступа .  

## Ресурсы, форумы  
- [Keeper Security](https://keepersecurity.com) — описание преимуществ SSO для бизнеса .  
- [Oracle](https://oracle.com) — руководства по настройке SSO с использованием OAuth 2.0 .  
- [AWS](https://aws.amazon.com) — документация по внедрению SSO в облачных сервисах .  

---