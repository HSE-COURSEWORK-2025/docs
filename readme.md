# HSE Coursework: документация

## Описание

Данный репозиторий содержит PlantUML-схемы с документацией архитектуры и процессов проекта. Здесь представлены диаграммы развертывания, архитектуры, DFD, последовательности сценариев, иллюстрирующие взаимодействие компонентов системы.

## Архитектура

- **Микросервисы**: FastAPI-сервисы для сбора данных, авторизации, уведомлений, оценок, мониторинга (Grafana).
- **Обработка данных**: Airflow DAGs для ETL, поиска выбросов, подготовки данных и ML-прогнозирования.
- **Очереди и хранилища**: Kafka, Redis, PostgreSQL.
- **Фронтенд**: React-приложение для пользователей.
- **Интеграции**: Google Fitness API, Google Health Connect, SMTP для email-уведомлений.

Диаграммы архитектуры и взаимодействия находятся в папке `docs`:
- `deployment-diagram.puml` — диаграмма развертывания
- `global-arch.puml` — общая архитектура
- `dfd.puml` — DFD системы
- `sequence-diagram-*.puml` — последовательности сценариев

## Основные компоненты

- [**hse-coursework-backend-data-collection-service**](https://github.com/HSE-COURSEWORK-2025/hse-coursework-backend-data-collection-service) — сервис сбора данных
- [**hse-coursework-auth-api**](https://github.com/HSE-COURSEWORK-2025/hse-coursework-auth-api) — сервис авторизации и управления пользователями
- [**hse-coursework-notifications-api**](https://github.com/HSE-COURSEWORK-2025/hse-coursework-notifications-api) — сервис уведомлений
- [**hse-coursework-ratings-api**](https://github.com/HSE-COURSEWORK-2025/hse-coursework-ratings-api) — сервис оценок
- [**hse-coursework-drammatiq-data-collector**](https://github.com/HSE-COURSEWORK-2025/hse-coursework-drammatiq-data-collector) — обработка очередей и нормализация данных
- [**hse-coursework-front**](https://github.com/HSE-COURSEWORK-2025/hse-coursework-front) — веб-интерфейс
- [**hse-coursework-airflow**](https://github.com/HSE-COURSEWORK-2025/hse-coursework-airflow) — оркестрация ETL и ML пайплайнов
- [**hse-coursework-backend-fetch-google-api-data**](https://github.com/HSE-COURSEWORK-2025/hse-coursework-backend-fetch-google-api-data) — сервис выгрузки данных из Google API
- [**hse-coursework-backend-prepare-data**](https://github.com/HSE-COURSEWORK-2025/hse-coursework-backend-prepare-data) — сервис подготовки данных
- [**hse-coursework-backend-find-outliers**](https://github.com/HSE-COURSEWORK-2025/hse-coursework-backend-find-outliers) — сервис поиска выбросов
- [**hse-coursework-backend-ml-predictions**](https://github.com/HSE-COURSEWORK-2025/hse-coursework-backend-ml-predictions) — сервис ML-прогнозирования
- [**hse-coursework-redis**](https://github.com/HSE-COURSEWORK-2025/hse-coursework-redis) — хранилище Redis
- [**hse-coursework-kafka**](https://github.com/HSE-COURSEWORK-2025/hse-coursework-kafka) — очередь Kafka
- [**hse-coursework-grafana**](https://github.com/HSE-COURSEWORK-2025/hse-coursework-grafana) — мониторинг (Grafana)
- [**hse-coursework-android-app**](https://github.com/HSE-COURSEWORK-2025/hse-coursework-android-app) — мобильное приложение
- [**hse-coursework-kubernetes-config**](https://github.com/HSE-COURSEWORK-2025/hse-coursework-kubernetes-config) — конфигурация Kubernetes

## Основные сценарии

1. **Выгрузка данных**: через Google Fit или через мобильное приложение.
2. **Обработка и анализ**: нормализация, поиск выбросов, ML-прогнозы.
3. **Просмотр данных и уведомлений**: через веб-интерфейс.
4. **Оценка приложения**: пользователи могут ставить оценки.

## Диаграммы

Представлены PlantUML-диаграммы:
- Архитектура развертывания
- DFD
- Последовательности сценариев (выгрузка, обработка, ML, фронтенд)
