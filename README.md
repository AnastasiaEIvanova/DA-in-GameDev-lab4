# Анализ данных в разработке игр
Отчет по лабораторной работе #4 выполнил(а):
- Иванова Анастасия Евгеньевна
- РИ-230911
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.


[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.  Создайте пустой проект на Unity.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2. Добавьте пустой объект Empty Game Object с именем Perceptron.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3. Подключите Perceptron.cs к пустому Game Object с именем Perceptron.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
Научиться работать с перцептроном и самостоятельно обучить его на примере простейших логических операций

## Цель работы
Научиться работать с перцептроном и самостоятельно обучить его на примере простейших логических операций

## Задание 1
### В проекте Unity реализовать перцептрон, который умеет производить вычисления:
#### OR | дать комментарии о корректности работы
#### AND | дать комментарии о корректности работы
#### NAND | дать комментарии о корректности работы
#### XOR | дать комментарии о корректности работы
Для всех вычислений, я видоизменила вывод в консоль, для большей наглядности. А именно, я убрала вывод весов и добавила к выводу кол-ва ошибок номер эпохи.

- OR.

![image](https://github.com/user-attachments/assets/68bdec8c-c3d5-4f6f-a132-e024a57ee9f2)

![image](https://github.com/user-attachments/assets/ac88cca0-7bc3-4dc4-a021-5b3a62079254)

В результате тестов, я увидела, что перцептрон стабильно обучается и пытается не допускать ошибок в 5 эпохе.

- AND. 

![image](https://github.com/user-attachments/assets/87832d62-bcbe-45c2-92c2-71078a905b12)

![image](https://github.com/user-attachments/assets/20d735a9-337e-4f7e-ae20-a4cfc6cc9af3)

В результате тестов, я увидела, что перцептрон обучается не так стабильно как с OR, чаще обучается не допускать ошибок ближе в 5-6 эпохе

- NAND.

![image](https://github.com/user-attachments/assets/c3d8de3d-8916-410d-a5fb-9d8bb899b17b)

![image](https://github.com/user-attachments/assets/9f8cf165-10eb-44c0-8264-745e3ad4e6ab)

Ситуация аналогичная, как с AND. Перцептрон обучается не совсем стабильно, но чаще обучается не допускать ошибок ближе к 6 эпохе.

- XOR.

![image](https://github.com/user-attachments/assets/839e2338-4ef0-41d5-858d-e99c461416ab)

![image](https://github.com/user-attachments/assets/adfdd6d8-f88d-4ae3-ac08-f762b3d0d72c)

Сколько попыток бы я не делала, перцептрону не удалость обучиться даже за 8 эпох.

## Задание 2
### Построить графики зависимости количества эпох от ошибки  обучения. Указать от чего зависит необходимое количество эпох обучения.
Графики зависимости кол-ва эпох от ошибки обучения:
![Task2-Lab4](https://github.com/user-attachments/assets/1399be65-eb23-4e38-a236-92160bda3027)

Из представленных выше графиков можно сделать вывод, что количество эпох обучения зависит от уровня сложности задачи. 
Например, для решения нелинейной задачи XOR перцептрону требуется намного больше восьми эпох. 
Количество эпох также зависит от степени изменения весов. 
Я заметила, что перед тем как количество ошибок начинает резко уменьшаться, перцептрон делает дополнительную ошибку, скорее всего это необходимо для исключения неправильных вариантов.

Ссылка на таблицу: [Ссылка на таблицу.](https://docs.google.com/spreadsheets/d/1PerPZ7JX-0dAS9iaM3vGdOorloNifJJ3ro5lMmF62CU/edit?gid=0#gid=0)


## Задание 3
### Построить визуальную модель работы перцептрона на сцене Unity.
Я построила визуальную модель работы перцептрона используя простейшие кубы в Unity. 
Я разукрасила их в белые и черные цвета, которые обозначают 0 и 1.

- OR:
До

![image](https://github.com/user-attachments/assets/a8f68c44-36ab-4137-9950-4214c4713a86)

После

![image](https://github.com/user-attachments/assets/825e4476-a669-4d1a-83d0-338adc0ae494)

- AND:
До

![image](https://github.com/user-attachments/assets/cb870768-dd55-45ad-ae87-f678f4832c11)

После

![image](https://github.com/user-attachments/assets/32d28132-4804-4996-bc1b-d70ab4d8191b)

- NAND:
До

![image](https://github.com/user-attachments/assets/a70b5fa0-f07c-4039-a1ff-ef221a53df8e)

После

![image](https://github.com/user-attachments/assets/88be404d-337f-497e-9e7f-16f4c30d8dcd)

- XOR:
До

![image](https://github.com/user-attachments/assets/1a5bb370-9064-4a1e-84bc-c47f2d94638a)

После

![image](https://github.com/user-attachments/assets/0e252a51-beec-4862-a6bb-6d41afaf7ffb)

## Выводы
В этой работе я научилась работать с перцептроном. 
Он самостоятельно обучался на примере логических операций OR, AND, NAND, XOR. 
Я визуализировала данные, полученные при обучении, узнала про роль весов и разобралась, как в целом работает перцептрон.

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
