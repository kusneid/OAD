ЛЕКЦИЯ 1. Современный Data-пайплайн: технологии и архитектуры

Технологический фокус:

Общая архитектура: Sources → Ingestion → Storage → Processing → Serving → BI/ML

Основные технологии: Kafka, Airflow, Spark, ClickHouse, S3, Parquet, dbt

Роли: DE, DA, DS, MLE

Batch vs Streaming

Сквозной пример реального проекта

ЛЕКЦИЯ 2. Архитектуры хранения: DWH, Data Lake, Lakehouse

Технологический акцент:

DWH: Snowflake, BigQuery, ClickHouse

Data Lakes: S3, HDFS

Lakehouse: Delta Lake, Apache Iceberg

Parquet/ORC — почему именно они

Зоны данных: Raw, Staging, Curated

ACID в lakehouse, schema evolution

ЛЕКЦИЯ 3. Источники данных и способы загрузки (Batch & Streaming Ingestion)

Технологии:

Источники: PostgreSQL, MySQL, MongoDB, API, лог-файлы, clickstream

Batch ingestion: Airflow (DAG, Sensor, Operator)

Streaming ingestion: Kafka (topics, partitions, producers/consumers)

CDC инструменты: Debezium, Kafka Connect

Ingestion в S3, ClickHouse, Lakehouse

ЛЕКЦИЯ 4. ETL/ELT: трансформации и инструменты

Технологии:

dbt (модели, staging, marts, lineage)

Spark SQL / DataFrame API

SQL-трансформации (joins, window functions, aggregation)

Методы очистки, нормализации, deduplication

Архитектурные паттерны: ETL vs ELT

Monitoring качества данных: Great Expectations

ЛЕКЦИЯ 5. Spark: распределённая обработка аналитических данных

Технологический фокус:

Spark DataFrame API

Spark SQL

Partitioning, Bucketing

Catalyst Optimizer, Tungsten

Broadcast join, shuffle

Построение витрины через Spark

ЛЕКЦИЯ 6. Data Quality, Data Validation и подготовка данных для BI/ML

Технологии:

DQ инструменты: Great Expectations, Deequ

Типы ошибок в данных

Feature preprocessing: scaling, encoding

Валидация схем (schema registry)

Метрики качества данных

Data Contracts

🟦 Блок 2 — Business Intelligence & DWH Modeling (4 лекции)

Фокус: проектирование витрин, OLAP, BI-платформы.

ЛЕКЦИЯ 7. Моделирование данных: Star Schema, Data Vault, SCD

Технологии:

Star Schema в Snowflake/ClickHouse

Data Vault 2.0 (Hubs, Links, Satellites)

Slowly Changing Dimensions SCD1–SCD6

Выбор архитектуры под задачу

Дизайн аналитических витрин

ЛЕКЦИЯ 8. OLAP и аналитические запросы

Технологии:

ClickHouse: колоночное хранилище, MergeTree, агрегации

OLAP-концепции: slice, dice, roll-up, drill-down

Многомерные данные без кубов (табличный OLAP)

BigQuery: аналитические функции

Типовые аналитические запросы

ЛЕКЦИЯ 9. BI-инструменты: Power BI, Tableau, Apache Superset

Технологии и фокус:

Подключение BI к DWH

Модели данных внутри Power BI

DAX (введение)

Tableau: визуальные паттерны

Superset: opensource BI

Реальные примеры дашбордов

ЛЕКЦИЯ 10. Reporting & Data Storytelling: аналитические отчёты и KPI

Технологии и методы:

Метрики: LTV, retention, MAU/DAU, conversion

Storytelling в BI

KPI-дешборды

Ошибки визуализации

Как объединить BI + ML (ML-прогнозы на дашборде)

🟥 Блок 3 — Machine Learning / Analytical ML / MLOps (5 лекций)

Фокус: практическая аналитика, фичи, модели, внедрение ML в production.

ЛЕКЦИЯ 11. Аналитический ML: роль машинного обучения в BI и данных

Технологический акцент:

ML как часть аналитической экосистемы

Типовые аналитические задачи: прогнозирование, scoring, сегментация

ML поверх витрин

Стек технологий: sklearn, pandas, MLflow, Airflow

Analytical ML vs Research ML

ЛЕКЦИЯ 12. Feature Engineering и построение Feature Sets

Технологии:

Feature stores: Feast, Hopsworks (концептуально)

pandas: трансформации, агрегации, merge

Технические фичи: лаги, окна, rolling

Категориальные признаки (OHE, target encoding)

Создание признаков из витрин

Важность reproducibility

ЛЕКЦИЯ 13. Прикладное ML-моделирование: forecasting, scoring, кластеризация

Технологии:

sklearn: LinearRegression, LogisticRegression, RandomForest, GradientBoosting

XGBoost/LightGBM (как индустриальный стандарт)

k-means, DBSCAN для сегментации

Feature importance, SHAP

Применение моделей в BI и продуктах

ЛЕКЦИЯ 14. Временные ряды и прогнозирование: аналитический подход

Технологии:

statsmodels для базовых моделей

sklearn + фичи для ML-прогнозирования

Prophet (при необходимости)

MAPE, SMAPE, MAE

Trend/seasonality decomposition

Добавление прогнозов в витрины/BI

ЛЕКЦИЯ 15. MLOps и внедрение моделей в production

Технологии:

MLflow (tracking, model registry)

Airflow для ML pipeline

Docker-контейнеризация моделей

Monitoring & drift detection

Feature store pipeline

Deployment моделей в витрины, серверы, BI

Полный ML lifecycle
