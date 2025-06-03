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

## Этапы проекта
 
1. 🧹 **Предобработка и Анализ данных (EDA)**: проверка пропусков, аномалий, распределений
2. 📊 **Подготовка данных**:
   - Кодирование категориальных признаков (OneHot, Ordinal)
   - Масштабирование числовых признаков
   - Обработка дисбаланса
3. 🧠 **Обучение моделей**:
   - Модели: CatBoost, Decision Tree, Logistic Regression, XGB, LGBM
   - GridSearchCV с перекрестной проверкой
   - Подбор гиперпараметров

4. 📈 **Метрики оценки**:
   - Основная метрика: `Recall` — важно выявлять сотрудников, которые **уйдут**
   - Дополнительно: `Precision`, `F1-score`, `Confusion matrix`

5. 🎯 **Дополнительные шаги**:
   - Оптимизация порога вероятности на основе trade-off `recall` и `precision`
   - Определение важности признаков (`Permutation Importance`)
   - Выбор финальной модели (CatBoost)

## Используемые библиотеки

*pandas | numpy | matplotlib | seaborn | scikit-learn | catboost | lightgbm*

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

