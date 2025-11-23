Um código criado em C para calcular média de um aluno 



#include <stdio.h>



// Função para calcular a média

float calcularMedia(float notas[], int qtd)

{

  float soma = 0;

  for (int i = 0; i < qtd; i++)

  {

    soma += notas[i];

  }

  return soma / qtd;

}



// Função para encontrar a maior nota

float maiorNota(float notas[], int qtd)

{

  float maior = notas[0];

  for (int i = 1; i < qtd; i++)

  {

    if (notas[i] > maior)

    {

      maior = notas[i];

    }

  }

  return maior;

}



// Função para encontrar a menor nota

float menorNota(float notas[], int qtd)

{

  float menor = notas[0];

  for (int i = 1; i < qtd; i++)

  {

    if (notas[i] < menor)

    {

      menor = notas[i];

    }

  }

  return menor;

}



// Função para exibir o menu

void menu(float notas[], int qtd)

{

  int opcao;

  do

  {

    printf("\n** MENU ESTATÍSTICO **\n");

    printf("1 - Calcular Média\n");

    printf("2 - Maior Nota\n");

    printf("3 - Menor Nota\n");

    printf("4 - Listar Notas\n");

    printf("0 - Sair\n");

    printf("Escolha uma opção: ");

    scanf("%d", &opcao);



    switch (opcao)

    {

    case 1:

      printf("Média das notas = %.2f\n", calcularMedia(notas, qtd));

      break;

    case 2:

      printf("Maior nota = %.2f\n", maiorNota(notas, qtd));

      break;

    case 3:

      printf("Menor nota = %.2f\n", menorNota(notas, qtd));

      break;

    case 4:

      printf("Notas inseridas: ");

      for (int i = 0; i < qtd; i++)

      {

        printf("%.2f ", notas[i]);

      }

      printf("\n");

      break;

    case 0:

      printf("Encerrando...\n");

      break;

    default:

      printf("Opção inválida!\n");

    }

  } while (opcao != 0);

}



int main()

{

  float notas[10];

  int i = 0;

  float entrada;



  while (i < 10)

  {

    printf("Digite a %dª nota (-1 para encerrar): ", i + 1);

    scanf("%f", &entrada);



    if (entrada == -1)

    {

      printf("\nFinalizada inclusão de notas.\n");

      break; // Encerra o loop se o usuário digitar -1

    }

    // Verifica se a nota está entre 0 e 10

    if (entrada < 0 || entrada > 10)

    {

      printf("Nota inválida! Digite entre 0 e 10.\n");

      continue; // Pede a nota novamente

    }

    // Se passou pela validação, a nota é válida

    printf("A %dª nota é válida: %.2f\n", i + 1, entrada);



    notas[i] = entrada;

    i++;

  }



  if (i == 0)

  {

    printf("Nenhuma nota válida foi inserida.\n");

  }

  else

  {

    menu(notas, i);

  }



  return 0; 

}
