# Exercício 02

Receba uma lista de itens e calcule o tamanho desta lista.

```
programa
{
	inclua biblioteca Texto --> txt
	
	funcao inicio()
	{
		inteiro i = 0
		cadeia item = "", lista = " "

		faca
		{
			escreva("Digite um item para lista ou digite FIM se não houver mais itens: ")
			leia(item)
			item = txt.caixa_alta(item)

			se (item != "FIM") {
				se (lista == " ")
				{
					lista += item
				} senao {
					lista += ", " + item
				}
                i++
			}
        } enquanto (item != "FIM")
          
        escreva("\nO número de itens digitados é ", i, ".")
        escreva("\nSua lista de itens é", lista, ".\n\n")
    }
}
```