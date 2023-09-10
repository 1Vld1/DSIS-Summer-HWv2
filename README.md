# DSIS-Summer-HW

В качестве выборки в рамках домашнего задания по курсу DSIS была выбрана cicids_static_data
https://www.kaggle.com/datasets/mohammednamory/cybersecurity

Набор данных "Cyber Security Indexes" включает в себя 79 свойств и 25190 строк. Все свойства типа float, кроме свойства 'Label', которое является значением типа str


# Ход работы
Первым делом проанализировал содержание csv-файла:
<img width="838" alt="image" src="https://github.com/1Vld1/DSIS-Summer-HWv2/assets/70940443/f3304371-5a55-40fa-9bd5-c5bef3b06f07">

Отсортировал порты по частоте обращения к ним:
<img width="443" alt="image" src="https://github.com/1Vld1/DSIS-Summer-HWv2/assets/70940443/258a0b91-c2a2-41a3-9476-d918427d752b">

Построил график для визуализации количества строк с одинаковым портом:
<img width="489" alt="image" src="https://github.com/1Vld1/DSIS-Summer-HWv2/assets/70940443/6161b8d8-e232-48e4-8db7-2455f19de187"> <img width="842" alt="image" src="https://github.com/1Vld1/DSIS-Summer-HWv2/assets/70940443/5f0ef653-0e72-48b7-87a3-a29ba4754634">

Потсроил гистограммы. Одну общую, вторую на увеличенном участке от 0 до 100:
<img width="841" alt="image" src="https://github.com/1Vld1/DSIS-Summer-HWv2/assets/70940443/5fb2e10f-5635-4239-82f6-fd33f839332e">

Попытался проанализировать зависимость общей длины пакета от продолжительности его передачи:
<img width="845" alt="image" src="https://github.com/1Vld1/DSIS-Summer-HWv2/assets/70940443/eaba90b5-6a1c-4bcf-9ed8-d0b3926d0d6e">

Построил тепловую карту корреляции (предварительно высчитав матрицу корреляции) всех признаков (полноразмерная карта в файлах с именем Original.png):
<img width="844" alt="image" src="https://github.com/1Vld1/DSIS-Summer-HWv2/assets/70940443/9631d46c-7621-4cf1-9e18-4186fb6ff9d5">

Отсортировал и вывел пары свойств с корреляцией больше 0.99:
<img width="680" alt="image" src="https://github.com/1Vld1/DSIS-Summer-HWv2/assets/70940443/cc18cb44-06d8-41b7-86cc-87e40601b1ee">

Построил тепловую карту корреляции признаков с корреляцией больше 0.99 (полноразмерная карта в файлах с именем Merged.png):
<img width="843" alt="image" src="https://github.com/1Vld1/DSIS-Summer-HWv2/assets/70940443/cd577885-a5ec-465c-bb20-54762a02e58d">

Разделил данные на два класса по свойству 'Label' на Benign и Attack. Построил по ним тепловый карты в попытке понять, что именно отличает "Норму" от "Атаки" (полноразмерная карта в файлах с именем Attack.png):
<img width="847" alt="image" src="https://github.com/1Vld1/DSIS-Summer-HWv2/assets/70940443/0a974569-2528-44ff-8962-d728eb9d8cb2">

И дополнительно вывел статистику:
<img width="466" alt="image" src="https://github.com/1Vld1/DSIS-Summer-HWv2/assets/70940443/a6dcca35-bd20-447d-a334-6569cf7c9036"> <img width="468" alt="image" src="https://github.com/1Vld1/DSIS-Summer-HWv2/assets/70940443/f29ffe74-6c68-4dc2-94be-fec4f06e1239">

# Выводы
В целом дальше на основе этих данных можно двигаться в сторону Случайного леса (Random Forest) и обучения модели





#Вывод
