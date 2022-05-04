# Exercício 04

Calcule a idade de uma pessoa de acordo com a data de nascimento dela. Você deve solicitar dia, mês e ano.

```
programa
{	
	funcao inicio()
	{
		inteiro diaNasc, mesNasc, anoNasc
		inteiro diaAtual, mesAtual, anoAtual
		inteiro anobiatual, anobinasc
		inteiro idade

		// Ano atual
		escreva("Em que ano estamos: ")
		leia(anoAtual)

		se ((anoAtual % 400 == 0) ou (anoAtual % 4 == 0) e (anoAtual % 100 != 0)) {
			anobiatual = 29
		} senao {
			anobiatual = 28
		}
		limpa()

		// Validação de mês atual
		faca {		
			escreva("Em que mês estamos (1 a 12): ")
			leia(mesAtual)
	
			se (mesAtual < 1 ou mesAtual > 12) {
				escreva("\nMês inválido. Digite um número entre 1 e 12 correspondente ao mês desejado.\n")
	        	}
        	} enquanto (mesAtual < 1 ou mesAtual > 12)
        	limpa()

		// Validação de dia atual
		faca {		
			escreva("Em que dia estamos (1 a 31): ")
			leia(diaAtual)
	
			se (diaAtual < 1 ou diaAtual > 31) {
				escreva("\nDia inválido. Digite o dia (entre 1 e 31).\n")
	        	} senao se (mesAtual == 2 e diaAtual > anobiatual) {
	        		escreva("\nDia inválido. No ano informado, fevereiro possui ", anobiatual, " dias.\n")
	        	} senao se (mesAtual == 4 ou mesAtual == 6 ou mesAtual == 9 ou mesAtual == 11) {
	        		escreva("\nDia inválido. O mês informado possui 30 dias.\n")
			}
        	} enquanto (diaAtual < 1 ou (diaAtual > 31 ou diaAtual > anobiatual ou (mesAtual == 4 ou mesAtual == 6 ou mesAtual == 9 ou mesAtual == 11) e diaAtual > 30))
        	limpa()

		// Validação de ano de nascimento
		faca {		
			escreva("Em que ano a pessoa nasceu: ")
			leia(anoNasc)
	
			se (anoNasc > anoAtual) {
				escreva("\nAno inválido. Esta pessoa ainda não nasceu. Digite o ano corretamente.\n")
			}
		} enquanto (anoNasc > anoAtual)

		se ((anoNasc % 400 == 0) ou (anoNasc % 4 == 0) e (anoNasc % 100 != 0)) {
			anobinasc = 29
		} senao {
			anobinasc = 28
		}
		limpa()

		// Validação de mês de nascimento
		faca {		
			escreva("Em que mês a pessoa nasceu (1 a 12): ")
			leia(mesNasc)
	
			se (mesNasc < 1 ou mesNasc > 12) {
				escreva("\nMês inválido. Digite um número entre 1 e 12 correspondente ao mês desejado.\n")
	        	}
        	} enquanto (mesNasc < 1 ou mesNasc > 12)
        	limpa()

		// Validação de dia de nascimento
		faca {		
		escreva("Em que dia a pessoa nasceu: ")
			leia(diaNasc)
	
			se (diaNasc < 1 ou diaNasc > 31) {
				escreva("\nDia inválido. Digite o dia (entre 1 e 31).\n")
	        	} senao se (mesNasc == 2 e diaNasc > anobinasc) {
	        		escreva("\nDia inválido. No ano informado, fevereiro possui ", anobinasc, " dias.\n")
	        	} senao se ((mesNasc == 4 ou mesNasc == 6 ou mesNasc == 9 ou mesNasc == 11) e diaNasc > 30) {
	        		escreva("\nDia inválido. O mês informado possui 30 dias.\n")
			}
        	} enquanto (diaNasc < 1 ou (diaNasc > 31 ou diaNasc > anobinasc ou (mesNasc == 4 ou mesNasc == 6 ou mesNasc == 9 ou mesNasc == 11) e diaNasc > 30))
        	limpa()		

		// Cálculo de idade
		se (mesNasc == mesAtual e diaNasc == diaAtual) {
			idade = anoAtual - anoNasc
			escreva("Parabéns! A pessoa faz ", idade, " anos hoje!")
		} senao se (mesNasc > mesAtual ou (mesNasc == mesAtual e diaNasc > diaAtual)) {
			idade = anoAtual - anoNasc - 1
			escreva("A pessoa tem ", idade, " anos.")
		} senao {
			idade = anoAtual - anoNasc
			escreva("A pessoa tem ", idade, " anos.")
		}
		escreva("\n\n")
	}
}

```