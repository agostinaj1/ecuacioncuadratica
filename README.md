#include <stdio.h>
#include<math.h>

int main() {
    float a, b, c;
    float discriminante, x1, x2;

    printf("Ingrese los coeficientes a, b y c de la ecuacion cuadratica (ax^2 + bx + c = 0):\n");
    scanf("%f %f %f", &a, &b, &c);

    if (a == 0) {
        printf("error: No es una ecuacion cuadratica (a no puede ser 0).\n");
        return 1;
    }

    discriminante = b * b - 4 * a * c;

    if (discriminante > 0) {
        
        x1 = (-b + sqrt(discriminante)) / (2 * a);
        x2 = (-b - sqrt(discriminante)) / (2 * a);
        printf("raices reales y diferentes:\n");
        printf("x1 = %.2f\n", x1);
        printf("x2 = %.2f\n", x2);
    } else if (discriminante == 0) {
        
        x1 = -b / (2 * a);
        printf("raiz real única:\n");
        printf("x = %.2f\n", x1);
    } else {
        
        printf(" La ecuacion no tiene raices reales (discriminante < 0).\n");
    }
    return 0;
}
