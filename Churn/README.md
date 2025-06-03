# Проект: Прогноз оттока клиентов телеком-компании

## 📦 Данные


В датасете содержится информация о 7043 клиентах, включая:

- **Общая информация**: `gender`, `SeniorCitizen`, `Partner`, `Dependents`
- **Услуги**: `PhoneService`, `MultipleLines`, `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`
- **Контракт**: `Contract`, `PaperlessBilling`, `PaymentMethod`
- **Финансовые данные**: `MonthlyCharges`, `TotalCharges`
- **Целевой признак**: `Churn` (Yes/No) — факт ухода клиента

## 🎯 Задача

Построить модель машинного обучения, которая сможет предсказать, уйдёт ли клиент в ближайшее время.

## Результат

- **Лучшая модель**: `CatBoostClassifier`
- **Метрика на тесте** (с оптимизированным порогом):
  - Recall: **0.85**
- **Наиболее важные признаки**:
  - `Contract`
  - `tenure`
  - `MonthlyCharges`
  - `OnlineSecurity`
  - `TechSupport`

## 🧰 Используемые библиотеки

*pandas | numpy | matplotlib | seaborn | scikit-learn | catboost | lightgbm*
