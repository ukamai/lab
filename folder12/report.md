# Отчет по лабораторной работе № 12
## по курсу "Фундаментальная информатика"

Студент группы М8О-108Б-23 Фролов Вячеслав Витальевич

Работа выполнена 

Преподаватель: каф. 806 Севастьянов Виктор Сергеевич

1. **Тема**: 
2. **Цель работы**:
3. **Задание (вариант №24)**:
4. **Протокол**: 


```
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>

typedef enum _state {
    GET_NUM,
    GET_RESULT_POSITIVE,
    GET_RESULT_NEGATIVE
} Estate;

int isSep();

int isdigit();

int isMinus();

int main() {
    Estate state = GET_NUM;
    int ch, count;
    char rab[20];

    while ((ch = getchar()) != EOF) {
        switch (state) {
            case GET_NUM:
                if (isdigit(ch))
                {
                    for (int k; k < sizeof(rab); k++)
                    {
                        rab[k] = 0;
                    }
                    rab[0] = ch;
                    count = 1;
                    state = GET_RESULT_POSITIVE;
                }
                if (isMinus(ch))
                {
                    for (int k; k < sizeof(rab); k++)
                    {
                        rab[k] = 0;
                    }
                    count = 0;
                    state = GET_RESULT_NEGATIVE;
                }
                break;
            case GET_RESULT_POSITIVE:
                if (isdigit(ch))
                {
                    rab[count] = ch;
                    count += 1;
                    state = GET_RESULT_POSITIVE;
                }
                if (isSep(ch))
                {
                    if (count <= 2)
                    {
                    printf("Если убрать крайние числа, длина числа нулевая\n");
                    state = GET_NUM;
                    }
                    else
                    {
                    printf("Изменённое число: ");
                    for (int k = 1; k < count - 1; k++)
                    {
                    printf("%d", rab[k] - 48);
                    }
                    printf("\n");
                    state = GET_NUM;
                    }
                }
                break;
            case GET_RESULT_NEGATIVE:
                if (isdigit(ch))
                {
                    rab[count] = ch;
                    count += 1;
                    state = GET_RESULT_NEGATIVE;
                }
                if (isSep(ch))
                {
                    if (count <= 2)
                    {
                    printf("Если убрать крайние числа, длина числа нулевая\n");
                    state = GET_NUM;
                    }
                    else
                    {
                    printf("Изменённое число: -");
                    for (int k = 1; k < count - 1; k++)
                    {
                    printf("%d", rab[k] - 48);
                    }
                    printf("\n");
                    state = GET_NUM;
                    }
                }
                break;
        }
    }
    return 0;
}

int isMinus(int ch)
{
    return (ch == '-');
}

int isSep(int ch)
{
    return (ch == ' ' || ch == ',' || ch == '\n' || ch == '\t');
}
```
