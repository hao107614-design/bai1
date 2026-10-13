# #include <stdio.h>
#include <math.h>
void PhuongTrinhBacHai(float a, float b, float c) {
    printf("\nGiai phuong trinh: %.2fx^2 + %.2fx + %.2f = 0\n", a, b, c);

    if (a == 0) {
        if (b == 0) {
            if (c == 0) {
                printf("-> Phuong trinh vo so nghiem.\n");
            } else {
                printf("-> Phuong trinh vo nghiem.\n");
            }
        } else {
            float x = -c / b;
            printf("-> Phuong trinh co 1 nghiem duy nhat: x = %.2f\n", x);
        }
    } 
    else {
        float delta = b * b - 4 * a * c;
        printf("-> Delta = %.2f\n", delta);
        if (delta < 0) {
            printf("-> Phuong trinh vo nghiem thuc.\n");
        } else if (delta == 0) {
            float x = -b / (2 * a);
            printf("-> Phuong trinh co nghiem kep: x1 = x2 = %.2f\n", x);
        } else {
            float x1 = (-b + sqrt(delta)) / (2 * a);
            float x2 = (-b - sqrt(delta)) / (2 * a);
            printf("-> Phuong trinh co 2 nghiem phan biet:\n");
            printf("   x1 = %.2f\n", x1);
            printf("   x2 = %.2f\n", x2);
        }
    }
}

int main() {
    float a, b, c;
    printf("Nhap a: ");
    scanf("%f", &a);
    printf("Nhap b: ");
    scanf("%f", &b);
    printf("Nhap c: ");
    scanf("%f", &c);
    PhuongTrinhBacHai(a, b, c);

    return 0;
}
