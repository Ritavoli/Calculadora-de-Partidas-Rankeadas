 # DESAFIO - Calculadora de partidas Rankeadas - javascript

 > Este repositório foi criado para resolver a atividade do Bootcamp Potência Tech iFood - Programação do Zero da DIO.  

## Deve ser utilizado
- Variáveis
- Operadores
- Laços de repetição
- Estruturas de decisões
- Funções

## Objetivo:

Criar uma função que recebe como parâmetro a quantidade de vitórias e derrotas de um jogador,
depois disso retorne o resultado para uma variável, o saldo de Rankeadas deve ser feito através do calculo (vitórias - derrotas)

Se vitórias for menor do que 10 = Ferro


Se vitórias for entre 11 e 20 = Bronze


Se vitórias for entre 21 e 50 = Prata


Se vitórias for entre 51 e 80 = Ouro


Se vitórias for entre 81 e 90 = Diamante


Se vitórias for entre 91 e 100= Lendário


Se vitórias for maior ou igual a 101 = Imortal



## Saída

Ao final deve se exibir uma mensagem:
"O Herói tem de saldo de **{saldoVitorias}** está no nível de **{nivel}**"
 

  
## SOLUÇÃO
 > A seguir é apresentado o código desenvolvido para resolver este desafio, onde é  solicitado ao jogador que insira o número de vitórias e de derrotas. Em seguida, realiza o cálculo necessário e, por fim, informa o número de vitórias junto com o nível de classificação do jogador.


  function calcularNivel(vitorias, derrotas) {
    let saldoVitorias = vitorias - derrotas;
    let nivel;

    if (vitorias < 10) {
        nivel = "Ferro";
    } else if (vitorias >= 11 && vitorias <= 20) {
        nivel = "Bronze";
    } else if (vitorias >= 21 && vitorias <= 50) {
        nivel = "Prata";
    } else if (vitorias >= 51 && vitorias <= 80) {
        nivel = "Ouro";
    } else if (vitorias >= 81 && vitorias <= 90) {
        nivel = "Diamante";
    } else if (vitorias >= 91 && vitorias <= 100) {
        nivel = "Lendário";
    } else {
        nivel = "Imortal";
    }

    return { saldoVitorias, nivel };
}

const vitoriasInput = prompt("Informe a quantidade de vitórias:");
const derrotasInput = prompt("Informe a quantidade de derrotas:");

const vitorias = parseInt(vitoriasInput || "0");
const derrotas = parseInt(derrotasInput || "0");

const { saldoVitorias, nivel } = calcularNivel(vitorias, derrotas);
console.log(`O Herói tem um saldo de ${saldoVitorias} está no nível ${nivel}`);
