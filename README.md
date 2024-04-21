# aeds.1
#include <stdio.h>

int main() {
    int contador = 1;
    int peso, g;
    int h = 0, m = 0;
    float somapesos = 0.0, media;
    int maiorgenero;

    while (contador <= 5) {
        printf("Digite o peso da pessoa %d: ", contador);
        scanf("%d", &peso);

        printf("Digite o gênero da pessoa %d (1 - Masculino, 2 - Feminino): ", contador);
        scanf("%d", &g);

        somapesos += peso;

        if (g == 1) {
            h++;
        } else if (g == 2) {
            m++;
        }

        contador++;
    }

   
    media = somapesos / 5.0;

    
    if (h > m) {
        maiorgenero = 1; // Masculino
    } else if (m > h) {
        maiorgenero = 2; // Feminino
    } else {
        maiorgenero = 0; // Igual
    }

    printf("\nNúmero de homens: %d\n", h);
    printf("Número de mulheres: %d\n", m);
    printf("Média dos pesos: %.2f\n", media);

    if (maiorgenero == 1) {
        printf("O gênero com maior ocorrência é: Masculino\n");
    } else if (maiorgenero == 2) {
        printf("O gênero com maior ocorrência é: Feminino\n");
    } else {
        printf("Há o mesmo número de homens e mulheres no grupo.\n");
    }

    return 0;
}
