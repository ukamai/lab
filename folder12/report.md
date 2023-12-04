# Отчет по лабораторной работе № 12
## по курсу "Фундаментальная информатика"

Студент группы М8О-108Б-23 Фролов Вячеслав Витальевич

Работа выполнена 

Преподаватель: каф. 806 Севастьянов Виктор Сергеевич

1. **Тема**: Обработка последовательности литер входного текстового файла.
2. **Цель работы**: Написать программу, выполняющую поставленную задачу.
3. **Задание (вариант №19)**: Отсечь первую и последние цифры числа
4. **Протокол**: 


```
#include <stdio.h>

int change(int number, int c)
{
    int l = 10;
    for (int k = 0; k < c - 2; k++)
    {
        l *= 10;
    }
    number = number % l;
    number = number / 10;
    return number;
}

int main()
{
    int k = 0, chislo, a, length;
    while (k != 1)
    {
        printf("Введите число: ");
        scanf("%d", &chislo);
        a = chislo;
        length = 0;
        while (a != 0)
        {
            a = a / 10;
            length += 1;
        }
        if (length <= 2)
        {
            printf("\n");
        }
        else
        {
        if (chislo > 0)
        {
            printf("%d\n", change(chislo, length));
        }
        else
        {
            chislo = chislo * -1;
            printf("%d\n", change(chislo, length) * -1);
        }
        }
    }

    return 0;
}
```

