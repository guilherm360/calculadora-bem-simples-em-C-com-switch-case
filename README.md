\\calculadora-bem-simples-em-C-com-switch-case

#include <stdio.h>
#include <math.h>
#include <locale.h>

int main()
{
    
    printf("\nMANUAL:\n");
    printf ("\n PARA SOMA E SUBTRAÇÃO, DIGITE: + OU -\n");
    printf ("\n PARA MULTIPLICAÇÃO E DIVISÂO, DIGITE: * OU /\n");
    printf ("\n PARA POTÊNCIA, RAIZ E LOG, DIGITE: ^, R OU L (MAIUSCULO)\n");
    
    
    
    
    int n1, n2, conta;
    double conta_div, conta_raiz, conta_log;

    char operator;
    
    scanf ("%d %c %d", &n1, &operator, &n2 );
    
    switch (operator) {
        case '+':
        conta = n1 + n2;
        printf ("%d", conta);
        break;
         case '-':
        conta = n1 - n2;
        printf ("%d", conta);
        break;
         case '*':
        conta = n1 * n2;
        printf ("%d", conta);
        break;
        case '/':
        if (n2 != 0) {
            conta_div = n1/n2;
            printf ("%lf", conta_div);
        }
        else printf("conta invalida");
        break;
        case 'R':
            if (n1 != 0) {
            conta_raiz = sqrt(n1);
            printf ("%lf", conta_raiz);
        } else 
          printf ("conta invalida");
        break;
        case 'L':
        if (n1 != 0) {
            conta_log = log(n1);
            printf("%lf", conta_log);
        } else printf ("conta invalida");
        break;

    return 0;
                      }
}

