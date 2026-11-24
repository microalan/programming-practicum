# Задание 1. Сигнатура функции


Напишите сигнатуру (заголовок) функций.


### Задание 1.1
Напишите заголовок функции `print_hello`, которая выводит в консоль сообщение `"Hello!"`

<details>
<summary>Ответ</summary>

```c
void print_hello();
```

</details>


### Задание 1.2
Напишите заголовок функции `square`, которая возводит целое число в квадрат.

<details>
<summary>Ответ</summary>

```c
int square(int x);
```
</details>


### Задание 1.3
Напишите заголовок функции `max_number`, которая возвращает наибольшее из переданных двух целых чисел.

<details>
<summary>Ответ</summary>

```c
int max_number(int a, int b);
```
</details>


### Задание 1.4
Напишите заголовок функции `circle_area`, которая по радиусу (вещественное число) находит площадь круга.

<details>
<summary>Ответ</summary>

```c
double circle_area(double r);
```

</details>


### Задание 1.5
Напишите заголовок функции `array_sum`, которая находит сумму элементов массива.

<details>
<summary>Ответ</summary>

```c
int array_sum(const int *arr, int n);
```
</details>


### Задание 1.6
Напишите заголовок функции `fill_zero`, которая заполняет массив целых чисел нулями

<details>
<summary>Ответ</summary>

```c
void fill_zero(int *arr, int n);
```
</details>


### Задание 1.7

Напишите заголовок функции `find_elem`, которая ищет индекс заданного элемента в массиве.

<details>
<summary>Ответ</summary>

```c
int find_elem(int *arr, int n, int elem);
```
</details>


### Задание 1.8
Напишите заголовок функции `swap`, которая меняет местами значения двух целых переменных.

<details>
<summary>Ответ</summary>

```c
void swap(int *a, int *b);
```
</details>


### Задание 1.9
Напишите заголовок функции `min_max`, которая находит минимум и максимум в массиве и «возвращает» их через параметры-указатели.

<details>
<summary>Ответ</summary>

```c
void min_max(const int *arr, int n, int *min_out, int *max_out);
```
</details>


### Задание 1.10
Напишите заголовок функции `copy_string`, которая копирует строку в буфер, за исключением пробелов, и возвращает размер новой строки.

<details>
<summary>Ответ</summary>

```c
int copy_string(const char *str1, char *str2);
```
</details>
