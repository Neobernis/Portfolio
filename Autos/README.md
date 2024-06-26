# Построение модели определения стоимости автомобиля

Стек: Python, Pandas, Scikit-learn, CatBoost, LightGBM, Seaborn, Matplotlib, Phik

Задача проекта:
Сервис по продаже автомобилей с пробегом разрабатывает приложение для привлечения новых клиентов. В нём можно быстро узнать рыночную стоимость своего автомобиля. На основе исторические данные необходимо построить модель для определения стоимости автомобиля.

Заказчику важны:
* качество предсказания, критерий успеха RMSE до 2500;
* скорость предсказания;
* время обучения.
  
Инструменты: градиентный бустинг, регрессия.

## Вывод:

В полученных данных было много аномалий и пропусков. После обработки, данные были проверенны на дубликаты и очищены. Во время анализа данных, наибольшая ф-корреляция с таргетом Price у признаков год регистрации 0.63, модель 0.55 и мощность 0.47.

Наиболее тояные и быстрые для данной задачи дала результаты модель LightGBM. На кросс-валидации фактически затратила 13 сек на обучение.

RMSE показала на тесте 1483, что является успехом и попадает под критерий до 2500.

![image](https://github.com/Neobernis/Portfolio/assets/109903977/90cf2914-d255-487b-91ef-f000e3449631)
