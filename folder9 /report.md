# Отчет по лабораторной работе № 8
## по курсу "Фундаментальная информатика"

Студент группы М8О-108Б-23 Фролов Вячеслав Витальевич

Работа выполнена 

Преподаватель: каф. 806 Севастьянов Виктор Сергеевич

1. **Тема**: Системы программирования на языке Си
2. **Цель работы**: Составление и отладка простейшей программы на Си итеративного характера с целочисленными рекурентными соотношениями, задающими некоторое регулярное движение точки в целочисленной системе координат (i, j) с дискретным временем k и динамическим параметром движения l.
3. **Задание (вариант №4)**: Кольцо ограниченное двумя окружностями с центром в точке (10, 10), радиус внутренней равен 5, а радиус внешней 10.
4. **Протокол**: 

```
#include <stdio.h>


int sgn(int a) {
    if (a > 0)
    {
        return 1;
    }
    if (a == 0)
    {
        return 0;
    }
    if (a < 0)
    {
        return -1;
    }
    }

int max(int a, int b,  int c) 
{
    if (a > b && a > c)
    {
        return a;
    }
    if (b > a && b > c)
    {
        return b;
    }
    if (c > a && c > b)
    {
        return c;
    }
}

int min(int a, int b)
{
    if (a < b)
    {
        return a;
    }
    else
    {
        return b;
    }
}

int main()
{
    int i, j, l, flag, a;
    flag = 1;
    i = 24;
    j = 8;
    l = -3;
    a = 0;
    /*(x - 10) ** 2 + (y - 10) ** 2 = 25 - уравнения окружностей
    (x - 10) ** 2 + (y - 10) ** 2 = 25*/ 
    for (int k = 0; k < 50; k++)
    {
     i = min(i + j, i + l) * (k + 1) % 30;
     j = j + l * sgn(j) % 20 + k * sgn(i) % 10;
     l = max(i * j, i * l, j * l);
     if ((i - 10) * (i - 10) + (j - 10) * (j - 10) >= 25 && (i - 10) * (i - 10) + (j - 10) * (j - 10) <= 100) 
     {
        printf("Попадание, шаг - %d \n", a);
        flag = 0;
        break;
     }
    a += 1;
    }
    if (flag == 1)
    {
        puts("Непопадание \n");
    }

    return 0;
}
```

Вердикт: точка не попадает в ограниченную территорию

5. **Вывод**: Данная работа понравилась мне больше предыдущей. Она задействует полученные знания по работе с алгоритмами и требует понимания основ языка программирования Си. Несмотря на свою простоту, помогает вспомнить, как писать основные конструкции на языке Си.
