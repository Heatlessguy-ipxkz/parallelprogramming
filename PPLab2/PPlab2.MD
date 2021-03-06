## Параллельное программирование
## Лабораторная работа 2
## Вариант 5

# Коллективные функции В MPI. ОБРАБОТКА МАССИВОВ

### Задание для 5 варианта:

Определить математическое ожидание  и среднее квадратическое отклонение для массива равномерно распределенных случайных чисел.

## Цель работы
Освоить применение коллективных функций MPI для рассылки и сборки с фрагментов массивов и параллельной их обработки по заданному алгоритму. 

## Лабораторное задание

1. Для предложенного алгоритма составить и отладить последовательную программу обработки числовых массивов индивидуального задания. Использовать динамическое выделение памяти для массивов (функции malloc(), calloc(),free()). Входные массивы заполнить случайными числами (см. программу genarg, приложение В).

2. Алгоритм обработки оформить внешней функцией.

3. Для параллельной обработки определить размер порции массива для каждого процесса и смещение порции от начала полного массива.

4. В каждом процессе выделить память для размещения порции массива. Функцией MPI_Scatter или MPI_Scatterv распределить исходный массив(ы) на число процессов, выбранных при запуске программы.

5. В каждом процессе выполнить обработку части массива составленной внешней функцией и разместить результаты в массиве порции или в выходных переменных.

6. Собрать в главном процессе окончательные результаты (функции MPI_Gather(v) или MPI_Reduce.

7. Вывести окончательные результаты. Для больших выходных массивов достаточно вывести первый и последний элементы.

## Содержание отчёта 

В отчет включить:
*  цель работы;
*  индивидуальное задание;
*  описание применяемого способа конструирования порции данных процесса;
*  полный текст параллельной программы;
*  результаты работы программы. 

## Приложение А
см.
[extvec.c](src/ext/extvec.c) и [genarg.c](src/ext/genarg.c)
