# 📊 Проект: Прогноз оттока сотрудников

## 📦 Данные

В наличии были следующие данные о сотрудниках:

- `Employee ID` — уникальный идентификатор сотрудника  
- `Age` — возраст  
- `Gender` — пол  
- `Years at Company` — стаж в компании  
- `Job Role` — должность  
- `Monthly Income` — ежемесячный доход  
- `Work–Life Balance` — баланс между работой и личной жизнью  
- `Job Satisfaction` — удовлетворённость работой  
- `Performance Rating` — оценка результативности  
- `Number of Promotions` — количество повышений  
- `Overtime` — переработки  
- `Distance from Home` — расстояние от дома  
- `Education Level` — уровень образования  
- `Marital Status` — семейное положение  
- `Number of Dependents` — количество иждивенцев  
- `Job Level` — уровень должности  
- `Company Size` — размер компании  
- `Company Tenure` — общее время работы в компании  
- `Remote Work` — работает ли удалённо  
- `Leadership Opportunities` — наличие лидерских возможностей  
- `Innovation Opportunities` — наличие инновационных задач  
- `Company Reputation` — репутация компании  
- `Employee Recognition` — признание сотрудника  
- `Attrition` — целевая переменная: уволился или остался

## 🎯 Задача

Построить модель машинного обучения, которая будет предсказывать вероятность ухода сотрудника.

## 📈 Результаты

- **💡 Лучшая модель**: `CatBoostClassifier`

- **📊 Метрики на тестовой выборке** (при оптимальном пороге в `0.44`):
  - `recall` = `0.8068`  
  - `precision` = `0.7128`  
  - `f1-score` = `0.7569`

- **🔑 Ключевые важные признаки** (по `Permutation Importance`):
  - `job_level_Senior`  
  - `marital_status_Single`  
  - `remote_work_Yes`  
  - `work_life_balance`  
  - `number_of_promotions`  
  - `company_reputation`  
  - `distance_from_home`  
  - `number_of_dependents`

## 🧰 Используемые библиотеки

pandas | numpy | matplotlib | seaborn | scikit-learn | catboost | lightgbm | xgboost | optuna | scipy | tqdm | re
