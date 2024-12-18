Описание:

Этот проект использует нейросети, построенную с помощью PyTorch и Tensorflow, а так же алгоритм на основе бибилотеки Sklearn, для генерации славянских имен на основе двух заданных слов. 
Модель обучена на наборе данных, содержащем существующие имена и исходные слова, из которых они были образованы, и может предлагать новые имена, комбинируя введенные слова.
!Важно!
В таблице имена.csv должно присутвовать хотя бы одно имя образованное из каждого слова.


Структура Данных:

    Таблица имена.csv должна содержать следующие столбцы:
    
        Имя: Имя, образованное из двух слов.
        Составляющее 1: Первое слово, из которого образовано имя.
        Составляющее 2: Второе слово, из которого образовано имя.
        Пол: Пол, отнесенный к имени (например, мужское, женское).

        Пример строки:
            Имя	Составляющее 1	Составляющее 2	Пол
            Белослава Белый	Слава	Женский

Установка и Запуск:

    Клонирование репозитория: bash git clone https://github.com/Pelmemant/Diplom.git cd name-generator

    Установка зависимостей: Убедитесь, что у вас установлен Python и библиотеки PyTorch, Tensorflow и Sklearn. 

    Запуск тренировки модели: Поместите ваш файл имена.csv в директорию проекта и запустите скрипт: bash python main.py

Пример Использования.

После обучения модели, вы можете сгенерировать новое имя следующим образом:

    Pytorch:
    
          word1 = "Первое слово"
          word2 = "Второе слово"
          gender = "Пол"
          try:
              generated_name = generate_name(word1, word2, gender, model, dataset)
              print(f'Сгенерированное имя: {generated_name}')
![pytorch](https://github.com/user-attachments/assets/17a8ccf5-7d58-4643-be14-1f9cb69ed0fc)


    Tensorflow:
    
          word1 = "Первое слово"
          word2 = "Второе слово"
          gender = "Пол"
          try:
              generated_name = generate_name(word1, word2, gender, model, word_to_idx, gender_to_idx, idx_to_name)
              print(f'Сгенерированное имя: {generated_name}')
![tensorflow](https://github.com/user-attachments/assets/30d9adb1-4cb5-4865-928e-251ce1aed01e)

          
    Sklern
    
          word1 = "Первое слово"
          word2 = "Второе слово"
          gender = "Пол"
          predicted_name = predict_name(word1, word2, gender)
          print(f'Предсказанное имя: {predicted_name}')
![Sklern](https://github.com/user-attachments/assets/dffefe2f-ef62-4e96-aa00-b6fef763c77c)

