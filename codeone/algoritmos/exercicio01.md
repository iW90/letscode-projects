# Exercício 01

Peça um número e valide se este número é divisível por 5.

```
programa {
    funcao inicio() {
        inteiro numero
        inteiro resto

        escreva ("Digite um número: ")
        leia (numero)

        resto = numero % 5

        se (resto == 0) {
            escreva ("O número ", numero," é divisível por cinco")
        }
        senao {
            escreva("o número ", numero," não é divisível por cinco")
        }
    }
}
```