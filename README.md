# 5-
#include <stdio.h>
#include <math.h>
#include <locale.h>

int main()
{
    setlocale(LC_ALL, "RUS");

    double x, y, z, gamma;
    double step1, step2, step3;

    printf("Введите x: ");
    scanf("%lf", &x);

    printf("Введите y: ");
    scanf("%lf", &y);

    printf("Введите z: ");
    scanf("%lf", &z);
    step1 = 5 * atan(x);

    step2 = (1.0 / 4.0) * acos(x)
            * (x + 3 * fabs(x - y) + x * x)
            / (fabs(x - y) * z + x * x);

    gamma = step1 - step2;

    printf("Результат: %lf\n", gamma);

    return 0;
}
