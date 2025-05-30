---
tags:
  - virtualization
---
---

# Описание  
Docker — это платформа для разработки, доставки и запуска приложений в изолированных контейнерах. Контейнеры позволяют упаковать приложение вместе с его зависимостями, что обеспечивает согласованность работы на разных средах .  

## Инструменты  
- **Volume Mounts**: используется для хранения данных вне контейнера, обеспечивая их персистентность .  
- **Bind Mounts**: позволяет монтировать директории или файлы с хост-машины в контейнер .  
- **Ephemeral container filesystem**: временное хранилище данных внутри контейнера, которое исчезает после остановки контейнера .  

## Связь с другими навыками  
| Технология | Взаимодействие |  
| ---------- | -------------- |  
| [[Kubernetes]] | Использует Docker как основу для создания подов . |  
| CI/CD      | Docker интегрируется в пайплайны для автоматизации сборки и тестирования . |  
| DevOps     | Docker помогает стандартизировать среды разработки и продакшена . |  

## Архитектура и основные понятия  
- **Volume Mounts**: данные хранятся в специальных областях, управляемых Docker. Это удобно для резервного копирования и миграции .  
- **Bind Mounts**: данные хранятся на хост-машине, что полезно для быстрого доступа и отладки .  
- **Ephemeral container filesystem**: временное хранилище внутри контейнера, которое не сохраняется после остановки или удаления контейнера .  

# Практика  

## Оценка уровня навыка  
| Уровень | Описание | Ключевые навыки | Критерии оценки |  
| ------- | -------- | --------------- | --------------- |  
| Junior  | Понимание базовых команд Docker. | Запуск контейнеров, создание Volume и Bind Mounts. | Может использовать готовые образы и базовые конфигурации. |  
| Middle  | Настройка контейнеров для проектов. | Работа с сетями, управление Volume и Bind Mounts. | Создает собственные Dockerfile и docker-compose.yml. |  
| Senior  | Проектирование архитектуры с использованием Docker. | Оптимизация размера образов, использование Ephemeral filesystem. | Минимизирует downtime и обеспечивает отказоустойчивость. |  
| Expert  | Использование Docker в сложных системах. | Интеграция с [[Kubernetes]], управление большими фермами контейнеров. | Гарантирует высокую производительность и масштабируемость. |  

## Бизнес-ценность и использование в работе  
| Применение      | Описание                               | Преимущества                   | Рекомендации по использованию     |  
| --------------- | -------------------------------------- | ------------------------------ | --------------------------------- |  
| Разработка ПО   | Обеспечивает изоляцию среды разработки. | Устраняет проблемы "у меня работает". | Использовать Volume для данных. |  
| Тестирование    | Автоматизация тестов в изолированных средах. | Ускоряет процесс тестирования. | Использовать Bind Mounts для отладки. |  
| Продакшен       | Запуск микросервисов в контейнерах.    | Легкость масштабирования.       | Использовать Ephemeral filesystem для временных данных. |  

## Pet-project  

| Уровень    | Название проекта | Описание | Технологии | Критерий успеха | Вспомагательные ссылки |  
| ---------- | ---------------- | -------- | ---------- | --------------- | ---------------------- |  
| **Junior** | Blog Engine       | Простой блог с возможностью добавления статей. | Docker, Flask, SQLite | Контейнер запускается и работает локально. |  |  
| **Middle** | Микросервисы     | Система с несколькими сервисами (API, frontend). | Docker Compose, Node.js, React | Сервисы взаимодействуют через сети Docker. |  |  
| **Senior** | CI/CD Pipeline   | Автоматизация сборки и деплоя приложения. | Jenkins, Docker, [[Kubernetes]] | Приложение деплоится в облако без простоя. |  |  
| **Expert** | Multi-region App | Приложение, работающее в нескольких регионах. | Docker Swarm, AWS ECS | Высокая доступность и отказоустойчивость. |  |  

## Траблшутинг  
- **Проблемы с данными**: используйте Volume вместо Bind Mounts для повышения надежности .  
- **Контейнер не запускается**: проверьте логи с помощью `docker logs <container_id>` .  
- **Недостаток места**: очистите неиспользуемые образы и Volume командой `docker system prune` .  

## Ресурсы, форумы  
- [Habr](https://habr.com) — статьи и практические примеры использования Docker .  
- [GeeksforGeeks](https://www.geeksforgeeks.org) — руководства по настройке Bind Mounts .  
- [Medium](https://medium.com) — обзоры Docker Volume и Bind Mounts .
