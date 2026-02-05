# ⚔️ Classificador de Nível de Herói – Partidas Ranqueadas

Este projeto foi desenvolvido com o objetivo de criar um **classificador de nível de herói** com base no desempenho do jogador em partidas ranqueadas, utilizando **JavaScript** e conceitos fundamentais de **lógica de programação**.

A aplicação implementa uma **função com retorno** que recebe como parâmetros a quantidade de **vitórias** e **derrotas** de um jogador e calcula o **saldo de vitórias**, utilizando a fórmula:

> saldo = vitórias − derrotas

Com base no saldo calculado, o programa classifica o herói de acordo com os seguintes níveis:

- 🪨**Ferro:** saldo menor que 10;
- 🥉**Bronze:** saldo entre 11 e 20;
- 🥈**Prata:** saldo entre 21 e 50;
- 🥇**Ouro:** saldo entre 51 e 80;
- 💎**Diamante:** saldo entre 81 e 90;
- 🔥**Lendário:** saldo entre 91 e 100;
- 👑**Imortal:** saldo maior ou igual a 101.

---

## 🛠️ Tecnologia e Conceitos Utilizados

JavaScript

- Funções com parâmetros e retorno
- Entrada de dados via terminal com prompt-sync
- Variáveis para armazenamento de dados
- Operadores aritméticos, relacionais e lógicos
- Estrutura de decisão switch case
- Template strings para exibição de mensagens

---

#### 📤 Saída Esperada
Ao final da execução, o programa exibe a seguinte mensagem no terminal:

> O Herói tem de saldo de {saldoVitorias} está no nível de {nivel}

---

## 🚀 Objetivo do Projeto
Este projeto tem como finalidade reforçar conceitos essenciais de programação, como:

1. fixação sobre os conceitos:
   - Variáveis;
   - Operadores;
   - Laços de repetição;
   - Estruturas de decisões;
   - Funções.
2. organização de código;
3. reutilização de funções;
4. separação entre entrada, processamento e saída de dados.

Servindo como base para desafios mais avançados e aplicações futuras.

---

## ✨Por fim, o código feito para esse desafio de projeto:

```javascript

const prompt = require("prompt-sync")()

//declarando a função com retorno para calcular o saldo de vitórias em partidas rakeadas
function calculateMatches(victories , defeats){
    return victories - defeats
}

//aqui é a entrada dos dados através do usúario para que o calculo seja feito
let victories = Number(prompt("Digite a quantidade de vitórias: "))
let defeats = Number(prompt("Digite a quantidade de derrotas: "))

//aqui chamamos o produto da função para utilizarmos no sistema de rank 
let balance = calculateMatches(victories , defeats)
let nivel = ""

//aqui um switch-case simples para, de acordo com o saldo do jogador, mandá-lo para o rank correto 
switch (true) {

    case balance <= 10:
        nivel = "Ferro"
            break

    case balance >= 11 && balance <= 20:
        nivel = "Bronze"
            break
            
     case balance >= 21 && balance <= 50:
        nivel = "Prata"
            break    
            
     case balance >= 51 && balance <= 80:
        nivel = "Ouro"
            break      
            
     case balance >= 81 && balance <= 90:
        nivel = "Diamante"
            break          

     case balance >= 91 && balance <= 100:
        nivel = "Lendário"
            break          

    default: 
        nivel = "Imortal"        
}

console.log(`O herói tem saldo de ${balance} e está no nível de ${nivel}`)
