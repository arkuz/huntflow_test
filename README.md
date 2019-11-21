#### Тестовое задание на должность Python-разработчик
##### Задача
Перенести тестовую базу кандидатов из Экселя и файлов в Хантфлоу, используя [Хантфлоу API](https://github.com/huntflow/api). 
Данные для входа в Хантфлоу и `access_token` будут предоставлены вместе с заданием.

##### Состав задачи

Есть файл с кандидатами `Тестовая база.xslx` с колонками.
Необходимо добавить в Хантфлоу кандидатов из этого файла в базу и на вакансию на соответствующий этап с комментарием (вакансии уже созданы в Хантфлоу).
Кроме этого, в папках с названием вакансии находятся резюме кандидатов, их также необходимо прикрепить к кандидату из Excel.

##### Приемка задачи и оценка выполнения

Будет оцениваться качество переноса информации и ее полнота.
Скрипт должен уметь принимать параметры командной строки (токен и путь к папке с базой).
Плюсом будет умение скрипта запускать заливку с места последнего запуска (на случай сетевых проблем или прерывании выполнения), например, с определенной строки.
Также, плюсом будет ссылка на выполненное задание на GitHub.

##### Структура папок для загрузки
 - Frontend-разработчик (папка)
    - Иванов Иван.doc
    - Сидоров Сидор Сидорович.pdf
 - Менеджер по продажам (папка)
    - Петров Петр Петрович.pdf
 - Тестовая база.xlsx
 
#### Требования к ПО
- Установленный Python 3.7
- Установленный инструмент для работы с виртуальными окружениями virtualenv
```bash
pip install virtualenv
```

#### Установка
```bash
git clone https://github.com/arkuz/huntflow_test
cd huntflow_test
virtualenv venv
venv/scripts/activate
pip install -r requirements.txt
```

#### Функциональность скрипта
1. Скрипт принимает параметры командной строки (токен и путь к папке с базой).
2. Добавляет в Хантфлоу кандидатов из файла в базу на вакансию на соответствующий этап с комментарием (вакансии уже созданы в Хантфлоу).
3. Прикрепляет резюме к кандидату из Excel.
4. Умеет запускать заливку с места последнего запуска (на случай сетевых проблем или прерывании выполнения)


#### Запуск
```bash
python main.py "aaa" "D:\candidats\Тестовая база.xlsx"
```

#### Результат выполнения
```bash
(venv) D:\GitHub\huntflow_test>python main.py "aaa" "D:\candidats\Тестовая база.xlsx"
Получение справочников
Загрузка данных из файла
Загрузка списка кандидатов
 - "Иванов Иван" успешно загружен
 - "Сидоров Сидор Сидорович" успешно загружен
 - "Петров Петр Петрович" успешно загружен
Загрузка завершена успешно
```
