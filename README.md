O sistema permite:

✔ Inserção de até 10 notas

✔ Validação das notas (somente valores entre 0 e 10)

✔ Encerramento da inserção com o valor -1

✔ Cálculo da média das notas

✔ Identificação da maior nota

✔ Identificação da menor nota

✔ Exibição de todas as notas cadastradas

✔ Menu interativo com repetição até o usuário optar por sair

O código é dividido em funções para melhor organização:

🔹 calcularMedia()

Recebe um vetor de notas e retorna a média.

🔹 maiorNota()

Percorre o vetor e retorna o maior valor encontrado.

🔹 menorNota()

Retorna a menor nota inserida pelo usuário.

🔹 menu()

Exibe um menu interativo permitindo que o usuário escolha qual estatística visualizar.

📝 Como Usar

Compile o programa:

gcc main.c -o notas


Execute:

./notas


Digite as notas conforme solicitado:

Entre 0 e 10

Ou digite -1 para parar antes das 10 notas

Após o cadastro, escolha uma opção no menu estatístico.

📂 Estrutura do Código
├── main.c
└── README.md

📌 Exemplo de Execução
Digite a 1ª nota (-1 para encerrar): 8
A 1ª nota é válida: 8.00

Digite a 2ª nota (-1 para encerrar): 9
A 2ª nota é válida: 9.00

Digite a 3ª nota (-1 para encerrar): -1

Finalizada inclusão de notas.

** MENU ESTATÍSTICO **
1 - Calcular Média
2 - Maior Nota
3 - Menor Nota
4 - Listar Notas
0 - Sair
Escolha uma opção: 

🧩 Tecnologias Utilizadas

Linguagem C

Compilador GCC / MinGW / Clang

📘 Licença

Este projeto é de uso livre para estudos e melhorias.
