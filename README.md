
![alt text](https://i.ibb.co/YkCTsXy/index.png)

# Серверная часть


## Что реализовано на данный момент?
____

- 1. Обучена модель speech-to-text с использованием движка DeepSpeech(https://clck.ru/NHxSj). 

- 2. На гугл-диске лежат следующие файлы: 

  - output.graph - обученная модель, 
  - kenlm.scorer - языковая модель, необходимая для запуска модели и коректного распознавания текста,
  - train-* - чекпоинты, полученные в процессе обучения модели.
  - LaunchModel.ipynb - руководство по запуску
  
- 3. Реализован удобный сервис для разметки датасетов, необходимых для последующего обучения модели:

  - git clone https://github.com/YurchenkoDD/VirusHack.git
  - cd VirusHack/Server
  - pip install -r requirements.txt
  - python main.py путь к файлу с алфавитом, путь к файлу с текстовой транскрипцией, путь с аудиодорожками, путь для сохранения CSV файлов
  
- 4. Реализован переводчик с помощью библиотеки googletrans:

  - cd VirusHack/Server/translate 
  - python translate.py
  
## Что планируем реализовать?
____

- 1. Реализация архитектуры client-server с ориентировкой на высоконагруженность.
- 2. Обучение нейронной сети для анализа контекста текста и выделение важных моментов.
- 3. Доработка переводчика.
____

# Клиентская часть

## Что реализовано на данный момент?
____
- 1. Реализованы практически все запланированные экраны(https://clck.ru/NHyfd)
- 2. Реализован основной функционал:
   - Добавление конференций;
   - Запись аудиопотока и отправка его на сервер;
   - Получение текстового файла с сервера и выдача его пользователю;
   - Сохранение файла в разных форматах.
  
## Что планируем реализовать?
____
- 1. Реализация субтитров
- 2. Реализация перевода текста на разные языки
