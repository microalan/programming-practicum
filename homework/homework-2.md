# Домашнее задание 2.

Ниже приведены пары задач, похожие между собой. Первая всегда с решением, вторую вы должны решить самостоятельно аналогичным способом.



## Задание 1. Ввод-вывод одномерного массива

### 1. Пример задачи и решения:

**Условие**: Пользователь вводит целое число n (размер массива, 1 <= n <= MAX_SIZE), затем n целых чисел. Вывести элементы массива на экран в одну строку через пробел.


**Решение**:
```c
#include <stdio.h>

#define MAX_SIZE 100

int main() {
    int n;
    int arr[MAX_SIZE];

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    printf("Enter %d integers: ", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("\nArray:");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }

    return 0;
}
```

### 2. Решите задачу:
**Условие**: Пользователь вводит целое число n (размер массива, 1 <= n <= MAX_SIZE), затем n вещественных чисел. Вывести элементы массива на экран в в обратном порядке с новой строки.


## Задание 2. Заполнение и вывод одномерного массива

### 1. Пример задачи и решения:

**Условие**: Пользователь вводит целое число n (размер массива, 1 <= n <= MAX_SIZE). Массив заполняется квадратами чисел от 1 до n.  Вывести элементы массива с нечётными индексами на экран в одну строку через пробел.


**Решение**:
```c
#include <stdio.h>

#define MAX_SIZE 100

int main() {
    int n;
    int arr[MAX_SIZE];

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    for (int i = 0; i < n; i++) {
        int value = i + 1;
        arr[i] = value * value;
    }

    printf("\nElements at odd indices:");
    for (int i = 1; i < n; i += 2) {
        printf("%d ", arr[i]);
    }

    return 0;
}
```

### 2. Решите задачу:
**Условие**: Пользователь вводит целое число n (размер массива, 1 <= n <= MAX_SIZE). Массив заполняется числами от -1 до -n.  Вывести на экран в одну строку через пробел каждый третий элемент массива (например, `-1 -4 -7 -10` и т.д.).


## Задание 3. Поиск индекса элемента массива

### 1. Пример задачи и решения:

**Условие**: Пользователь вводит целое число n (1 <= n <= MAX_SIZE), затем n целых чисел. Найти индекс максимального элемента и вывести этот индекс и само значение. Если максимальных элементов несколько, вывести индекс первого из них.


**Решение**:
```c
#include <stdio.h>

#define MAX_SIZE 100

int main() {
    int n;
    int arr[MAX_SIZE];

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    printf("Enter %d integers: ", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    int max_index = 0;
    for (int i = 1; i < n; i++) {
        if (arr[i] > arr[max_index]) {
            max_index = i;
        }
    }

    printf("Maximum value: %d\n", arr[max_index]);
    printf("Index of first maximum: %d\n", max_index);

    return 0;
}
```

### 2. Решите задачу:
**Условие**: Пользователь вводит целое число n (1 <= n <= MAX_SIZE), затем n целых чисел, а затем ещё одно целое число **target**. Найти индекс первого вхождения элемента **target** в массив и вывести его. Если такого элемента нет - вывести сообщение об этом.


## Задание 4. Преобразование массива

### 1. Пример задачи и решения:

**Условие**: Пользователь вводит целое число n (1 <= n < MAX_SIZE), затем n целых чисел, затем целое число **pos** (0 <= pos <= n) и целое число **value**. Вставить **value** в массив на позицию **pos**, сдвинув все элементы с индексами `pos...n-1` на одну позицию вправо, и вывести получившийся массив.


**Решение**:
```c
#include <stdio.h>

#define MAX_SIZE 100

int main() {
    int n;
    int arr[MAX_SIZE];

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    printf("Enter %d integers: ", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    int pos, value;
    printf("Enter position and value: ");
    scanf("%d %d", &pos, &value);

    for (int i = n; i > pos; i--) {
        arr[i] = arr[i - 1];
    }
    arr[pos] = value;
    n++;

    printf("Array after insertion:");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }

    return 0;
}
```

### 2. Решите задачу:
**Условие**: Пользователь вводит целое число n (1 <= n <= MAX_SIZE), затем n целых чисел, а затем целое число **pos** (0 <= pos < n). Удалить элемент с индексом **pos**, сдвинув все элементы с индексами `pos+1...n-1` на одну позицию влево, и вывести получившийся массив.


## Задание 5. Ввод-вывод двумерного массива

### 1. Пример задачи и решения:

**Условие**: Пользователь вводит два целых числа rows и cols (1 <= rows, cols <= MAX_SIZE), затем rows * cols целых чисел - элементы матрицы. Сохранить их в двумерный массив и вывести матрицу на экран в виде таблицы.


**Решение**:
```c
#include <stdio.h>

#define MAX_SIZE 100

int main() {
    int rows, cols;
    int matrix[MAX_SIZE][MAX_SIZE];

    printf("Enter rows and cols: ");
    scanf("%d %d", &rows, &cols);

    printf("Enter %d integers: ", rows * cols);
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            scanf("%d", &matrix[i][j]);
        }
    }

    printf("\nMatrix:\n");
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            printf("%4d", matrix[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```

### 2. Решите задачу:
**Условие**: Пользователь вводит два целых числа rows и cols (1 <= rows, cols <= MAX_SIZE), затем rows * cols целых чисел - элементы матрицы по строкам. Cохранить их в двумерный массив и вывести матрицу в транспонированном виде: то есть cols строк по rows элементов, где элемент (i, j) исходной матрицы стоит на месте (j, i).


## Задание 6. Работа с двумерным массивом

### 1. Пример задачи и решения:

**Условие**: Пользователь вводит целое число n (1 <= n <= MAX_SIZE), затем n * n целых чисел - элементы квадратной матрицы. Найти и вывести сумму элементов, стоящих над главной диагональю (не включая саму диагональ).


**Решение**:
```c
#include <stdio.h>

#define MAX_SIZE 100

int main() {
    int n;
    int matrix[MAX_SIZE][MAX_SIZE];

    printf("Enter n: ");
    scanf("%d", &n);

    printf("Enter %d integers: ", n * n);
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            scanf("%d", &matrix[i][j]);
        }
    }

    int sum = 0;
    for (int i = 0; i < n; i++) {
        for (int j = i + 1; j < n; j++) {
            sum += matrix[i][j];
        }
    }

    printf("Sum above main diagonal: %d\n", sum);

    return 0;
}
```

### 2. Решите задачу:
**Условие**: Пользователь вводит целое число n (1 <= n <= MAX_SIZE), затем n * n целых чисел - элементы квадратной матрицы. Найти и вывести произведение элементов, стоящих под главной диагональю (не включая саму диагональ).


## Задание 7. "Рисование" на двумерных массивах

### 1. Пример задачи и решения:

**Условие**: Пользователь вводит два целых числа rows и cols (2 <= rows, cols <= MAX_SIZE). Создайте матрицу rows × cols и  и нарисуйте в ней **рамку**: все элементы на границе (первая строка, последняя строка, первый столбец, последний столбец) были равны `#`, а все внутренние элементы - пробелу ` `. Выведите матрицу.

**Пример вывода для матрицы 4×4:**
```
# # # #
#     #
#     #
# # # #
```

**Решение 1 (заполнение граней отдельными циклами)**:
```c
#include <stdio.h>

#define MAX_SIZE 100

int main() {
    int rows, cols;
    char matrix[MAX_SIZE][MAX_SIZE];

    printf("Enter rows and cols: ");
    scanf("%d %d", &rows, &cols);

    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            matrix[i][j] = ' ';
        }
    }

    for (int j = 0; j < cols; j++) {
        matrix[0][j] = '#';
    }

    for (int j = 0; j < cols; j++) {
        matrix[rows - 1][j] = '#';
    }

    for (int i = 0; i < rows; i++) {
        matrix[i][0] = '#';
    }

    for (int i = 0; i < rows; i++) {
        matrix[i][cols - 1] = '#';
    }

    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            printf("%c ", matrix[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```

**Решение 2 (заполнение граней попарно)**:
```c
#include <stdio.h>

#define MAX_SIZE 100

int main() {
    int rows, cols;
    char matrix[MAX_SIZE][MAX_SIZE];

    printf("Enter rows and cols: ");
    scanf("%d %d", &rows, &cols);

    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            matrix[i][j] = ' ';
        }
    }

    for (int j = 0; j < cols; j++) {
        matrix[0][j] = '#';
        matrix[rows - 1][j] = '#';
    }

    for (int i = 1; i < rows - 1; i++) {
        matrix[i][0] = '#';
        matrix[i][cols - 1] = '#';
    }

    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            printf("%c ", matrix[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```

**Решение 3 (заполнение всех граней в одном цикле)**:
```c
#include <stdio.h>

#define MAX_SIZE 100

int main() {
    int rows, cols;
    char matrix[MAX_SIZE][MAX_SIZE];

    printf("Enter rows and cols: ");
    scanf("%d %d", &rows, &cols);

    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            if (i == 0 || i == rows - 1 || j == 0 || j == cols - 1) {
                matrix[i][j] = '#';
            } else {
                matrix[i][j] = ' ';
            }
        }
    }

    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            printf("%c ", matrix[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```


### 2. Решите задачу:
**Условие**: Пользователь вводит целое нечётное число n (5 <= n <= MAX_SIZE). Заполните квадратную матрицу n × n так, чтобы она изображала упрощённую схему флага Великобритании (Юнион Джек): элементы на главной диагонали, побочной диагонали, а также на средней горизонтальной и средней вертикальной линиях - это `#` (кресты), все остальные элементы - пробел ` ` (фон). Выведите матрицу.


**Пример вывода для матрицы 9×9:**
```
#       #       #
  #     #     #
    #   #   #
      # # #
# # # # # # # # #
      # # #
    #   #   #
  #     #     #
#       #       #
```
