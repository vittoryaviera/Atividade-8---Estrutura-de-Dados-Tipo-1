#include <stdio.h>

int fibonacci(int n) {
    if (n <= 0) {
        return 0;
    } else if (n == 1) {
        return 1;
    } else {
        int a = 0;
        int b = 1;
        int result = 0;

        for (int i = 2; i <= n; i++) {
            result = a + b;
            a = b;
            b = result;
        }

        return result;
    }
}

int main() {
    int n;

    printf("Digite um número inteiro n: ");
    scanf("%d", &n);

    if (n < 0) {
        printf("Por favor, insira um número inteiro não negativo.\n");
    } else {
        int result = fibonacci(n);
        printf("O %d-ésimo número da sequência de Fibonacci é: %d\n", n, result);
    }

    return 0;
}
