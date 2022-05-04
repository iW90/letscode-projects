# Exercício 03

Coloque, num algoritmo, um processo de chamada em sala de aula.

```
programa
{
	inclua biblioteca Texto --> txt
	
	funcao inicio()
	{
		cadeia nomes[5] = {"Alberto","Beatriz","Carlos","Diana","Erasmo"}
		cadeia presenca[5]
		
		para(inteiro i = 0; i < 5; i++){
			escreva(nomes[i]," está presente(S/N)? ")
			leia(presenca[i])
			presenca[i] = txt.caixa_alta(presenca[i])

			se (presenca[i] == "S") {
				presenca[i] = "Presente"
				limpa()
			} senao {
				se (presenca[i] == "N") {
						presenca[i] ="Faltou"
						limpa()
				} senao {
						escreva("Resposta inválida.\n")
						i--
				}
			}
		}
		escreva("\t   LISTA DE PRESENÇA:\n")
		para(inteiro i = 0; i < 5; i++) {
			escreva("\t", nomes[i],": \t", presenca[i], "\n")
		}
		escreva("\n")
	}
}

```