# Проект: Прогноз времени доставки

## 📦 Данные

В наличии были следующие данные о заказах и доставках:

- `ID` — уникальный идентификатор заказа  
- `Warehouse_block` — склад, с которого была отгрузка  
- `Mode_of_Shipment` — способ доставки (например, Ship, Flight, Road)  
- `Customer_care_calls` — количество обращений в службу поддержки  
- `Customer_rating` — оценка клиента (1–5)  
- `Cost_of_the_Product` — стоимость товара  
- `Prior_purchases` — количество покупок клиента до текущей  
- `Product_importance` — важность продукта (Low, Medium, High)  
- `Gender` — пол покупателя  
- `Discount_offered` — предоставленная скидка  
- `Weight_in_gms` — вес продукта в граммах  
- `Reached.on.Time_Y.N` — целевая переменная: доставлено вовремя (1) или с опозданием (0)

## 🎯 Задача

Построить модель машинного обучения, которая будет предсказывать, будет ли доставка своевременной

## 📊 Результаты

- **Лучшая модель**: `LogisticRegression`
- **Метрики на тестовой выборке** (при оптимальном пороге в 0.47):
  - recall = 0.776
  - precision = 0.663

- **Ключевые важные признаки** (по Permutation Importance):
  - `discount`
  - `weight`
  - `prior_purchases`
  - `price`
  - `weight_class`

## 🧰 Используемые библиотеки

*pandas | numpy | matplotlib | seaborn | scikit-learn | catboost | lightgbm | xgboost | optuna | scipy | tqdm | re*
