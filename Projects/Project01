# Classificador de Nível de Herói

Este projeto foi desenvolvido como parte do Bootcamp da DIO em parceria com a Blip, com foco na prática de lógica de programação utilizando JavaScript.

O desafio consiste em criar um programa que armazene o nome e a quantidade de experiência (XP) de um herói e, a partir disso, utilize estruturas de decisão para classificar o herói em diferentes níveis.

---

## No projeto, foi utilizado:

- Variáveis para armazenar o nome, XP e nível do herói;
- Operadores lógicos e relacionais para análise do XP;
- Estrutura switch case para definir o nível do herói;
- Laço de repetição while para permitir o cadastro de múltiplos heróis.

---

Por fim fiz um projeto que permite a entrada de dados via terminal utilizando a biblioteca prompt-sync e permite que o usuário repita o processo de cadastro, tornando a execução dinâmica e interativa.

# Código do Projeto 

```javascript

//prompt-sync - biblioteca node.js que permite digitar dados no terminal como se fosse um prompt()
//require("prompt-sync") - importa a biblioteca e retorna uma função 
//os () no final chamam essa função e criam uma instância 
//const prompt = - guarda essa função pronta na váriavel prompt
const prompt = require("prompt-sync")()

//declarando a váriavel booleana que vai ser "usada" pelo while
let cadastroHeroi = true

//o while aqui funciona como: enquanto a variavel for true então... 
while (cadastroHeroi) {
  //jogando para o usuário contar como é o herói dele
  let nome = prompt("Digite o nome do herói: ")
  let xp = Number(prompt(`Digite o XP do ${nome}: `))
  let nivel = ""

  //aqui começa as análises de cada caso para saber a patente do heroi 
  switch (true) {
    case xp < 1000:
      nivel = "Ferro"
      break

    case xp >= 1001 && xp <= 2000:
      nivel = "Bronze"
      break

    case xp >= 2001 && xp <= 5000:
      nivel = "Prata"
      break

    case xp >= 5001 && xp <= 7000:
      nivel = "Ouro"
      break

    case xp >= 7001 && xp <= 8000:
      nivel = "Platina"
      break

    case xp >= 8001 && xp <= 9000:
      nivel = "Ascendente"
      break

    case xp >= 9001 && xp <= 10000:
      nivel = "Imortal"
      break

    default:
      nivel = "Radiante"
  }

  console.log(`O Herói de nome ${nome} está no nível ${nivel}`)
  
  //se caso colocar s, o programa inicia novamente
  let resposta = prompt("Deseja cadastrar outro herói? (s/n): ")
  // O toLowerCase() transforma todas as letras em minúsculas
  //permitindo que o usuário digite s, S ou Ss, e o programa interprete como "s"
  cadastroHeroi = resposta.toLowerCase() === "s"
}
