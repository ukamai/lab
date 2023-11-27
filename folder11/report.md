# Отчет по лабораторной работе № 11
## по курсу "Фундаментальная информатика"

Студент группы М8О-108Б-23 Фролов Вячеслав Витальевич

Работа выполнена 

Преподаватель: каф. 806 Севастьянов Виктор Сергеевич

1. **Тема**: Обработка последовательности литер входного текстового файла.
2. **Цель работы**: Написать программу, выполняющую поставленную задачу.
3. **Задание (вариант №24)**: Подсчитать количество восьмиричных чисел, находящихся в диапазоне от 10 до 1000.
4. **Протокол**: 

```
#include <stdio.h>
#include <ctype.h>


typedef enum {
    STATE_START,
    STATE_OCTAL,
    STATE_OTHER
} State;

int atoi();

int isSep();

int isOctalNumber(const char *str) {
    while (*str) {
        if (!isdigit(*str) || (*str - '0' >= 8)) {
            return 0; 
        }
        str++;
    }
    return 1;  
}

int main() {
    State state = STATE_START;
    char c;
    int numberCount = 0;
    char currentNumber[10];  
    int currentIndex = 0;

    while ((c = getchar()) != EOF) {
        switch (state) {
            case STATE_START:
                if (isdigit(c) && c != '0') {
                    state = STATE_OCTAL;
                    currentIndex = 0;
                    currentNumber[currentIndex++] = c;
                } else if (!isSep(c)) {
                    state = STATE_OTHER;
                }
                break;

            case STATE_OCTAL:
                if (isdigit(c) && c != '8' && c != '9') {
                    currentNumber[currentIndex++] = c;
                } else if (isSep(c)) {
                    currentNumber[currentIndex] = '\0';
                    int value = atoi(currentNumber);
                    if (value >= 10 && value <= 1000 && isOctalNumber(currentNumber)) {
                        numberCount++;
                    }
                    state = STATE_START;
                } else {
                    state = STATE_OTHER;
                }
                break;

            case STATE_OTHER:
                if (isSep(c)) {
                    state = STATE_START;
                }
                break;
        }
    }


    if (state == STATE_OCTAL) {
        currentNumber[currentIndex] = '\0';
        int value = atoi(currentNumber);
        if (value >= 10 && value <= 1000 && isOctalNumber(currentNumber)) {
            numberCount++;
        }
    }

    printf("Количество чисел в восьмеричной системе счисления от 10 до 1000: %d\n", numberCount);

    return 0;
}

int isSep(int ch)
{
    return (ch == ' ' || ch == ',' || ch == '\n' || ch == '\t');
}
```

5. **Вывод**: Работу считаю непрактичной. Она развивает навыки работы с состояниями, но данные задачи можно было решить проще и быстрее, используя циклы.
