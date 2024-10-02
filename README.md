# Система обработки фотографий с карточек товаров на маркетплейсах
## Описание
Этот проект предназначен для сегментации изображений и замены фона с использованием предобученной модели U-Net. Основная цель — выделить объект на изображении и заменить исходный фон на заданный. Проект демонстрирует применение методов компьютерного зрения и глубокого обучения для решения задачи сегментации объектов.

## Основные возможности
Сегментация объектов на изображениях с помощью модели U-Net. 
Замена фона на изображении любым другим изображением или цветом.
Поддержка работы с произвольными изображениями.

## Особенности
### Модель
- Используется модель U-2-Net, архитектура для задач обнаружения и сегментации объектов. Модель состоит из кодирующей и декодирующей частей, что позволяет эффективно выделять объекты на изображении и заменять фон. [Репозиторий с оригинальной моделью](https://github.com/NathanUA/U-2-Net.git)
- В качестве предсказаний берется выход первого слоя модели
### Данные
- Класс ImageDataset хранит путь до изображений для обработки
- Изображения загружаются в модель по одному при помощи dataloader
### Создание фона
- Желаемый цвет фона задается в формате RGB (BACKGROUND_COLOR_RGB), на него накладываются гауссовский шум и вертикальное затемнение
- Тень объекта  создается по форме маски, предсказанной моделью, и накладывается на фон


## Пример работы алгоритма
<img height="300" alt="ar1" src="https://github.com/user-attachments/assets/18182965-b047-4613-bf71-9ac568a4eead">

<img height="300" alt="ar1" src="https://github.com/user-attachments/assets/f22c3f42-5ab9-4170-8bc4-bde4c0bb76e9">

<img height="300" alt="ar1" src="https://github.com/user-attachments/assets/1c883db0-8ac4-4772-a62c-058ff83ee766">

<img height="300" alt="ar1" src="https://github.com/user-attachments/assets/df3c4686-b568-4cb0-858f-ef801e59473f">

## Использованные библиотеки 
- Numpy
- PyTorch
- OpenCV
  
