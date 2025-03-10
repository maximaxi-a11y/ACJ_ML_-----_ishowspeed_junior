### ACJ_ML_-_ishowspeed_junior

Этот репозиторий содержит исходный код модели от команды IshowSpeed Junior для **Alfa Campus Junior**.

**Назначение модели:**  
Данная модель предназначена для прогнозирования оттока партнеров в будущем.

### Как скачать:

```
git clone https://github.com/maximaxi-a11y/ACJ_ML_-_ishowspeed_junior.git
cd ACJ_ML_-_ishowspeed_junior
```

### Установка необходимых библиотек

Для установки всех необходимых библиотек можно воспользоваться файлом requirements.txt:

```
pip intsall -r requirements.txt
```


### Запуск кода


```
python ML_IshowSpeed_junior.py
```

### Используемые инструменты

- **pandas**: библиотека для работы с данными, предоставляет мощные средства для анализа и обработки данных.
- **catboost**: библиотека для градиентного бустинга на деревьях решений, разработанная для работы с категориальными признаками.
- **numpy**: библиотека для работы с многомерными массивами и матрицами, содержит большое количество математических функций.
- **XGBoost**: библиотека для реализации градиентного бустинга, оптимизированная для производительности и скорости.
- **matplotlib**: библиотека для визуализации данных в графическом виде.
- **shap**: библиотека для интерпретации моделей машинного обучения с использованием SHAP значений.
- **tsfresh**: библиотека для извлечения временных признаков из временных рядов.

### Структура проекта

- **dataset_main.csv**: исходный файл данных.
- **ML_IshowSpeed_junior.py**: основной файл скрипта для запуска модели.
- **requirements.txt**: список зависимостей проекта.

### Описание кода

**Предобработка данных:**
- Чтение данных из CSV файла и преобразование столбцов с датами в формат datetime.
- Добавление столбца с месяцем начала клиента.
- Создание диапазона дат для требуемого периода и агрегация данных по месяцам и партнёрам.

**Формирование признаков:**
- Создание лаговых признаков (значения за предыдущие месяцы).
- Создание скользящих признаков (средние, максимальные, минимальные значения за несколько месяцев).
- Создание стандартных отклонений и относительных стандартных отклонений.
- Создание признаков на основе разниц значений.

**Моделирование:**
- Разделение данных на обучающую и тестовую выборки.
- Обучение моделей (CatBoost, RandomForest, XGBoost).
- Оценка качества моделей с использованием метрик ROC-AUC и classification report.
- Использование кросс-валидации для оценки стабильности модели.

**Интерпретация результатов:**
- Использование библиотеки SHAP для интерпретации моделей и определения важности признаков.

**Подготовка данных для отправки:**
- Формирование данных для прогнозирования и сохранение результатов в CSV файл.

### Лицензия

Этот проект лицензирован под лицензией MIT. Подробности см. в файле [LICENSE](LICENSE).

### Контрибьюторы

- **Колесников Максим**: разработка модели, обработка данных, создание презентации.
- **Козлов Сергей**: визуализация данных, обработка данных,подготовка данных.


### Контактная информация

Если у вас есть вопросы или предложения, вы можете связаться с нами в телеграмме: [LilTeck](https://t.me/LilTeck1337), [Maximaxi-a11y](https://t.me/ggggg54680).

Мы надеемся, что этот проект будет полезен для Альфа Банка!








